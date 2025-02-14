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
    * 最常用参数
      ```bash
      jadx --show-bad-code --comments-level debug -d outputFolder yourAndroidApp.apk
      ```
      * 说明
        * 不加上`--deobf`=不开启反混淆：是为了后续用[Frida](https://crifan.github.io/reverse_debug_frida/website/)去hook类和函数名时，可以看到（被混淆后的）**原始的变量名**
          * 而如果开启反混淆，导致类和变量名变了后：就不方便查看原始名称，不方便Frida去hook了
  * 主页
    * [skylot/jadx: Dex to Java decompiler](https://github.com/skylot/jadx)
* 详解
  * [安卓反编译利器：jadx](https://book.crifan.org/books/android_re_decompile_jadx/website/)
    * [jadx基本用法 · 安卓反编译利器：jadx](https://book.crifan.org/books/android_re_decompile_jadx/website/jadx_basic_usage/)
