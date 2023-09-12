# dex2jar

* `dex2jar`
  * 功能
    * 用于处理`安卓`的`.dex`文件和`java`的`.class`文件的一系列的工具
      * 核心和常用功能
        * 从`dex`文件导出`jar`文件
      * 一系列的工具，包括
        * `dex-reader/writer`: 读写`dex`（Dalvik Executable）文件
          * 具有和`ASM`类似的轻量级的API接口
        * `d2j-dex2jar`: 把`dex`文件转换为`class`文件（=jar压缩包文件=`jar`包=`jar`文件）
        * `smali/baksmali`: 反汇编`dex`转换出`smali`文件, `从smali`文件中汇编出`dex`文件
          * 和[smali/baksmali](https://github.com/JesusFreke/smali)虽然语法相同，但不太一样的是，此处支持描述中包含`"Lcom/dex2jar\t\u1234;"`这类文字描述
        * 其他一些工具
          * [d2j-decrypt-string](https://sourceforge.net/p/dex2jar/wiki/DecryptStrings)
  * 资料
    * 官网
      * [dex2jar | Penetration Testing Tools](https://tools.kali.org/reverse-engineering/dex2jar)
    * 其他主页/镜像
      * github
        * [pxb1988/dex2jar: Tools to work with android .dex and java .class files](https://github.com/pxb1988/dex2jar)
      * SourceForge
        * https://sourceforge.net/p/dex2jar

## 下载dex2jar

* 从[dex2jar的下载页面](https://github.com/pxb1988/dex2jar/releases)下载到最新版本的`dex2jar`
  * 比如：[dex-tools-2.1-SNAPSHOT.zip](https://github.com/pxb1988/dex2jar/files/1867564/dex-tools-2.1-SNAPSHOT.zip)
    * 解压后得到：`d2j-dex2jar.sh`

## 使用

* 概述
  ```bash
  d2j-dex2jar.sh -f apk_file.apk
  d2j-dex2jar.sh -f dex_file.dex
  ```
  * 举例
    ```bash
    sh dex-tools/dex-tools-2.1-SNAPSHOT/d2j-dex2jar.sh -f com.huili.readingclub3986968.dex
    ```
