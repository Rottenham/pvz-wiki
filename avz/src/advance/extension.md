<!--
 * @Coding: utf-8
 * @Author: vector-wlc
 * @Date: 2021-09-26 11:16:50
 * @Description: 
-->

# 插件

AvZ 无法满足所有使用者的需求，因此会有一些使用者编写一些实用的插件来丰富 AvZ 的内容。由于提供的 AvZ 包是只支持编译单文件的，因此如果插件有 `.cpp` 源文件编译无法通过，这时需要一定的多文件配置，这时需要编写者有一定的多文件配置基础，因为一些复杂的原因，笔者暂时不提供 AvZ 插件开发包。

当然有些读者想到既然不能写到源文件里面，那我可以直接把插件的代码写到头文件里面啊，这种想法确实可以实现，而且使用起来貌似非常方便，**但是这样的头文件不可以被多个源文件重复包含** ，否则会报标识符被重定义的错误，一般情况下头文件是放函数的声明和类的定义的。

这里还要说明的一点是，插件的文件一定不要修改 AvZ 本身的文件，因为这样 AvZ 一旦更新就会破坏插件的文件，这样会给用户带来非常困惑的问题。

AvZ 教程到此结束，感谢大家学习 AvZ。


[上一篇 变量内存管理](./memory_manage.md)

[目录](../catalogue.md)
