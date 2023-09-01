# 可执行文件

## 常见可执行文件格式

* 不同系统
  * 最早
    * `COFF`
      * =`Common Object File Format`
  * `Windows`
    * `PE`
      * =`Portable Executable`
  * `Linux`类系统：`Linux`、`Unix`、`Mac`等
    * [ELF](https://book.crifan.org/books/android_re_static_analysis/website/by_file_type/for_so/elf_format/)
      * =`Executable and Linkable Format`
  * `Mac`
    * [Mach-O](https://book.crifan.org/books/ios_re_static_analysis/website/analysis_content/bin_info/mach_o/)
* 其他相关
  * 二进制往往还根据系统不同而略有不同
    * 举例
      * Windows系统
        * `32位`=`x86`
        * `64位`=`x64`
