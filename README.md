<div align=center><img width="300" height="180" src="./pic.jpg"/></div>

---

- [控制类](#控制类)
- [仪器仪表类](#仪器仪表类)
- [飞行器类](#飞行器类)
- [扩展知识](#扩展知识)
- [实验室项目团队的工作方式](#实验室项目团队的工作方式)
- [为什么采用这样的工作方式](#为什么采用这样的工作方式)
- [Todo Lists](#todo-lists)
---
# 控制类
- [C51贪吃蛇游戏机](https://github.com/ywg121020/51_sanke_game)
- [Raspiberry + picamera + opencv Toolbox](https://github.com/IyangDc/py_opencv_tools.git)
- [stm32 串口驱动集合](https://github.com/zgpTree/stm32_serial_driver.git)
- [StateMachine For C51](https://github.com/zgpTree/c51_state_machine.git)`推荐`
- [stm32f429](https://github.com/MaJerle/stm32f429)`官方`

# 仪器仪表类
- 

# 飞行器类
-

# 扩展知识
- [stm32 C++ cin cout对象实现项目](https://github.com/zgpTree/stm32_cppTest)

# 201-203项目团队的工作方式
1. 注册[GitHub](https://github.com/)帐号，并新建一个仓库Repo（下文称其为仓库X）；
2. 本地计算机安装[git](https://git-scm.com/downloads)软件，通过命令行在本地的项目根目录(例如stm32项目根目录)初始化仓库，并连接远程仓库X；
3. 将本地仓库推送至github端；
4. 克隆`刘老师`的仓库到本地，修改readme文件(加入仓库X的链接)，向刘老师提交修改申请(如果是建设者不需要可以直接修改)。
5. 如果你熟悉了这样的工作方式，你会做的更好；你要做的更好，就必须熟悉它。
6. 就像这样:
<div align=center><img width="800" height="350" src="./工作方式图解.png"/></div>

# 为什么采用这样的工作方式
- 刘老师希望实验室的软件项目有更优质的样例程序，有益于后来人学习；不至于每一届都重复造轮子，这不是否定造轮子。
- 这样的工作方式支持多人协同开发软件项目，团队意识可以受到培养，毕竟这是一种趋势，协同开发是软件工程师必须掌握的技能。
- 这培养我们软件开发要考虑维护的工作如何进行，如何更具有可读性，因为你的项目可能由后来人接手，谁都不愿意看到糟糕的程序。
- 这样的工作方式并不容易上手，但是上手后带来的效率不可小觑，正所谓磨刀不误打柴工。
- 给你笑脸 :smile:

# 详细说明
1. 需要的所有文件如图![](./picture/需要的文件.png)

    - Demo目录是项目根目录(你可以选择任何一个项目根目录)
    - [Git-*.exe](https://git-scm.com/downloads)是git安装程序
    - [VSCodeSetup-*.exe](https://git-scm.com/downloads)是Visual Studio Code，微软开源的编辑器，它支持插件预览github风格的markdown

2. 本地安装Git程序，一直点击next默认安装即可，安装完成后鼠标右击菜单如图
    <div align=center><img src="./picture/鼠标右击菜单.png"/></div>

3. github新建仓库如图
    <div align=center><img src="./picture/1-new repo.png"/></div>
    <div align=center><img src="./picture/2-new repo.png"/></div>
    实际上，github是非常友好的，它提示了Quick setup:
    <div align=center><img src="./picture/3-new repo.png"/></div>
4. 打开`Git Bash`
    <div align=center><img src="./picture/gitBash.png"/></div>
    改变工作目录到项目根目录
    <div align=center><img src="./picture/gitbashCommand.png"/></div>
    <div align=center><img src="./picture/gitbashCommand2.png"/></div>
    <div align=center><img src="./picture/gitbashCommand3.png"/></div>
    <div align=center><img src="./picture/gitbashCommand4.png"/></div>
    <div align=center><img src="./picture/gitbashCommand4.png"/></div>
5. 安装VSCode
# Todo Lists
- [x] 基本完成工作方式说明
- [ ] 定制.gitignore文件，可以参考[stm32f429](https://github.com/MaJerle/stm32f429)。为什么需要这个文件，它可以告知git过滤一些不需要的文件(如可执行文件、临时对象文件...)，也就减轻了版本控制系统git的工作的负担，这是有意义的！
