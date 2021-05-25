# winchecksec

* `winchecksec`
  * 作用：Windows静态安全检测工具
  * 支持检测如下`安全特性`
    * `ASLR`
      * `/DYNAMICBASE` with stripped relocation entries edge-case
      * `/HIGHENTROPYVA` for 64-bit systems
    * `Code integrity/signing:`
      * `/INTEGRITYCHECK`
      * Authenticode-signed with a valid (trusted, active) certificate (currently unsupported on Linux)
    * `DEP`
      * 别称：`W^X`, `NX`
    * `Manifest isolation`
      * `/ALLOWISOLATION`
    * `SEH`和`SafeEH`
      * `SEH`=`Structured Exception Handling`
    * `Control Flow Guard`和`Return Flow Guard instrumentation`
    * `Stack cookie`
      * `/GS`
  * 资料
    * Github
      * trailofbits/winchecksec: Checksec, but for Windows: static detection of security mitigations in executables
        * https://github.com/trailofbits/winchecksec
