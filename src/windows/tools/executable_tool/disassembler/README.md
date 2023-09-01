# 反汇编器

* `disassembler`=`反汇编`
  * `反汇编引擎/框架`
    * 名称
      * `反汇编引擎`=`disassembler engine`
      * `反汇编框架`=`disassembler framework`
    * 常见
      * `llvm`
      * `capstone`
        * 详见独立子教程：[Capstone](https://book.crifan.org/books/ultimate_disassembler_capstone/website/)
      * `Ollydbg`的`ODDisasm`
        * `ODDisasm`= `Ollydbg Disassembler` = [Disasm()](http://www.ollydbg.de/Help/Disasm.htm)
        * 官网
          * [Assembling and disassembling](http://www.ollydbg.de/Help/i_Disasm.htm)
      * `BeaEngine`
      * `udis86`
      * `XDE`
    * 对比
      * udis86 vs BeaEngine vs capstone
        * 细节
          * 性能：`udis86 > BeaEngine > capstone`
          * 解码能力：`capstone > BeaEngine > udis86` (udis86不支持寄存器分析,其余解码能力是相近的)
          * 平台支持：`capstone > (udis86 = BeaEngine)`
          * X86扩展指令集：`capstone` > (`udis86` ≈ `BeaEngine`)
        * 结论
          * 如果你需要的是一个X86/64下的性能又好同时解码能力又强的反汇编引擎，并且不需要寄存器分析这种特技的话，那么udis86合适你
          * 如果你还需要带寄存器分析功能的话，那么BeaEngine与capstone合适你；如果你还需要ARM构架支持的话，capstone应该会更适合你
