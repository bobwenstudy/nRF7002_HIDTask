# 概述

本项目是[Digikey Funpack (eetree.cn)](https://www.eetree.cn/page/digikey-funpack)活动的任务一实现。

SDK基于**2.4.2**版本实现，环境是nRF Connect SDK。

硬件板子是项目提供的**nRF7002DK**。

使用的时候会出现一直找不到板子，需要调整vscode设置。

![image-20230915101905995](https://markdown-1306347444.cos.ap-shanghai.myqcloud.com/img/image-20230915101905995.png)



# 编码步骤

## 使用blinky例程测试板子功能OK

确保编译环境和硬件环境是OK的，并且为了减少去了解板子的DeviceTree的时间。

![image-20230915195901564](https://markdown-1306347444.cos.ap-shanghai.myqcloud.com/img/image-20230915195901564.png)

## 创建HIDS_Keyboard例程

需要将HIDS里面的代码复制到blinky项目代码中，也就是替换main.c和prj.conf。nrf的东西不要，都拿掉。

将keypad和led换成任务所需的。

**注意**：这个例程不直接支持nRF7002DK，所以我们主要是拿里面的代码到blinky中。

![image-20230915195939038](https://markdown-1306347444.cos.ap-shanghai.myqcloud.com/img/image-20230915195939038.png)

## 创建HIDS_Mouse例程

前一个工作将report map和hid service改好，可以到这里再拿一些mouse实现的代码。

![image-20230915200214220](https://markdown-1306347444.cos.ap-shanghai.myqcloud.com/img/image-20230915200214220.png)





# 一些基本信息

## 确认build target

[Features of nRF70 Series — nRF Connect SDK 2.4.99 documentation (nordicsemi.com)](https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/device_guides/working_with_nrf/nrf70/features.html#supported-boards)

  

  ![image-20230914214913852](https://markdown-1306347444.cos.ap-shanghai.myqcloud.com/img/image-20230914214913852.png)





## nRF Connect SDK上手

[Welcome to the nRF Connect SDK! — nRF Connect SDK 2.4.99 documentation (nordicsemi.com)](https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/index.html)

建议用其集成开发环境。自动集成到VSCode中。

[Installing automatically — nRF Connect SDK 2.4.99 documentation (nordicsemi.com)](https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/installation/assistant.html)



## nRF7002 DK上手说明

[Getting started with nRF70 Series — nRF Connect SDK 2.4.99 documentation (nordicsemi.com)](https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/device_guides/working_with_nrf/nrf70/gs.html)



## Bluetooth的Sample

[Bluetooth samples — nRF Connect SDK 2.4.99 documentation (nordicsemi.com)](https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/samples/bl.html)





![image-20230914215530933](https://markdown-1306347444.cos.ap-shanghai.myqcloud.com/img/image-20230914215530933.png)



