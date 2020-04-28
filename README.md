# 黑苹果OpenCore配置从入门到放弃
> 记录一下安装macOS Catalina过程

## 硬件配置

|硬件|配置|
| :---: | --- |
| CPU | Intel 9600kf |
| 主板 | 技嘉z390 Gaming x |
| GPU | RX 580 |
| SSD | 三星 SM951 256G|

## 目录结构

```
.      
├── BIOS                               // CFG Lock解锁相关
├── EFI                                // EFI 文件
├── TOOLS                              // 相关工具软件
└── README.md
```

## 安装macOS

### 用到的工具

1. Macbook pro
我是mac环境下安装的，windows用户可能仅作参考了；

2. U盘 * 3
制作macOS安装盘;
制作shell启动盘;
PE以备不时之需;

### 制作macOS安装盘

> 主要参考[tonymacx86](https://www.tonymacx86.com/threads/unibeast-install-macos-catalina-on-any-supported-intel-based-pc.285366/)的安装教程

大致步骤如下:
1. App Store下载Catalina
    1.1 使用一下mac设备或者另一台hackintosh

    * MacBook (Early 2015 or newer)​
    * MacBook Air (Mid 2012 or newer)​
    * MacBook Pro (Mid 2012 or newer)​
    * Mac mini (Late 2012 or newer)​
    * iMac (Late 2012 or newer)​
    * iMac Pro (2017)​
    * Mac Pro (Late 2013 model or newer)​

    1.2 打开App Store
    1.3 登录Apple ID
    1.4 搜索并下载下载macOS Catalina

2. 使用UniBeast制作macOS Catalina安装盘

    2.1. 安装盘尽量使用USB2.0 U盘，我也不知道为什么我用3.0就不行
    2.2. 格式化U盘
    2.3. 打开UniBeast，将Catalina安装到U盘；软件在`/TOOLS`目录下，或者到[tonymacx86](https://www.tonymacx86.com/resources/categories/tonymacx86-downloads.3/)下载相应版本；

### 安装macOS

#### BIOS设置
首先将主板BIOS所有配置回复默认

1. tonymacx86的通用BIOS配置如下

    * VT-d -> Disable
    * CFG-Lock -> Disable
    * Secure Boot Mode -> Disable
    * IO Serial Port -> Disable
    * XHCI Handoff -> Enabled
    * OS Type -> Other OS

2. 技嘉z390 Gaming x BIOS配置
> 主要抄自

