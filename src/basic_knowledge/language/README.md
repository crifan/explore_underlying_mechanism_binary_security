# 编程语言

* 编程语言种类
  * 机器语言：用二进制编码表示每条指令，是计算机能直接识别和执行的语言。
    * 原理：底层都是0和1的二进制数据
    * 注：理论上来说，程序员也可以写机器语言
      * 只不过太难写，以及没必要直接写，所以实际上没人直接写机器语言
  * 汇编语言
    * 实质和机器语言是相同的，都是直接对硬件操作，只不过指令采用英文缩写的标识符，更容易识别和记忆
    * 组成
      * 指令，伪指令，宏指令
    * 逻辑
      * 你（程序员）写汇编的字母（和要操作的数字等），汇编程序帮你把 汇编的字母（和数字）翻译成0和1的二进制
        * 这样机器才能看懂，才能运行对应程序
  * 高级语言
    * 编写的程序不能直接被计算机识别，必须经过转换（目标代码即机器码）才能被执行
    * 按照转换方式分类
      * 解释类：**边**翻译**边**执行
      * 编译类：**先**翻译**再**执行
    * 常见语言
      * `C`
        * C语言的特点
          * c语言允许直接访问物理地址，可以直接对硬件进行操作
          * c语言程序代码质量高，程序执行效率高
          * c语言使用范围大，可移植性好
      * `C++`
        * 由于：C++编译器优化程度太大
        * 结果：世界上没有C++反编译器
          * 也没有完美的C语言反编译器
            * 很难做到完美