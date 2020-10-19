# 注意
2020年10月20日00:00:16
由于换了台式装黑苹果加上固态太小，这个笔记本就不再装黑苹果了，所以这个仓库以后就不再更新了。
系统最后版本 10.15
有兴趣可以看我的新项目 b85d3v+4590+rx560

# Asus ZX50J
具体安装流程请百度了解
这里只放了下载地址和详细说明
华硕zx50jx4200 黑苹果EFI配置 可适用于macos 10.15
注：本仓库仅供极客玩家测试使用，请勿用于任何商业行为!!!
## 配置：

CPU：Intel i5-4200h

内存：8G 

显卡：Intel HD 4600 + GTX950M(已屏蔽）

外存：120G M.2 SSD 

网卡/蓝牙：无线网卡蓝牙更换为 DW1560 M.2接口

### 原装网卡驱动WiFi

删除Clover/kexts/others下面四个驱动
```
AirportBrcmFixup.kext 
FakePCIID_Broadcom_WiFi.kext 
BrcmFirmwareData.kext
BrcmPatchRAM3.kext 
```
原装网卡驱动教程[地址](http://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1829501&highlight=AR9565)

DW1820A 驱动教程[地址](https://blog.daliansky.net/DW1820A_BCM94350ZAE-driver-inserts-the-correct-posture.html)

## 目前bug 
```
1.fn+F1会导致睡死 （请勿尝试!）

2.clover启动设置1080P分辨率开机画面闪现15苹果花屏 (Clover引导无此情况，oc引导需要bios开启CSM模式解决问题）

3.无法使用pppoe拨号 未测试

4.HDMI视频正常，音频无法正常输出

5.其他未知bug

2019年10月16日重新提取dsdt、ssdt
```
```
音频输入需要用工具修复

变频正常

屏幕亮度调解正常

键盘灯正常  

睡眠唤醒正常(启用睡眠需要bios中关闭power off energy saving)

Fn快捷键正常
```
仿冒白苹果鼠标教程[地址](https://sxz799.ml/2019/10/17/%E9%BB%91%E8%8B%B9%E6%9E%9C%E4%B9%8B%E4%BB%BF%E5%86%92%E7%99%BD%E8%8B%B9%E6%9E%9C%E9%BC%A0%E6%A0%87/)

##更新日志
### 2020年08月07日23:14:34
	删除oc引导
### 2020年04月07日23:14:34
	更新部分驱动
### 2020年04月06日12:20:37
	修复OC引导部分bug
	目前bug
	    无法睡眠
		无法使用触控板
		开机卡顿几秒
### 2020年04月05日13:36:17
	更新添加OC引导
	目前bug：
		无法调解屏幕亮度
		无法睡眠
		无法使用触控板
		开机卡顿几秒
### 2020年03月31日15:32:12
	FakeSMC更换为VirtualSMC.
