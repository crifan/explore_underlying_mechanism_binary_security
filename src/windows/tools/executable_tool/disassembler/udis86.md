# udis86

* `udis86`
  * 是什么：X86架构的反汇编工具
    * `反汇编工具`=`反汇编器`=`反汇编框架`
  * 一句话描述：Udis86 is an easy-to-use, minimalistic disassembler library (libudis86) for the x86 class of instruction set architectures. It has a convenient interface for use in the analysis and instrumentation of binary code.
  * 概述
    * Udis86 is a disassembler for the x86 and x86-64 class of instruction set architectures. It consists of a C library called libudis86 which provides a clean and simple interface to decode a stream of raw binary data, and to inspect the disassembled instructions in a structured manner.
    * udis86支持的X86扩展指令集有：MMX, FPU (x87), AMD 3DNow, SSE, SSE2, SSE3, SSSE3, SSE4.1, SSE4.2, AES, AMD-V, INTEL-VMX, SMX
    * Udis86提供了一套反汇编的第三方库，用户可自行编写代码进行扩展。udcli是基于Udis86的反汇编工具，集成在Udis86项目里，通过命令行可快速实现反汇编
  * 主页
    * GitHub
      * https://github.com/vmt/udis86

