# Lenovo-Yoga-14S-4800U-hackintosh

Lenovo Yoga14s 4800U macOS `monterey`版本的 EFI 文件

|硬件 | 状态|
|----|-----|
|CPU: AMD 4800 U| ✔ |
|内存 板载内存| ✔ |
|显卡 核显 Vega 8| ✔ |
|网卡 ax 200 | ✔ |
|硬盘 梵想S500Pro 512G | ✔ |


|功能 | 状态|
|----|-----|
|键盘|✔|
|触摸板|✔|
|WIFI|✔|
|核显|✔|
|蓝牙|❌|
|睡眠|❌|
|USB接口|✔|


## 安装步骤

### 1. 解锁 BIOS 高级菜单

关闭`bios`中的 快速启动 安全启动

修改显存为 `1G - 4G`

### 2. 生成 PI 信息

用 [OC auxiliary tools 工具](https://github.com/ic005k/OCAuxiliaryTools) 打开 config.plist

PI -> 在 SystemProductName 后面点击生成，生成自己的机器码

PI -> 在 ROM 后面点击生成

保存

## 参考项目
本项目教程主要参考下面项目，仅更换为`Monterey`的EFI

[whitescent/Lenovo-Yoga-14S-4800U-hackintosh](https://github.com/whitescent/Lenovo-Yoga-14S-4800U-hackintosh)