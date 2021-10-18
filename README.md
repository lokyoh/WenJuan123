# WenJuan123

## 输入格式为：
    ;,"<类型>","<id>","<问题>","<其他附加值>",;,"<类型>","<id>","<问题>","<其他附加值>",;......;
    其中，问题中的每个常量用 ," 和 ", 包裹（问题中禁止出现半角的 ," 和 ", 字符组合），常量间可用 "," ",," 连接。
    每个问题间用 ; ; 进行分割（开头结尾必须含有 ; ），所有字符在一行中。

## 每个常量的具体描述：
    其中通用的常量为上述输入格式中的 类型,id,问题 。
    id为题目的顺序编号，只能使用 q+数字 ，例如 q1 q123 等等。
    问题为题目的编号和问题，例如 1.这是个问题吗？ 和没编号的 这是个没有编号的问题吗？ 等等，问题中可添加HTML5代码。
    类型为题目的类型，目前只有4个，具体以下再讲。

## 问题的类型、格式以及附加值：
    ### 1.单选题：
        格式为 ,"radio","<id>","<问题>","<答案个数>",+<答案个数>个返回值+<答案个数>个答案（包含编号）
        例如 ,"radio","q1","1.会了吗","2","YES","NO","A.会了","B.不会",
        返回值即为想获得答案返回数据。
    ### 2.简答题：
        格式为 ,"textarea","<id>","<问题>",
        例如 ,"textarea","q2","1附加.说出你学会了的感想。",
    ### 3.自定义题：
        格式为 ,"custom","<id>","<问题>","<自定义答案>",
        例如 ,"custom","q3","2.你会HTML吗，请写下是否会了?","<div class='option'><input class='text' type='text' name='p3' style='width: 50px;'></div>",
        每条自定义答案必须被<div class='option'></div>包裹。
    ### 4.多选题：
        格式为 ,"checkbox","<id>","<问题>","<答案个数>","<最少选择项>","<最多选择项>",+<答案个数>个返回值+<答案个数>个答案（包含编号）
        例如 ,"checkbox","q4","4.你会以下那些语言","6","0","6","java","python","c","c++","c#","go","A.java","B.python","C.c","D.c++","E.c#","F.go",
    ### 可以在问题或答案中添加代码以实现更多的功能
