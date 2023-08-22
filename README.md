# Lenovo-Yoga-14S-4800U-hackintosh

Lenovo Yoga14s 4800U macOS `Ventura`版本的 EFI 文件

![Image](https://cdn.jsdelivr.net/gh/koyangyang/Lenovo-Yoga-14S-2020ARE-hackintosh@main/images/system13.4.png)

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
|3.5mm 声音h|✔|
|3.5mm 麦克风|✔|
|扬声器和内置麦克风|✔|
|睡眠|❌|


## 安装步骤

### 1. 修改 BIOS 

关闭`bios`中的 `快速启动`和`安全启动`

修改显存为 `2G - 4G`（`2G`以上显存需要解锁高级`BIOS`）

(`2G`够用。。。)

解锁高级`BIOS`参考[这篇文章](https://zhuanlan.zhihu.com/p/184982689)

### 2. 生成 PI 信息

用 [OC auxiliary tools 工具](https://github.com/ic005k/OCAuxiliaryTools) 打开 `config.plist`

`PI` -> 在 `SystemProductName` 后面点击生成，生成自己的机器码

`PI` -> 在 `ROM `后面点击生成

保存

### 3. 引导安装

重启笔记本按 F12 选择 U 盘引导即可。

### 4. 修复内置麦克风

安装完毕后，

1. 下载[hackintool](https://github.com/benbaker76/Hackintool/releases)工具
2. 将`AMDMicrophone.kext`放入`Library\Extensions`文件夹中
3. 打开`hackintool-工具`中重建缓存

![Image](https://cdn.jsdelivr.net/gh/koyangyang/Lenovo-Yoga-14S-2020ARE-hackintosh@main/images/hackintool.png)

4. 在弹出`设置-隐私与安全`中允许安装`AMDMicrophone`，重新启动即可

## 存在问题
1. 此 EFI 可能一开始无法使用触摸板！！！但是重启几次即可恢复。

2. 睡眠问题尚未修复
   
3. 硬件等待`Nootedred`修复

4. 在无人为干扰情况下cpu温度维持在70+,手动调整频率后可以降至50-70。

如果你能解决以上问题，欢迎提交 PR 到这个 repo，也可以联系我，一起探讨该技术问题。
