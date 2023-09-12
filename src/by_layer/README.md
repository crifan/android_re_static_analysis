# 按层级分

* 按层级分
  * Java 层
    * 主要是dex文件
    * Dex文件
      * 先要有(未加壳的)dex
        * 如果apk加壳：要先砸壳
          * 壳的类型：360加固保，腾讯乐固等
          * 砸壳工具：FDex2等
          * 得到：脱壳后的dex =未加壳的dex
        * 如果未加壳：Apk解压直接得到 未加壳的dex
          * apktool即可解压和反编译
            * 内部从解压apk得到dex
      * 继续处理：(未加壳的)dex
        * 反编译
          * Dex to java
            * 工具：jadx, JEB, GDA等
          * 先Dex to jar 再jar to Java
            * Dex to jar
              * 工具：dex2jar等
            * Jar to Java
              * 各种java反编译器
  * Native层
    * 主要是so库文件
      * （安卓中的）so文件主要是ELF格式
        * 查看ELF文件的信息
          * 工具：readelf、objdump、rabin2等
      * 反编译so库文件
        * 主要是ARM汇编）查看代码逻辑
          * 反汇编工具：IDA、Hopper、radare2、Ghidra等
