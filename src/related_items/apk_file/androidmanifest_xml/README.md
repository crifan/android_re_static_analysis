# AndroidManifest.xml

安卓的`apk`中有个`AndroidManifest.xml`文件，是保存了相关项目的类，资源等配置信息。

而对于安卓的`apk`文件：

* （由于本身就是个zip压缩包文件，所以）直接改名为`zip`后再解压即可得到的（加了密的）**二进制**格式的`AndroidManifest.xml`文件
* 用`apktool`等工具去反编译：得到的是**文本**格式的`AndroidManifest.xml`文件
  * 就可以看到xml的原始内容了
    * 注：即使`apk`加固了，也可以用`apktool`反编译

### AndroidManifest.xml的作用

得到了xml源码后，可以从其中看到很多有用的信息。

比如， 小花生安卓版 v3.6.9的`apk`，apktool反编译出的`AndroidManifest.xml`中包含：

```xml
<activity android:name="com.huili.readingclub.activity.classroom.SelfReadingActivity" android:screenOrientation="portrait"/>
...
<activity android:name="com.huili.readingclub.activity.classroom.ParentChildReadingActivity" android:screenOrientation="portrait"/>
```

其中的类名：

* `activity.classroom.SelfReadingActivity`
* `activity.classroom.ParentChildReadingActivity`

=类的文件名，对应了app界面：

![androidmanifest_xml_contain_app_class](../../../assets/img/androidmanifest_xml_contain_app_class.png)

中的：

* 自主阅读馆
* 亲子阅读馆

-》从而有利于后续分析内部的业务逻辑，了解到内部有哪些类和功能。
