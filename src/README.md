# Android逆向：静态分析

* 最新版本：`v1.2.0`
* 更新时间：`20240725`

## 简介

介绍安卓逆向之静态分析。包括先是概览；然后是相关子项，包括apk文件，以及其中的AndroidMenifest.xml，以及反编译，包括反编译的典型流程，以及如何从apk破解出java源码；常见反编译工具，包括jad、JEB、GDA等；以及常见的二进制编辑器，比如010editor、EverEdit等；接着是综合类工具，包括AndroidKiller、Android-Crack-Tool For Mac、ByteCode Viewer、Android Decompiler、decompile-apk、Android逆向助手、Androguard等；接着是按层级去介绍安卓静态分析所涉及的内容；以及再按文件格式去分相关内容；包括针对apk的，查看apk信息的aapt、APK Analyzer、ClassyShark等，apk解包的apktool，apk转java的jadx、JEB、GDA等；针对dex的，如何砸壳导出dex文件，包括判断哪家加固方案，砸壳工具FDex2以及如何用FDex2砸壳导出dex、DumpDex、DexExtractor、drizzleDumper、InDroid、DexHunter、FART等；接着是反编译dex，包括dex转jar、dex转smali、dex转java等。其中dex转jar包括dex2jar以及用法、Enjarify、Dedexer，dex转smali包括baksmali、dex转java包括jadx、GDA；针对jar的，jar转java，包括各种java反编译器的对比，以及常用的java反编译器，包括Procyon/Luyten、CFR、JD-GUI、Krakatau、Fernflower、Dare、JAD等；针对so的，ELF文件格式，以及如何从ELF的so导出静态资源供分析，常用工具有readelf、objdump、razbin2；以及如何反编译查看代码逻辑，常用工具有IDA、Hopper、radare2、Ghidra等；以及涉及到的子领域，包括反代码混淆，以及相关系列的子教程。

## 源码+浏览+下载

本书的各种源码、在线浏览地址、多种格式文件下载如下：

### HonKit源码

* [crifan/android_re_static_analysis: Android逆向：静态分析](https://github.com/crifan/android_re_static_analysis)

#### 如何使用此HonKit源码去生成发布为电子书

详见：[crifan/honkit_template: demo how to use crifan honkit template and demo](https://github.com/crifan/honkit_template)

### 在线浏览

* [Android逆向：静态分析 book.crifan.org](https://book.crifan.org/books/android_re_static_analysis/website/)
* [Android逆向：静态分析 crifan.github.io](https://crifan.github.io/android_re_static_analysis/website/)

### 离线下载阅读

* [Android逆向：静态分析 PDF](https://book.crifan.org/books/android_re_static_analysis/pdf/android_re_static_analysis.pdf)
* [Android逆向：静态分析 ePub](https://book.crifan.org/books/android_re_static_analysis/epub/android_re_static_analysis.epub)
* [Android逆向：静态分析 Mobi](https://book.crifan.org/books/android_re_static_analysis/mobi/android_re_static_analysis.mobi)

## 版权和用途说明

此电子书教程的全部内容，如无特别说明，均为本人原创。其中部分内容参考自网络，均已备注了出处。如发现有侵权，请通过邮箱联系我 `admin 艾特 crifan.com`，我会尽快删除。谢谢合作。

各种技术类教程，仅作为学习和研究使用。请勿用于任何非法用途。如有非法用途，均与本人无关。

## 鸣谢

感谢我的老婆**陈雪**的包容理解和悉心照料，才使得我`crifan`有更多精力去专注技术专研和整理归纳出这些电子书和技术教程，特此鸣谢。

## 其他

### 作者的其他电子书

本人`crifan`还写了其他`150+`本电子书教程，感兴趣可移步至：

[crifan/crifan_ebook_readme: Crifan的电子书的使用说明](https://github.com/crifan/crifan_ebook_readme)

### 关于作者

关于作者更多介绍，详见：

[关于CrifanLi李茂 – 在路上](https://www.crifan.org/about/)
