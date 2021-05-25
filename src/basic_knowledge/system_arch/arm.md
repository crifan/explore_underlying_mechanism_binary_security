# ARM 寄存器

* ARM寄存器和架构
  * 32位 arm
  * 64位 arm

## 32位arm的调用约定

| 寄存器 | 描述 |
| ----- | --- |
| r0-r3 |传递参数与返回值。如果断点在 OC 方法的第一行，那 r0 就是 self，r1 就是 cmd。如果超过四个参数，或者一些例如结构体的参数超过了32位 bit，那么参数将会通过栈来传递；返回值一般都在 r0 上 |
| r4-r6, r8, r10-r11 | 没有特殊规定，通用寄存器 |
| r7 | 栈帧指针寄存器(Frame Pointer)，指向前一个保存的栈帧(stack frame)和链接寄存器(link register， lr)在栈上的地址 |
| r9 | 操作系统保留 |
| r12 | IP 寄存器(intra-procedure scratch) |
| r13 | SP 寄存器(stack pointer)，是栈顶指针 |
| r14 | LR 寄存器(link register)，存放函数返回后需要继续执行的指令地址 |
| r15 | PC 寄存器(program counter)，指向当前指令地址 |
| CPSR | 当前程序状态寄存器(Current Program State Register)，在用户状态下存放像 condition 标志中断禁用等标志 |

## arm64的调用约定

arm64有 r0 - r30 是31个通用整形寄存器，PC 不能再作为寄存器直接访问。每个寄存器可以存取一个64位大小的数。 当使用 x0 - x30 访问时，它就是一个64位的数。当使用 w0 - w30 访问时，访问的是这些寄存器的低32位。

| 寄存器 | 描述 |
| ----- | --- |
| x0–x7 | 传递参数与返回值。如果参数个数超过了8个，多余的参数会存在栈上；返回值一般都在 x0 上 |
| x29 | 栈帧指针寄存器(Frame Pointer)，指向前一个保存的栈帧(stack frame)和链接寄存器(link register， lr)在栈上的地址 |
| x31 | SP 寄存器(stack pointer)，是栈顶指针；根据不同指令，也有可能是 zero register |
| x30 | LR 寄存器(link register)，存放函数的返回地址 |
| CPSR | 当前程序状态寄存器(Current Program State Register)，在用户状态下存放像 condition 标志中断禁用等标志 |
