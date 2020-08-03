<div align=center><img width="300" height="180" src="./picture/pic.jpg"/></div>

------------------------------------------------------

- [控制类](#控制类)
- [仪器仪表类](#仪器仪表类)
- [飞行器类](#飞行器类)
- [基础知识](#基础知识)
- [扩展知识](#扩展知识)
- [非电赛或个人项目](#非电赛比赛或个人项目添加)
- [201-203项目团队的工作方式](#201-203项目团队的工作方式)
    - [为什么采用这样的工作方式](#为什么采用这样的工作方式)
- [推荐阅读](#推荐阅读)
- [Todo Lists](#todo-lists)
- [附录](#附录)

---
# 控制类

- [C51贪吃蛇游戏机](https://github.com/ywg121020/51_sanke_game)`推荐` **林佳涛**
- [stm32f429](https://github.com/MaJerle/stm32f429)`官方`
    - HC-SR04超声波测量距离(超声波传感器)
    - GPS - Read GPS data
    - ...
- [无刷电机练习]()**`等待添加`**
    - 期望实现正弦运动,并能够设定中心位置的高度
    - 建议使用超声波传感器+测距平台
    - ...
- [风力摆控制系统解析及源码][1] **网上大佬**
- [帆板控制系统]()**`等待添加`**
- [寻迹程序]()**`等待添加`**
- **赵博文的奇幻游乐场**
    - [Raspiberry + picamera + opencv Toolbox](https://github.com/IyangDc/py_opencv_tools)
    - [板球控制系统](https://github.com/IyangDc/Board-ball_control_system)
    - [电光灯环](https://github.com/IyangDc/Point_Ring)

# 仪器仪表类
需要自己额外找资料学习，多制作PCB板实践，学习电路设计，练习焊工及摸索排版技巧  
熟悉各芯片用途及用法，看的懂相应datasheet
- [锁相环][4]
- [AGC][5]
- [调制解调][6] [检波][7] [相敏检波][8]
- [滤波器][9]
- 更多电路设计  **`等待添加`**
- 相关AD原理图及PCB **`等待添加`**
# 飞行器类
<<<<<<< HEAD
-
=======
- 
# AI人工智能
  - [jetson NANO 折腾记](https://github.com/mti05001/Electronic-Design-Contest/blob/master/AI/jetson/jetsonNano/jetson%20nano%20%E6%8A%98%E8%85%BE%E8%AE%B0.md)



# 基础知识
- [51单片机C语言程序100例](https://github.com/qianxinbubian/51source) **李明华**
    - 新来的同学或者又想用51单片机做项目再或者有人需要一些模块源代码的可以看一看
# 扩展知识
- [STM32CubeMX][2] `官方`
    - STM32图形化配置。`基本熟悉STM32配置后使用 ！`
    - 其他相关使用等资料请百度  :sunglasses:


# 201-203项目团队的工作方式
## 以`帆板控制系统`项目为例说明
1. 申请github，或gitee（码云）账号，
    学习基本的git知识及操作(初次使用git的同学，先到推荐下自己找一些学习的资料)
2. 用自己的账户，在网页上建立`帆板控制系统`项目的仓库，clone到本地，
    添加相应文件后推送到远程仓库（方法不唯一，这样比较方便）
3. clone[`刘燕娜的仓库`][3]到本地计算机，把`帆板控制系统`仓库的链接写入到README.md文件，
    向刘老师提交修改申请（若是建设者可以直接修改，可以找刘老师要权限；或提交issue，由管理员修改）
4. 工作方式图解:
<div align=center><img width="750" height="380" src="./picture/工作方式图解.png"/></div>

## 为什么采用这样的工作方式
- 实验室的软件项目需要优秀的样例程序，这有益于后来人学习，不至于每一届都重复造轮子。
- 支持多人协同开发软件项目，利于培养良好的团队意识，协同开发是软件工作者必须掌握的技能。
- 这培养我们软件开发要考虑维护的工作如何进行，如何更具有可读性，
    因为你的项目可能由后来人接手，谁都不愿意看到糟糕的程序。
- 这不容易上手，但磨刀不误打柴工。
- 如果有兴趣参加实验室的Git队伍，请查看[Git.md](./readme/Git.md)
- :smile:

# Todo Lists
- [x] 完成工作方式说明
- [ ] 定制.gitignore文件，可以参考[stm32f429][5]。
    这个文件可以告知git过滤文件(如可执行文件、临时对象文件...)，
    也就减轻了版本控制系统git的工作的负担！

# 推荐
- [优秀项目或个人](./readme/Extension.md) :star:
---
# 附录
## 相关资料已放百度云群，包括各模块资料，电子书籍

***加群方式 —— 找刘老师***

## 其他

- 可以将一些好的项目添加进来，共同学习提高 :heart:
- github(gitee)是个好东西 :sunny:
- 维护者
<<<<<<< HEAD
    - 赵国潘 陈鹏昀
    - 李明华
      -
<div align=center><img width="320" height="240" src="./picture/we want you.jpg"/></div>

[1]: http://bbs.eeworld.com.cn/forum.php?mod=viewthread&tid=476344&extra=page%3D1&page=1
[2]: http://www.st.com/content/st_com/zh/products/development-tools/software-development-tools/stm32-software-development-tools/stm32-configurators-and-code-generators/stm32cubemx.html
[3]: https://github.com/mti05001/Electronic-Design-Contest
[4]:https://baike.baidu.com/item/%E9%94%81%E7%9B%B8%E7%8E%AF/4213?fr=aladdin
[5]:https://baike.baidu.com/item/agc/15278295
[6]: https://baike.baidu.com/item/%E8%B0%83%E5%88%B6%E8%A7%A3%E8%B0%83
[7]: https://baike.baidu.com/item/%E6%A3%80%E6%B3%A2/1049132?fr=aladdin
[8]: https://baike.baidu.com/item/%E7%9B%B8%E6%95%8F%E6%A3%80%E6%B3%A2
[9]: https://baike.baidu.com/item/%E6%BB%A4%E6%B3%A2%E5%99%A8/2551370?fr=aladdin
=======
    - 创始人： [赵国潘](https://gitee.com/ZhaoGuoPan) [陈鹏昀](https://github.com/ChenPY95) 
    - [李明华](https://github.com/qianxinbubian)
    - 
<div align=center><img width="500" height="350" src="./picture/we want you.jpg"/></div>
>>>>>>> 9b3956598d5a9370e704e0ab81f15b9098f98889
