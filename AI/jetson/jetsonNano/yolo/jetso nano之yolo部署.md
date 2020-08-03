# jetso nano 之 yolo 部署

[toc]

## 1. 框架选择

务必选择正确的框架，由于使用 jetson nano(armv8框架，使用jetpack4.4系统)，支持tkDNN框架：

https://github.com/ceccocats/tkDNN

## 2. 软件版本

官方给出版本：

+ CUDA 10.0
+ CUDNN 7.603
+ TENSORRT 6.01
+ OPENCV 3.4
+ yaml-cpp 0.5.2 (sudo apt install libyaml-cpp-dev)

实际使用版本(经验证通过)：

+ CUDA 10.2.89
+ CUDNN 8.0.0.180
+ TENSORRT 7.1.3.0
+ OPENCV 4.1.1
+ yaml-cpp 0.5.2 (sudo apt install libyaml-cpp-dev)

该使用版本为 `jetpack` 自带版本，版本可通过 `jtop` 查看

## 3. opencv版本选择

官方给出版本为`3.4`，实际使用中可以应用`4.x`版本，(目前 `jetpack4.4` 自带 `opencv4.x` )，但要 **注意** 注释 `tkDNN/include/tkDNN/DetectionNN.h` 中 `#define OPENCV_CUDACONTRIB` 

## 4. 编译安装

**注** ：该编译过程需要用到 `cmake` ，若使用 `opencv4.x` ，需要最新版本 `cmake` ，( `cmake > 3.15` )  

```bash
cd tkDNN
mkdir build
cd build
// cmake .. -DDEBUG=True          //if you want debug
cmake ..
make
```

## 5. 导入权重

权重对于任何网络进行推理都是必不可少的。对于每个测试，需要一个按如下方式组织的文件夹（在build文件夹中）

```
test_nn
        |---- layers/ (folder containing a binary file for each layer with the corresponding wieghts and bias)
        |---- debug/  (folder containing a binary file for each layer with the corresponding outputs)

```

(待续。。。。。)

## 6. 测试

这是使用 `yolov4-tiny` 的示例。

要运行对象检测，请首先通过运行以下命令创建 `.rt` 文件：

```bash
rm yolo4_fp32.rt        # be sure to delete(or move) old tensorRT files
./test_yolo4            # run the yolo test (is slow)
```

如果您在创建过程中遇到问题，请尝试通过以下方式检查激活TensorRT调试的错误：

```bash
cmake .. -DDEBUG=True
make
```

成功创建rt文件后，运行演示：

```bash
./demo yolo4_fp32.rt ../demo/yolo_test.mp4 y
```

通常，演示程序采用6个参数：

```bash
./demo <network-rt-file> <path-to-video> <kind-of-network> <number-of-classes> <n-batches> <show-flag>
```

+ `<network-rt-file>` 是测试生成的rt文件
+ `<<path-to-video>` 是视频文件或摄像机输入的路径
+ `<kind-of-network>`是网络的类型。当前支持这些类型：`y`（YOLO系列），（CenterNet `c`系列）和`m`（MobileNet-SSD系列）
+ `<number-of-classes>`网络接受培训的课程数
+ `<n-batches>` 用于推理的批次数（注意，首先应将TKDNN_BATCHSIZE导出到所需的n_batches，然后再次为网络创建rt文件）。
+ `<show-flag>` 如果设置为0，则演示将不显示可视化效果，而是将视频保存到result.mp4中（如果n个批处理== 1）

默认情况下用于FP32推理

## 7. 训练自己的数据集

(待续。。。。)



## 错误锦集

### 1. cmake 编译错误

请检查 `cmake` 版本，`cmake >= 3.15` 

如果 `opencv = 4.x` ，请使用最新版

### 2. make 错误

请检查对应版本，目前测试通过版本为

+ CUDA 10.2
+ CUDNN 8.0.0
+ TENSORRT 7.1
+ OPENCV 4.1.1
+ yaml-cpp 0.5.2 

官方支持版本：

+ CUDA 10.1
+ CUDNN 7.x
+ TENSORRT 6.x
+ OPENCV 4.1.1 ( 3.4.0 )
+ yaml-cpp 0.5.2 (sudo apt install libyaml-cpp-dev)

**注：** CUDA 和 CUDNN 版本要对应

### 3. 测试错误

- 如果出现下载慢或出错，请尝试其他渠道下载权重文件，并注释 `tkDNN/tests/darknet/yolo4tiny.cpp` 中

```c++
 downloadWeightsifDoNotExist(input_bins[0], bin_path, "https://cloud.hipert.unimore.it/s/iRnc4pSqmx78gJs/download");
```

- 如果出现

```
could not parse line: 
/home/lingblopdreame/jupyter/tkDNN/src/DarknetParser.cpp:246
Aborting...
```

请修改 `tkDNN/src/DarknetParser.cpp:246` 

```c++
} else {
	continue;
	FatalError("could not parse line: " + line);
}
```

- 如果出现

```
activation not supported: leaky
/home/lingblopdreame/jupyter/tkDNN/src/DarknetParser.cpp:180
Aborting...
```

请修改 `tkDNN/src/DarknetParser.cpp:177:178:179` 

```c++
if(f.activation != "relu") act = tkdnnActivationMode_t(CUDNN_ACTIVATION_RELU);
            else if(f.activation != "leaky") act = tk::dnn::ACTIVATION_LEAKY;
            else if(f.activation != "mish") act = tk::dnn::ACTIVATION_MISH;
```







