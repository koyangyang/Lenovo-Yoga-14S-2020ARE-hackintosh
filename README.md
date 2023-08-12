# Lenovo-Yoga-14S-4800U-hackintosh

Lenovo Yoga14s 4800U macOS `monterey`版本的 EFI 文件
![Image](https://cdn.jsdelivr.net/gh/koyangyang/Lenovo-Yoga-14S-2020ARE-hackintosh@main/images/system.png)

> [!Important]
> Yoga14s 原装  `海力士硬盘` 无法安装 MacOS系统，自行更换。

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
|扬声器|✔|
|触摸板|✔|
|WIFI|✔|
|核显|✔|
|蓝牙|✔|
|全USB|✔|
|3.5mm 声音|✔|
|睡眠|❌|
|3.5mm 麦克风|❌|


## 安装步骤

### 1. 解锁 BIOS 高级菜单

关闭`bios`中的 快速启动 安全启动

修改显存为 `2G - 4G`（`2G`以上显存需要解锁高级`BIOS`）

解锁高级`BIOS`参考[这篇文章](https://zhuanlan.zhihu.com/p/184982689)

### 2. 生成 PI 信息

用 [OC auxiliary tools 工具](https://github.com/ic005k/OCAuxiliaryTools) 打开 config.plist

PI -> 在 SystemProductName 后面点击生成，生成自己的机器码

PI -> 在 ROM 后面点击生成

保存

### 3. 引导安装

重启笔记本按 F12 选择 U 盘引导即可。

## 参考项目
本项目安装过程主要参考下面项目，仅更换为`Monterey`的EFI

> [!Important]
> 经过修复，已经无需禁用XHCI，修复蓝牙连接和第二个USB口

[whitescent/Lenovo-Yoga-14S-4800U-hackintosh](https://github.com/whitescent/Lenovo-Yoga-14S-4800U-hackintosh)

## 存在问题
1. 此 EFI 可能一开始无法使用触摸板！！！但是重启几次好像会莫名其妙好，问题原因应该是在定制USB过程中存在某些问题，等待修复。

2. 睡眠问题尚未修复

3. 自带3.5mm耳机孔，声音正常，麦克风失效。可以通过蓝牙暂时替代

如果你能解决以上问题，欢迎提交 PR 到这个 repo，也可以联系我，一起探讨该技术问题。
