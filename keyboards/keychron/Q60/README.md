# GeekRGB-Firmware for Keychron Q60 (HHKB like)

![Q60](https://i.imgur.com/4Eqjq6z.jpeg)

# 固件更新 2025-11-2
* 充分利用 6 个Layer 的功能区
* 支持Mac 的 Globe 键
* 支持 Win，Mac 模式切换
* Control + FN + B 可以切换 Delete 和 Backspace 键（仿HHKB模式）
* FN + ESC，切换固定数字键区成F1-F12功能区
* 功能开关灯效，Caps Lock 和 Layer 层切换
* 支持 GeekRGB + OpenRGB
* 默认 HHKB like 键位


## 固件文件
Q60 ANSI 版本: [keychron_q60_q60_ansi_stm32l432_geekrgb.bin](https://github.com/puterjam/GeekRGB-Firmware/raw/main/keyboards/keychron/Q6/keychron_q60_q60_ansi_stm32l432_geekrgb.bin)

> 注意，不支持 Q60 Max 三模版本

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
> USB VID：`3434` USB PID：`01C0`

保存 - 重新搜索设备