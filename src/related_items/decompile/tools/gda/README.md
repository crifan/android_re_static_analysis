# GDA

* `GDA`=`GJoy Dex Analysizer`=GDA反编译器
  * 主页
    * GDA主页-亚洲首款交互式Android反编译器
      * http://www.gda.wiki:9090/

  * 简介
    * GDA是一款由本人对反编译理论的长期研究和实践而形成的全交互式反编译器，世界上唯一一款用c++写的android-java反编译器，中国第一款也是唯一一款全交互式反编译器。其简洁、轻便、快速，无需安装，也无需java和android sdk环境支持。支持apk、dex、odex、oat、jar、aar、class文件的反编译分析，GDA中包含多个由本人独立研究的高速分析引擎: 反编译引擎、漏洞检测引擎、恶意行为检测引擎、污点传播分析引擎、反混淆引擎、apk壳检测引擎等。
    * 在Android可执行文件反编译分析上，GDA摆脱了使用java速度慢的问题，完全采用C++完成核心反编译引擎的编写，并且使用了字节码直接转java伪代码的解析方式，无需转换成smali汇编后在做反编译，大大提升了解析速度。
    * 此外，在反编译引擎的基础上，我做了一些更加实用的功能，如路径求解、 漏洞检测、隐私泄露检测、查壳、odex转dex、oat转dex、加解密算法工具、android设备内存dump等等功能，在交互式分析上，提供了( multi-dex的跨dex的 )字符串、方法、类和域交叉引用查询、调用者查询、搜索功能、注释功能、分析结果保存等等功能。
  * 功能
    * 一款强大而轻便的交互式反编译器，也是一款综合性逆向分析利器
      * 支持分析`apk`, `dex`, `odex`, `oat`, `jar`, `class`, `aar`类型文件
      * 支持python脚本以及方法签名制作与识别
    * 工具包含三个由作者独立完成的高速解析引擎
      * 反编译引擎
      * apk壳检测引擎
      * 恶意行为检测引擎
    * 再加上作者独创的使用了字节码直接转java伪代码的解析方式
      * 无需转换成smali汇编后再做反编译
        * 大大提升了解析速度
  * 特点
    * 无需安装java环境和android环境就可以使用
      * 不是依赖其他的（很多安卓反汇编的、java的）库
    * 分析速度快、体积小、内存占用少
  * 特性
    * c++编写,独立于java和android sdk，无需安装java和android sdk即可使用
    * 有效绕过各种字节码陷阱、类型混淆以及anti-disassembling和anti-decompiling技术
    * 支持dex、odex、apk、oat、jar、class、aar文件的反编译分析
    * 支持multi-dex反编译
    * 支持对strings,class,method,field进行交叉引用和搜索(模糊匹配、精确匹配、正则)
    * 支持class、method、field及变量重命名，java代码注释
    * 分析结果保存，odex、oat转dex
    * 设备内存dump,可用于辅助脱壳
    * 反混淆支持
    * 针对字符串、方法、类、域等关键信息提供了强大的搜索、交叉引用
    * 算法工具提供主流大部分算法，可进行加密和解密
    * Python和Java自动化插件支持
    * 方法签名支持
    * 基于API链的恶意行为识别
    * 变量及寄存器追踪与溯源分析
    * 漏洞扫描，自定义漏洞规则
    * 隐私泄露检测
    * 精细化的程序路径求解
    * APK取证分析
  * 截图
    * ![gda_main_ui](../../../../assets/img/gda_main_ui.jpg)
    * ![gda_ui_pro](../../../../assets/img/gda_ui_pro.jpg)
    * ![gda_ui_1](../../../../assets/img/gda_ui_1.png)
    * ![gda_ui_2](../../../../assets/img/gda_ui_2.png)
    * ![gda_ui_3](../../../../assets/img/gda_ui_3.jpg)
    * ![gda_ui_4](../../../../assets/img/gda_ui_4.gif)
    * ![gda_ui_5](../../../../assets/img/gda_ui_5.gif)
  * 快速上手
    * [原创]GDA：国产反编译器快速上手指南-Android安全-看雪-安全社区|安全招聘|kanxue.com
      * https://bbs.pediy.com/thread-220111.htm
  * 下载
    * [GDA下载 最新版](http://www.gda.wiki:9090/down.php)
  * GDA vs JEB
    * ![gda_vs_jeb](../../../../assets/img/gda_vs_jeb.png)
