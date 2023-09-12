# JD-GUI

* 主页
  * [Java Decompiler](http://java-decompiler.github.io)
* JD Project=Java Decompiler Project
  * `JD-Core`
    * 是什么：`一个库`
    * 功能：从一个或多个.class文件中重构java源代码
    * 用途：
      * 可用于恢复丢失的源代码
      * 可用于查看jar包的java源码=查看JRE（Java运行时）库的源码
    * 特点：
      * java 5中最新的功能
        * 注释annotations
        * generics 或 枚举类
    * 说明：
      * JD-GUI内置包含了JD-Core
      * JD-Eclipse内置包含了JD-Core
  * `JD-GUI`
    * 是什么：一个独立的带图形界面的`程序`
    * 作用：显示查看jar包的java源代码
      * 注：`jar包`=内部包含了很多`.class`文件的，被压缩打包成`jar`
    * 举例
      * ![java_decompiler_jd_gui_demo](../../../assets/img/java_decompiler_jd_gui_demo.png)
    * github主页
      * [java-decompiler/jd-gui: A standalone Java Decompiler GUI](https://github.com/java-decompiler/jd-gui)
    * 下载
      * http://java-decompiler.github.io
      * -》
      * [Releases · java-decompiler/jd-gui](https://github.com/java-decompiler/jd-gui/releases)
      * -》
      * 比如：
        * `Mac`：
          * [jd-gui-osx-1.4.1.tar](https://github.com/java-decompiler/jd-gui/releases/download/v1.4.1/jd-gui-osx-1.4.1.tar)
  * 插件
    * JD-Eclipse：Eclipse的插件
      * 举例：
        * ![jd_eclipse_plugin](../../../assets/img/jd_eclipse_plugin.png)
    * JD-IntelliJ：IntelliJ IDEA的插件
      * 举例：
        * ![jd_intellij_idea_plugin](../../../assets/img/jd_intellij_idea_plugin.png)

## JD-GUI反编译jar的效果

### 举例

用`JD-GUI`打开jar文件，即反编译jar文件，`com.ishowedu.child.peiyin9201516-dex2jar.jar`，得到java代码的效果：

![jd_gui_open_app_logic_jar](../../../assets/img/jd_gui_open_app_logic_jar.png)

其中找到了我们之前需要的app相关的业务逻辑的代码：

`/com/huili/readingclub/activity/classroom/SelfReadingActivity.class`

![include_app_logic_selfreadingactivity_code](../../../assets/img/include_app_logic_selfreadingactivity_code.png)

其中`onSuccess`中就是我们希望得到的对于`J`字段解密的逻辑。

### 其他无效的jar转换出jar的效果

如前一步所述，从多个`dex`可以转换出多个`jar`

而这些无效的、没有包含app业务逻辑的`jar`，去用一些反编译工具打开后的效果是：

![jd_gui_open_jar_android](../../../assets/img/jd_gui_open_jar_android.png)

其他的一些，比如腾讯乐固加密了的，最终转换出来的jar，去打开后只能看到腾讯乐固的代码：

![jd_gui_jar_show_tencent_legu](../../../assets/img/jd_gui_jar_show_tencent_legu.png)
