# radare2

* 简称：`r2`
* 主页
  * Github
    * [radare/radare2: unix-like reverse engineering framework and commandline tools](https://github.com/radare/radare2)
  * 官网
    * [radare](https://rada.re/)
* 功能和特点
  * 一个开源的逆向工程和二进制分析框架
  * 功能非常强大
    * 反汇编、分析数据、打补丁、比较数据、搜索、替换、虚拟化等等
    * 强大的静态或动态分析、十六进制编辑以及溢出漏洞挖掘
    * 具备超强的脚本加载能力
  * 可以运行在几乎所有主流的平台
    * GNU/Linux, Windows, *BSD, iOS, OSX, Solaris
* 组成
  * 由一系列的组件构成
    * `rahash2`：各种密码算法，`hash算法`
    * `rabin2`：查看文件格式
    * `ragg2`/`ragg2­cc`：用于更方便的生成`shellcode`
    * `rax2`：用于数值转换
    * `rasm2`：反汇编和汇编
    * `radiff2`：对文件进行`diff`
    * => `radare2`：整合了上面的工具
  * 额外还有很多**插件**=`Plugins`
    * `esilsolve`: The symbolic execution plugin, based on esil and z3
    * `r2diaphora`: Diaphora's diffing engine working on top of radare2
    * `iaito`: The official Qt graphical interface
    * `radius2`: A fast symbolic execution engine based on boolector and esil
    * `r2dec`: A decompiler based on r2 written in JS, accessed with the pdd command
    * `r2ghidra`: The native ghidra decompiler plugin, accessed with the pdg command
    * `r2frida`: The frida io plugin. Start r2 with r2 frida://0 to use it
    * `r2poke`: Integration with GNU/Poke for extended binary parsing capabilities
    * `r2pipe`: Script radare2 from any programming language
    * `r2papi`: High level api on top of r2pipe
* 典型用途
  * 参加CTF
  * 逆向工程
  * 漏洞挖掘
  * 分析恶意软件（如溯源）
