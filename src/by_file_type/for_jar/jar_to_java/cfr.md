# CFR

* `CFR`=`Class File Reader`
  * 官网
    * CFR - yet another java decompiler
      * http://www.benf.org/other/cfr/
  * 特点
    * 支持java 9/10/12等（中的Java的新特性）
  * 下载
    * 从[官网]( http://www.benf.org/other/cfr/)下载
      * `cfr-0.152.jar`
        * https://www.benf.org/other/cfr/cfr-0.152.jar

## 用法

* 命令
  * 反编译jar文件
    * 输出到终端
      ```bash
      java -jar cfr.jar <compiled.jar>
      ```
    * 输出到文件夹
      ```bash
      java -jar cfr.jar <compiled.jar> --outputdir <dir>
      ```
  * 反编译单个class文件
    ```bash
    java -jar cfr.jar <someClassFile.class
    ```
* 说明
  * 只支持输入格式是：`.jar`
    * 不支持：`.dex`、`.apk`
