# GeekRGB Firmware

让QMK客制化键盘，在游戏场景上，给游戏玩家获得更好的沉浸灯效联动体验

> For Gamer，Become Geeker

固件基于QMK官方源码进行了二次开发

## 如何让自己的键盘使用 GeekRGB 固件

### 1. 使用已支持的键盘固件（推荐）
目前支持GeekRGB的键盘列表

* [keyChron V1](keyboards/keychron/V1/) 
* [keyChron Q1](keyboards/keychron/Q1/)
* [Tegic 框架主义](keyboards/melgeek/tegic/)

在 [keyboards](keyboards) 目录中，找到对应的键盘固件下载

### 2. 编译 GeekRGB 固件，支持新键盘
```diff
- 刷固件过程，请勿断开USB线。因人为操作失误等，请自行承担
```

1. 下载 QMK MSYS https://msys.qmk.fm/

2. 启动 QMK MSYS，在命令行中创建一个目录。输入命令 
```Bash
mkdir geekRGB
```

3. 进入目录。输入命令
 ```Bash
cd geekRGB
```

4. 克隆GeekRGB源码 
```Bash
git clone https://github.com/puterjam/qmk_firmware.git
```

5. 进入 qmk_firmare 目录，准备qmk的编译环境
 ```Bash
 cd qmk_firmware
 make git-submodule
 ```

6. 打开 qmk 的键盘目录 `%userprofile%\geekRGB\qmk_firmware\keyboards` 找到你的键盘型号

7. 找到键盘的 `rules.mk` 文件，在键盘根目录，或者 `KEYMAP` 目录的 `rules.mk` 文件都可以

8. 打开 `rules.mk` 文件，添加两项参数
```
OPENRGB_ENABLE = yes
SIGNALRGB_SUPPORT_ENABLE = yes
```
9. 编译键盘固件
```Bash
make KEYBOARDBRAND/KEYBOARD:KEYMAP
```

```diff
+ 最后，欢迎有动手能力的小伙伴，可以分享您编译好的固件
```

### 3. GeekRGB Firmware 固件源码
https://github.com/puterjam/qmk_firmware

### 4. GeekRGB Firmware 更新历史
#### v2.1.1
* GeekRGB特效支持键盘开机动画

#### v2.1(preview)
* 增加 HIDRGB USB 协议，彻底解决VIA 和 软件灯效冲突的问题 （重要更新）
* 优化 OpenRGB 设置灯效的兼容性
* 优化 OpenRGB 可以读取非默认键位的配置
* 还原 VIA 协议代码，方便后面更新 v3 版本

#### v2
* 成功整合 via/SignalRGB/openRGB，支持和其他设备灯效联动
* 扩展 via.c 接口，支持在不同使用场景下切换协议
* 支持独立按键灯效配置，支持社区灯效，音乐联动，游戏场景联动
* 支持全局亮度同步，方便通过键盘调整亮度
* 提升了VIA和SignalRGB的兼容性，可同时使用

#### v1
* v1.2 修复 SignalRGB 键盘插件，Tegic键盘最后一排按键灯效不亮的问题
* v1.1 本固件第一个版本，支持 via + SignalRGB —— 来自装备前线

## 开源
最后感谢，[QMK](https://qmk.fm/zh-cn/)，[OpenRGB](https://gitlab.com/CalcProgrammer1/OpenRGB)，[QMK-OpenRGB](https://github.com/Kasper24/QMK-OpenRGB)，[VIA](https://github.com/the-via)，[SignalRGB](https://gitlab.com/signalrgb/qmk_firmware)，[Zhaqian](https://github.com/zhaqian12) 等众多开源项目，与贡献者
