# 固件更新 2022-12-26
* 增加对mac系统部分快捷键支持
* 增加Geek RGB内核成 2.1.1，支持，启动特效
* 添加键盘15分钟后自动关闭灯效
* 添加一键切换 Geek RGB 自定义按键，FN+Tab
 
# 固件更新 2022-12-15
* 更新 GeekRGB v2.1，完美解决 VIA 和 软件灯效冲突的问题
* 解决 OpenRGB 和 SignalRGB 的冲突
* 更新 SignalRGB 插件
* 还原官方默认内置灯效
* 还原官方出厂按键配置
* 更新VIA的配置文件
* 修复 待机状态没有关闭rgb的问题

## 固件文件
[melgeek_tegic_rev1_geekrgb.hex](https://raw.githubusercontent.com/puterjam/GeekRGB-Firmware/main/keyboards/melgeek/tegic/melgeek_tegic_rev1_geekrgb.hex)
（可右键保存链接）

## 刷固件
### 1载 QMK 键盘刷固件工具 qmk_toolbox

下载地址：https://github.com/qmk/qmk_toolbox/releases

第一次启动，会安装对应的键盘驱动，耐心等待即可


### 2. 进入键盘 bootloader 模式
拔掉USB线 - 长按 ESC 键（不松开）- 插上USB线 即进入键盘的 bootloader 模式。


### 3. 刷写固件
下载固件文件，拖拽到 qmk toolbox 的输入框, 点击 Flash 即可

# openRGB 使用
## 1. 下载 GeekRGB 兼容的 OpenRGB 软件
[下载地址](https://github.com/puterjam/GeekRGB-Firmware/tree/main/software)


## 2. 添加键盘
第一次使用，需要在OpenRGB软件中添加键盘

打开 `设置 - OpenRGB QMK 协议` 添加键盘

> 名称：任意
>
> USB VID：`EDED` USB PID：`0081`

保存 - 重新搜索设备


# signalRGB 使用
把 Tegic 的 SignalRGB 插件，复制到 ```%userprofile%/Documents/WhirlwindFX/``` 的plugins目录中

![Tegic](https://i.imgur.com/WVxnvmX.png)
