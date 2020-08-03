# jetson nano 之 Hello AI World

[toc]

## 简介

这里我们直接从配置Jetson-Inference项目的环境开始。首先，Jetson-Inference的github项目链接：https://github.com/dusty-nv/jetson-inference (访问慢或有问题的可以直接在当前目录获取哟！！！)。该文章较整理笔者的学习与错误。

## 硬件配置

运行本项目，需要用到的配件：

- Jetson nano Developer Kit
- Wireless-AC 8265无线网卡（你也可以选择其他网络连接方式）
- IMX219-77 Camera  (这个就是树莓派v2摄像头)    (或者其他CSI摄像头）
- 5V 4A DC电源
- HDMI 屏幕     (或者你也可以远程连接)

## 安装

- 软件上需要 `cmake` ,  `python3` ,  `numpy` ，安装如下：(其中 `cmake` 请参考之前文章)

```bash
sudo apt-get update
sudo apt-get install libpython3-dev python3-numpy
```

- 正式安装：

```bash
cd ~/
git clone https://github.com/dusty-nv/jetson-inference
cd jetson-inference
git submodule update --init    
sudo mkdir build
cd build
sudo cmake ../     //如果出现提示键盘右键Quit，国内下载不下来，权重文件可在本站下载
make
sudo make install
```

- 权重文件的导入：

解压后直接放在 `build/aarch64/bin/network` 目录下

## 使用

请参考官方教程