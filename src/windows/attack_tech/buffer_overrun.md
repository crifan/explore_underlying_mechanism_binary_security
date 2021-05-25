# 缓冲区溢出

* `缓冲区溢出`
  * 会导致
    * 覆盖了
      * 函数返回值
        * overwrite a function's return address
      * 异常处理地址
        * exception handler address
      * 某些类型的参数
        * certain types of parameters
  * 黑客
    * 会利用`缓冲区溢出`去对于
      * 没有强制实现缓存大小的限制的那些代码
    * 实现漏洞检测和攻击

缓冲区溢出代码举例：

```c
// compile with: /c /W1
#include <cstring>
#include <stdlib.h>
#pragma warning(disable : 4996)   // for strcpy use

// Vulnerable function
void vulnerable(const char *str) {
   char buffer[10];
   strcpy(buffer, str); // overrun buffer !!!

   // use a secure CRT function to help prevent buffer overruns
   // truncate string to fit a 10 byte buffer
   // strncpy_s(buffer, _countof(buffer), str, _TRUNCATE);
}

int main() {
   // declare buffer that is bigger than expected
   char large_buffer[] = "This string is longer than 10 characters!!";
   vulnerable(large_buffer);
}
```
