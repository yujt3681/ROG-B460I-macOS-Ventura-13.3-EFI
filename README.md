# ROG-B460I-macOS-Ventura-13.3-EFI
黑苹果华硕ROG B460I macOS Ventura 13.3 EFI引导文件


## OpenCore & Kext

`OpenCore-0.9.1`

| Kext名称 | 版本号 | 作用  |
| --- | --- | --- |
| Lilu.kext | V1.6.5 | 核心扩展，黑苹果必须 |
| VirtualSMC.kext | V1.3.2 | 模拟系统 SMC 及提供一些传感器插件 |
| WhateverGreen.kext | V1.6.5 | 显卡补丁集，驱动核显必备 |
| SMCProcessor.kext | V1.3.2 | 用于监控 cpu 温度 |
| SMCSuperIO.kext | V1.3.2 | 用于监控散热器速度 |
| AppleALC.kext | V1.8.1 | 驱动 ALC 芯片声卡 |
| IntelBTPatcher.kext | V2.2.0 | 修复蓝牙4.0和5.0设备连接问题 |
| IntelMausi.kext | V1.0.8 | 驱动英特尔板载有线以太网卡 |
| USBInjectAll.kext | V0.78 | 定制USB驱动 |
| IntelBluetoothFirmware.kext | V2.3.0 | 驱动英特尔蓝牙 |
| BlueToolFixup.kext | V2.6.5 | 英特尔蓝牙需要此驱动 |
| AirportItlwm.kext | V2.2.0 | 驱动英特尔板载无线网卡 |

## 配置

| 项目  | 配置  |
| --- | --- |
| CPU | 英特尔 Core i5-10500 @ 3.10GHz 六核 |
| 主板  | 华硕 ROG STRIX B460-I GAMING |
| 内存  | 金士顿 8G DDR4 2400 x 2 |
| 显卡  | 无独立显卡 |
| 核显  | Intel®UHD Graphics 630 |
| 无线网卡 | Intel® Wi-Fi 6 AX200 160MHz（主板集成） |
| 网卡  | Intel® Ethernet  I219-V（主板集成） |
| 蓝牙  | Intel® Bluetooth® （主板集成） |
| 声卡  | 瑞昱 High Definition Audio @ 英特尔（主板集成） |
| 主硬盘 | Lexar 512GB SSD |
| 次硬盘 | Fanxiang S100PRO 512GB ( 512 GB / 固态硬盘 ) |

##

## 涉及软件

```
1. OpenCore 0.9.1以上版本
```

## 优点

1. 精简了很多的东西，保留主要的kext。无线网卡、核显可以驱动，macOS可以直接升级到13.3.1，升级后进入系统慢点。
2. 该EFI是基于“黑果小兵的macOS Ventura 13.3双引导分区原本镜像”里的EFI修改而来，他对OC引导界面做了美化。
3. 可以安装WIN10老机型GHO版实现双系统，我按照后OC界面多了win10操作系统，可以正常启用使用。
4. 设置机型为iMac20.1。
5. 可以休眠启动。
6. 支持USB3.0。

## 缺点

1. USB端口基本可以使用，所以 USB没有自己定制
2. 蓝牙有问题：军刀工具没有看到蓝牙设备；蓝牙可以发现连接手机；蓝牙可以发现蓝牙键盘和鼠标，但无法建立连接。
