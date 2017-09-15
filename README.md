# Rqalpha-myquant-learning
对开源项目Rqalpha的改造，在应用上面更适合个人的应用。学习量化策略，对量化策略进行开发调试。

2017-09-15：更新内容（重要更新）

1.修改命名规则

2.增加爬虫程序，可以爬取所有场外基金的历史净值数据，用于之后的分析

2017-09-13：更新内容

增加了一个增加账户资金的函数，用于模拟周期增量资金定投的情况。

增加了rqalpha\strategy\investment.py策略，展示如何模拟增量资金定投的情况。

2017-09-08：更新至Rqalpha版本3.0.6

目前的改造情况：

1.增加ats.main.py，来驱动起回测，使程序可以使用pycharm进行开发调试

2.增加批量回测功能

3.在AlgoTradeConfig中进行配置回测的策略和所需要的参数信息，参数信息通过excel文件进行配置

4.在ats.main.py中设置参数为batch，运行回测，会将输出的.csv文件放在cvsResult目录下，将回测的图片保存在picResult目录下。

5.读取回测的.csv文件，提取账户信息，可以将不同参数回测的结果输出在同一张图片上，更加清晰的看清同一个策略，不同参数所带来的变化。

6.从广发信号站点获取历史交易信号（站点已停止，此处无法继续）

7.增加通用函数的封装，现阶段增加了对TA_LIB的调用封装（未完整完成）

8.增加了对增量资金定投的情况的模拟，用来模拟每月工资进行定投，研究资产储蓄的情况。

在notebook目录下包含学习所写的notebook信息：

程序部分学习：

1.rqalpha的get_bar函数中对bcolz数据进行获取部分的逐步展示

统计学知识学习：

1.python科学计算（平均数、众数、标准差等）

2.相关性学习

3.简单线性回归学习

4.多元线性回归

5.参数统计

学习目标：

1.增加量化策略的开发练习，现阶段主要以量化择时策略为主

2.优化批量回测功能，完善对不同策略回测结果的展示，增加最大回撤等信息的展示，增加对批量回测结果的统计，如交易次数

2.学习rqalpha的框架结构

3.增加对分钟级别K线的支持

4.增加图形界面化功能

策略开发：

将学习的一些策略的实现，分享在rqalpha/strategy目录下，现阶段所包含的策略如下

量化择时部分：

[ma20.py]：20日均线策略

[llt.py]：广发证券自适应移动平均线策略

[td.py]：广发证券TD策略

[rsrs.py]：基于阻力支撑相对强度（RSRS）的市场择时

[hurst.py]：hurst指数计算方法（需要增加择时的研究）

