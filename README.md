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
|右侧第二个 USB 接口|❌|

> [!NOTE]
> 因为本机型需要禁用 XHCI 1 口才能正常进入安装系统，所以无法使用蓝牙、右侧第二个 USB 口。


## 安装步骤

### 1. 解锁 BIOS 高级菜单

首先，请先解锁 14s 的 BIOS 高级菜单，具体请参考[这篇文章](https://zhuanlan.zhihu.com/p/184982689)

修改显存为 `1G - 4G`

### 2. 生成 PI 信息

用 [OC auxiliary tools 工具](https://github.com/ic005k/OCAuxiliaryTools) 打开 config.plist

PI -> 在 SystemProductName 后面点击生成，生成自己的机器码

PI -> 在 ROM 后面点击生成

保存

### 3. 禁用 XHCI

重启笔记本，按住 F2 进入 BIOS，AMD CBS -> FCH Common Options -> USB Configuration Options.

将 XHCI1 Controller enable 从 Auto 改成 Dissabled.

保存，之后重启按 F12 选择 U 盘引导即可。

## 参考项目
本项目教程主要参考下面项目，仅更换为·、`Monterey`的EFI
[whitescent/Lenovo-Yoga-14S-4800U-hackintosh](https://github.com/whitescent/Lenovo-Yoga-14S-4800U-hackintosh)