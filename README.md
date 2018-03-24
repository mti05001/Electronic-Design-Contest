<div align=center><img width="300" height="180" src="./picture/pic.jpg"/></div>

---

- [控制类](#控制类)
- [仪器仪表类](#仪器仪表类)
- [飞行器类](#飞行器类)
- [扩展知识](#扩展知识)
- [201-203项目团队的工作方式](#201-203项目团队的工作方式)
    - [为什么采用这样的工作方式](#为什么采用这样的工作方式)
- [Todo Lists](#todo-lists)

---
# 控制类
- [Arduino PID库(基于C++)](https://github.com/br3ttb/Arduino-PID-Library) 详见 **[官方介绍](http://playground.arduino.cc/Code/PIDLibrary)** :star:
    - [倒立摆](http://www.arduino.cn/forum.php?mod=viewthread&tid=3826&highlight=%E5%80%92%E7%AB%8B%E6%91%86)
- [stm32f429](https://github.com/MaJerle/stm32f429)`官方`:star:
    - [HC-SR04超声波测量距离](https://github.com/MaJerle/stm32f429/blob/master/00-STM32F429_LIBRARIES/tm_stm32f4_hcsr04.c)
    - GPS - Read GPS data
- [风力摆控制系统解析及源码](http://bbs.eeworld.com.cn/forum.php?mod=viewthread&tid=476344&extra=page%3D1&page=1) :star:
- [无刷电机练习]()**`等待添加`**
    - 期望实现正弦运动,并能够设定中心位置的高度
    - 建议使用超声波传感器+测距平台
- [帆板控制系统]()**`等待添加`**
- [寻迹程序]()**`等待添加`**
- [C51贪吃蛇游戏机](https://github.com/ywg121020/51_sanke_game) :star: **林佳涛**
- [StateMachine(状态机) For C51](https://github.com/zgpTree/c51_state_machine.git):star: **赵国潘**
- [stm32 串口驱动集合](https://github.com/zgpTree/stm32_serial_driver.git) **赵国潘**
    - 我通过配置stm32f103每一个串口的驱动了解了很多知识，但是部分没完成。
- [Raspiberry + picamera + opencv Toolbox](https://github.com/IyangDc/py_opencv_tools.git) **赵博文**
- [2017电赛B题-板球控制系统](https://github.com/xiaohongxiao/ball_rolling_control_system) :star: **鲁乾鹏**  



# 仪器仪表类
- [2017 调幅信号处理实验电路（F题）分析](https://wenku.baidu.com/view/7764e55d854769eae009581b6bd97f192379bf58.html) 

# 飞行器类
- 

# 扩展知识
- 如果受够了硬件初始化配置，学习[STM32CubeMX](http://www.st.com/content/st_com/zh/products/development-tools/software-development-tools/stm32-software-development-tools/stm32-configurators-and-code-generators/stm32cubemx.html)将给你带来好处。
- [stm32使用C++ cout对象](https://github.com/zgpTree/stm32_cppTest) **赵国潘**
    - 大三时想使用C++丰富的语言特性在单片机中编程，如果你感兴趣，请移步[stm32plus](https://github.com/andysworkshop/stm32plus)
- [网络爬虫](https://baike.baidu.com/item/%E7%BD%91%E7%BB%9C%E7%88%AC%E8%99%AB)   **陈鹏昀**
    - 利用网络爬虫技术获取互联网上公开的数据，加以存储分析。有兴趣可以深入[数据挖掘](https://baike.baidu.com/item/%E6%95%B0%E6%8D%AE%E6%8C%96%E6%8E%98)，[数据分析](https://baike.baidu.com/item/%E6%95%B0%E6%8D%AE%E5%88%86%E6%9E%90)
    - 可以使用python内置urllib，re等模块，或第三方request，BeautifulSoup模块（需要pip下载），或使用开源爬虫架构如[Scrapy](https://baike.baidu.com/item/scrapy)（[官方文档](https://doc.scrapy.org/en/latest/intro/overview.html)），方法多样
    - 使用爬虫程序时要注意对爬虫进行伪装，以免某些需要认证的网站识别出这是爬虫程序，从而报错。可以模仿浏览器，使用Cookie等。很多网站有[robots协议](https://baike.baidu.com/item/robots%E5%8D%8F%E8%AE%AE)（类似于公交车上的老弱病残专座），不必严格遵守，但也要遵守道德，避免过度频繁的爬取，以免对对方服务器造成不便
    - [pythonLearning](https://gitee.com/ChenPY95/pythonLearning) 

# 201-203项目团队的工作方式
## 以`C51 状态机`项目为例说明
1. 在本地计算机建立`C51 状态机`项目的仓库，与github的仓库连接，推送到github端；
1. fork[`刘燕娜的仓库`](https://github.com/mti05001/Electronic-Design-Contest)到本地计算机，加入`C51 状态机`仓库的链接到README.md文件，向刘老师提交修改申请；(若是建设者可以直接修改)
1. 工作方式图解，请参考[详细说明](#详细说明):
<div align=center><img width="750" height="380" src="./picture/工作方式图解.png"/></div>

## 为什么采用这样的工作方式
- 实验室的软件项目需要优秀的样例程序，这有益于后来人学习；不至于每一届都重复造轮子。
- 支持多人协同开发软件项目，利于培养良好的团队意识，协同开发是软件工作者必须掌握的技能。
- 这培养我们软件开发要考虑维护的工作如何进行，如何更具有可读性，因为你的项目可能由后来人接手，谁都不愿意看到糟糕的程序。
- 这不容易上手，但磨刀不误打柴工。

## 推荐阅读
- [廖雪峰Git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001373962845513aefd77a99f4145f0a2c7a7ca057e7570000)
- [GitHub Markdown](https://guides.github.com/features/mastering-markdown/)


# Todo Lists
- [x] 完成工作方式说明
- [ ] 定制.gitignore文件，可以参考[stm32f429](https://github.com/MaJerle/stm32f429)。这个文件可以告知git过滤文件(如可执行文件、临时对象文件...)，也就减轻了版本控制系统git的工作的负担！
- [ ] 完成详细说明

---
<!--# 附录>
