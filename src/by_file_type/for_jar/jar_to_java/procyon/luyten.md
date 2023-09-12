# Luyten

* 主页
  * [deathmarine/Luyten: An Open Source Java Decompiler Gui for Procyon](https://github.com/deathmarine/Luyten)
* 功能
  * Java Decompiler Gui for Procyon
  * 基于Procyon的带图形界面的Java反编译器
* 界面
  * ![luyten_ui_demo](../../../../assets/img/luyten_ui_demo.png)
* 下载
  * [Release Luyten v0.5.4 · deathmarine/Luyten](https://github.com/deathmarine/Luyten/releases/latest)

## Luyten的语法高亮的不同主题的效果

* 默认：Default = Default-Alt
  * ![luyten_theme_default_alt](../../../../assets/img/luyten_theme_default_alt.png)
* Dark
  * ![luyten_theme_dark](../../../../assets/img/luyten_theme_dark.png)
* Eclipse
  * ![luyten_theme_eclipse](../../../../assets/img/luyten_theme_eclipse.png)
* Visual Studio
  * ![luyten_theme_visual_studio](../../../../assets/img/luyten_theme_visual_studio.png)
* IntelliJ
  * ![luyten_theme_intellij](../../../../assets/img/luyten_theme_intellij.png)

## 下载和使用Luyten去查看和导出java代码

去[Releases · deathmarine/Luyten](https://github.com/deathmarine/Luyten/releases/)下载最新版本，比如Mac版的：

[luyten-OSX-0.5.4.zip](https://github.com/deathmarine/Luyten/releases/download/v0.5.4/luyten-OSX-0.5.4.zip)

解压得到`Luyten.app`：

![luyten_app_uncompressed](../../../../assets/img/luyten_app_uncompressed.png)

运行后：

![luyten_app_main_ui](../../../../assets/img/luyten_app_main_ui.png)

然后去把`jar`包拖进来即可看到代码：

![luyten_drag_jar_into](../../../../assets/img/luyten_drag_jar_into.png)

导出所有代码的步骤：

`File -> Save All -> decompiled-xxx.zip`

![luyten_file_save_all_source_zip](../../../../assets/img/luyten_file_save_all_source_zip.png)

解压后，即可用VSCode等工具方便查看代码了。

之前`JD-GUI`、`CFR`等工具转换出错的代码，此处是可以正确解析的：

![luyten_convert_correct_code](../../../../assets/img/luyten_convert_correct_code.png)

但是也还是有部分代码无法正确解析：

![luyten_some_code_convert_failed](../../../../assets/img/luyten_some_code_convert_failed.png)
