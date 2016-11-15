# 编译程序主模块

* ### 源代码读取模块
    首先提示用户输入源代码文件名字。
    将读取来的源代码每一行作为一个String存在List中，方便其他模块调用。
    ```java
    ArrayList<String> sourceCode;
    ```

# 词法分析模块

* ### 单词类型内部类
    ```
    enum WordType{
        //此处略..
    }
    
    class Word{
        SYM     //存放每个单词的类别
        ID      //存放用户所定义的标识符的值，即标识符字符串的机内表示
        NUM     //存放用户定义的数
    }
    ```

* ### 获取一个字符
    每次从主模块读取一行，存入缓存区，被取空后再去取一行
    ```
    char getch()
    ```

* ### 获取一个单词
    词法分析，获取一个符号
    如果出错，则调用相应的错误处理程序
    ```
    void getsym()
    ```
    
# 语法分析模块
在词法分析的基础上将单词序列分解成各类语法短语
    
# 语义分析模块
审查源程序有无语义错误，为代码生成阶段收集类型信息

# 中间代码生成模块
# 代码优化模块
# 目标代码生成模块
# 错误处理模块
# 解释执行时的存储分配