# 探究底层机制：二进制安全

* 最新版本：`v0.8`
* 更新时间：`20210525`

## 简介

整理二进制安全，即PWN；先对二进制安全概述；再介绍相关基础知识，比如编程语言，包括汇编语言X86、ARM等；体系架构的寄存器X86、ARM和堆栈，以及可执行文件；再总结Windows相关的二进制安全，包括安全机制的ASLR、CFG、DEP、GS、SafeSEH、SEHOP，和攻击技术，包括缓冲区溢出、ROP、Heap spray、Shellcode等；再整理二进制相关工具，包括反汇编器的disassembler，反编译器的dnSpy、ILSpy，静态安全检工具的winchecksec，可执行文件工具的Exeinfo PE，查壳工具的Detect It Easy、PEiD，逆向工具的IDA、Ollydbg、WinDbg，内存修改工具的CE、MHS、ModifyMemory；最后附上参考资料。

## 源码+浏览+下载

本书的各种源码、在线浏览地址、多种格式文件下载如下：

### Gitbook源码

* [crifan/explore_underlying_mechanism_binary_security: 探究底层机制：二进制安全](https://github.com/crifan/explore_underlying_mechanism_binary_security)

#### 如何使用此Gitbook源码去生成发布为电子书

详见：[crifan/gitbook_template: demo how to use crifan gitbook template and demo](https://github.com/crifan/gitbook_template)

### 在线浏览

* [探究底层机制：二进制安全 book.crifan.com](http://book.crifan.com/books/explore_underlying_mechanism_binary_security/website)
* [探究底层机制：二进制安全 crifan.github.io](https://crifan.github.io/explore_underlying_mechanism_binary_security/website)

### 离线下载阅读

* [探究底层机制：二进制安全 PDF](http://book.crifan.com/books/explore_underlying_mechanism_binary_security/pdf/explore_underlying_mechanism_binary_security.pdf)
* [探究底层机制：二进制安全 ePub](http://book.crifan.com/books/explore_underlying_mechanism_binary_security/epub/explore_underlying_mechanism_binary_security.epub)
* [探究底层机制：二进制安全 Mobi](http://book.crifan.com/books/explore_underlying_mechanism_binary_security/mobi/explore_underlying_mechanism_binary_security.mobi)

## 版权说明

此电子书教程的全部内容，如无特别说明，均为本人原创和整理。其中部分内容参考自网络，均已备注了出处。如有发现侵犯您版权，请通过邮箱联系我 `admin 艾特 crifan.com`，我会尽快删除。谢谢合作。

## 鸣谢

感谢我的老婆**陈雪**的包容理解和悉心照料，才使得我`crifan`有更多精力去专注技术专研和整理归纳出这些电子书和技术教程，特此鸣谢。

## 更多其他电子书

本人`crifan`还写了其他`100+`本电子书教程，感兴趣可移步至：

[crifan/crifan_ebook_readme: Crifan的电子书的使用说明](https://github.com/crifan/crifan_ebook_readme)
