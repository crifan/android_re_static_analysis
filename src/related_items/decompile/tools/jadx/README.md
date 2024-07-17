# jadx

* 概述
  * 从`apk`/`dex`直接一步转`java`的好用的反编译之一
  * 用法
    ```bash
    jadx -d output_folder apk_file.apk
    jadx -d output_folder dex_file.dex
    ```
    * 如果要开启反混淆，则是：
      ```bash
      jadx --deobf -d output_folder apk_file.apk
      ```
      * 注：
        * 好处：效果是，给普通的a、b、c、d等类名，改名，类似于C9830a等，方便查看和分析代码
        * 坏处：可能会导致无法hook
          * 如果后续（用Frida等）去hook，则反混淆后的类名，是无效的，丢失了原始的，混淆后的类名，导致无法正常（用Frida）去hook了
  * 主页
    * [skylot/jadx: Dex to Java decompiler](https://github.com/skylot/jadx)
* 详解
  * [安卓反编译利器：jadx](https://book.crifan.org/books/android_re_decompile_jadx/website/)
