# GeekRGB-Firmware for Keychron V1

![Q1](https://i.imgur.com/syr9jmw.jpeg)

# 固件更新 2022-12-26
* 增加对mac系统部分快捷键支持
* 增加Geek RGB内核成 2.1.1，支持，启动特效
* 添加键盘15分钟后自动关闭灯效
* 添加一键切换 Geek RGB 自定义按键，FN+Mute (非旋钮版本，可以在VIA改建)
* 旋钮版本，优化VIA配置

# 固件特性（更新时间：2022-12-15）
* 更新 signalRGB 插件
* 更新 GeekRGB v2.1
* 更新部分内置灯效
* 支持 mac 和 windows 键层切换
* 支持旋钮版本和非旋钮的ANSI版本（不支持ATmega32版本键盘）
* 仅支持 OpenRGB

## 固件文件
旋钮版本固件: [keychron_v1_ansi_stm32l432_ec11_geekrgb.bin](https://github.com/puterjam/GeekRGB-Firmware/raw/main/keyboards/keychron/V1/keychron_v1_ansi_stm32l432_ec11_geekrgb.bin)

非旋钮版本: [keychron_v1_ansi_stm32l432_geekrgb.bin](https://github.com/puterjam/GeekRGB-Firmware/raw/main/keyboards/keychron/V1/keychron_v1_ansi_stm32l432_geekrgb.bin)

## 刷固件
### 1. 安装固件工具
下载 QMK 键盘刷固件工具 qmk_toolbox

下载地址：https://github.com/qmk/qmk_toolbox/releases

第一次启动，会安装对应的键盘驱动，耐心等待即可


### 2. 进入键盘 bootloader 模式
拔掉USB线 - 长按 ESC 键（不松开）- 插上USB线 即进入键盘的 bootloader 模式。

`第一次刷固件，需长按空格下的reset按钮`


### 3. 刷写固件
下载固件文件，拖拽到 qmk toolbox 的输入框, 点击 Flash 即可


# openRGB 使用
第一次使用，需要在OpenRGB软件中添加键盘

打开 `设置 - OpenRGB QMK 协议` 添加键盘

> 名称：任意
>
> USB VID：`3434` USB PID：`0311`

保存 - 重新搜索设备

非滚轮版本 PID 为 `0311`