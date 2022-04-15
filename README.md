# Hackintosh Monterey EFI
* Hackintosh Monterey EFI for MSI B450m Mortar + R5 2600 + RX 570

### EFI不再更新了
* 虽然觉得部分功能都近乎完美了，但是在adobe软件里兼容性还是硬伤，已经更换硬件用回了intel了，最后更新一次在用的efi，之后不再更新了。


### EFI详情
* 支持MacOS版本：Monterey 12.3
* OpenCore版本：0.7.8
* 更新日期：2022年04月02日


### 配置清单
* 主板：MSI B450m Mortar 迫击炮钛金版
* CPU：AMD Ryzen5 2600
* 显卡：Radeon RX 570 迪兰恒进/酷能 (后来换成了R7-370加了驱动)
* 网卡：Fenvi-T1919 / BCM94360CD
* 内存：铭瑄/MAXSUN DDR4 2600MHZ 16GX2 （超频3600mhz）
* 固态硬盘：海康威视C2000 512G 
* 机械硬盘：西部数据 3T + 东芝 3T （1T作为TimeMachine备份）

### 完美程度
* 独显硬件加速
* 使用VoodooHDA解决音频输入，可正常使用麦克风。
* 接力、随航功能正常使用。
* iMessage、FaceTime正常登陆使用。
* 有线网络/无线网络2G+5G正常使用。
* 前后各IO接口正常使用。
* 支持2k输出/4K未测试。
* 随眠唤醒不是100%成功。

### BIOS推荐设置
* 高级 -- windows操作系统的配置 -- CSM 改为 UEFI
* 高级 -- windows操作系统的配置 -- 安全引导 -- 禁止安全启动（默认禁止）
* 高级 -- USB设置 -- XHCI Hand-off -- 开启（默认开启）

### 使用说明
* 本EFI支持由Catalina直接更新到BigSur，在软件更新中下载好最新版本系统，重启前替换EFI即可。
* 本EFI在目前的BigSur版本均可使用，支持小版本内直接更新系统。

### 可能问题及解决方案
* 更新完系统后没有Hipi的话，可以使用one-key-hidpi-master脚本一键开启。
* 系统可以正常休眠，不过睡眠唤醒不是100%能成功，建议在节能中设置「防止系统进入睡眠」。
* 如果无法登陆使用iMessage和FaceTime等功能，可以自行替换三码和ROM参数，详细可以参考下方链接。

### Fixing iMessage and other services with OpenCore
* [https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#clean-out-old-attempts](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#clean-out-old-attempts)
