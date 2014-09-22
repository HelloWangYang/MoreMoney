MoreMoney
=========

Personal Finance Application

Java编写的个人记账软件。个人业余时间开发，参考到一些开源的项目，尽量做到简单实用。欢迎 find bug and pull request，希望能跟大家多多交流，共同进步！

##1.设计思路

用户界面获取用户的操作，系统处理后存入`.csv`文件。`csv`文件仅存放基础数据，其他的例如生成表格、饼图和导出等等由程序处理，而非直接保存。(P.S.这些统计数据本人是想用`R`来实现，顺便练练手，嗯)

##2.用户界面

用户界面使用`Swing`开发，初步提供以下几个操作：
* 日期：默认由系统提供当前时间，格式为`年-月-日`，也可以由用户修改。
* 类别：早餐、午餐、晚餐，还是超市购物等等，实现同地点。
* 地点：实现一个下拉列表，提供常去的餐厅等等，可以添加或者删除其中的选项。
* 金额：手动输入，注意是浮点数且小数点后保留两位。
* 备注：手动输入，例如今天有充值，或者发工资啦 b(^o^)d
* 保存时间：界面上显示，用于保存编辑时间，用户不可修改。

##3.数据格式

数据文件为csv，格式如下：
```csv
日期,类别,地点,金额,备注,保存时间
```

##4.模块设计

排除例如获取当前目录权限的操作，目前系统大致分为以下3个模块：
* 文件操作
* 界面数据输入
* 数据处理

##5.参考的开源项目

* [jGnash](http://sourceforge.net/projects/jgnash/)
* [YouMoney](https://code.google.com/p/youmoney/)
* [GnuCash](http://www.gnucash.org/)