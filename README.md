

# Asus-Prime-Z590-P黑苹果EFI OpenCore1.0.3（2025.02.17更新）


配置文件仍然在持续更新中，如果有任何问题或者错误请向我反馈。

以下是本人电脑的配置信息

---


<h2>电脑配置：</h2>

操作系统：

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;W印dows **[11 专业版（24H2）](https://www.microsoft.com/zh-cn/software-download/windows11)**

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;MacOS Sequoia 15 **[15.3.1(24D70)](https://www.apple.com.cn/macos/ventura/)**

处理器&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&nbsp;&nbsp;&nbsp; 英特尔 &nbsp;&nbsp;Core **[i9-10900k@3.70GHz](https://www.intel.cn/content/www/cn/zh/products/sku/199332/intel-core-i910900k-processor-20m-cache-up-to-5-30-ghz/specifications.html)** 10核

主板&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;华硕&nbsp;&nbsp;**[Asus-Prime-Z590-P](https://www.asus.com.cn/motherboards-components/motherboards/prime/prime-z590-p/)**

显卡&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&nbsp;&nbsp;华擎&nbsp;&nbsp;**[AMD Radeon™ RX 6800 XT
Phantom Gaming D 16G OC](https://pg.asrock.com/Graphics-Card/AMD/Radeon%20RX%206800%20XT%20Phantom%20Gaming%20D%2016G%20OC/index.tw.asp)/HD630(只硬解）**

内存&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&nbsp;&nbsp;金士顿&nbsp;&nbsp;**[KF432C16BB/16 （16gx2）](https://www.kingston.com.cn/cn/memory/search?partid=KF432C16BB%2F16)**&ensp;&ensp;&ensp;&ensp;[查看方式](https://www.kingston.com.cn/cn/memory/memory-part-number-decoder)

主硬盘&ensp;&nbsp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&nbsp;&nbsp;&nbsp;**[Samsung SSD 970 EVO Plus 1TB+2TB](https://www.samsung.com/tw/memory-storage/nvme-ssd/970-evo-plus-nvme-m-2-ssd-1tb-mz-v7s1t0bw/) +Samsung SSD 860 EVO 500GB**

声卡&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&nbsp;&nbsp;&nbsp;&nbsp;Realtek **ALC897**

网卡&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&nbsp;&nbsp;&nbsp;&nbsp;**BCM94360CD**

摄像头&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&nbsp;&nbsp;&nbsp;**[LogiC1000e](https://www.logitech.com/zh-cn/products/webcams/brio-4k-hdr-webcam.html?srsltid=AfmBOorAurNkhv166yF81RLL4X0y_lTen3GJs5I0ckBAckve0emN8Yfk)**

---

<h2>驱动情况：</h2>

- [x] 显卡：核显只作为硬解码，独显免驱 *（BIOS开启初始化iGPU）*

&ensp;&ensp;&ensp;&ensp;&ensp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&ensp;[显示器调节软件](https://github.com/MonitorControl/MonitorControl#readme)

- [x] 声卡：正常使用（id:11&nbsp;&nbsp;正常输入与输出）

- [x] 网卡：免驱网卡**BCM94360CD**

- [x] CPU变频正常（ **35档** ）

- [x] FaceTime ，iMessage，隔空投送，接力，Apple Watch解锁（前提三码入住）
      
- [x] USB&ensp;2.0；3.0&ensp;已定制

- [ ] 目前已知问题：
- [ ] 核显无法作为屏幕输出
- [ ] 随航，相机接续互通 导致电脑死机


---

<h2>BIOS设置：</h2>

- 更新到**1601**版本
- BIOS设置为如下（启动按DEL/F2键）

高级模式（F7）

&ensp;&ensp;&ensp;&ensp;**Ai Tweaker**

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*-Ai智能超频：XMP I*

&ensp;&ensp;&ensp;&ensp;**高级**

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-CPU设置

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*Intel (VMX)虚拟化技术：Enabled*

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-北桥

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-显示设置

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*初始化iGPU：Disabled*

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-PCH储存设置

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*SATA6G_(1-4)热拔插：Enabled*

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-Thunderbolt（TM）设置

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*独立Thunderbolt（TM）支持：Disable*

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-PCI Subsystem Settings

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*大于4G地址空间解码：Enabled*

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-USB设置

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*Legacy USB 支持：开启*

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*XHCI 接管：开启*

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-内置设备

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-串口设置

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*串口：Disabled*

&ensp;&ensp;&ensp;&ensp;**启动**

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-CSM（兼容性支持模块）

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*开启CSM：Disabled*

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-安全启动

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*操作系统类型：其他操作系统*

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-启动设置

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*快速启动：关闭*

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*开机自检（POST）延迟时间：0秒*

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*若出现错误等按下F1键：Disabled*

&ensp;&ensp;&ensp;&ensp;**工具**

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;-华硕Armoury Crate

&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;*下载并安装ARMOURY CRATE应用程序：Disabled*

---

感谢：

[乌龙蜜桃来一打](https://space.bilibili.com/244390800/?spm_id_from=333.999.0.0)

[国光](https://www.sqlsec.com/about/)

[独行之秀才](https://shuiyunxc.oschina.io)

[黑果小兵的部落阁](https://blog.daliansky.net/)

[大头蔡Cass](https://space.bilibili.com/16323318/?spm_id_from=333.999.0.0)

[tonymacx86](https://www.tonymacx86.com/)

等提供的软件及技术支持！

---

2025年2月17日周一 （更新）

多云12℃～20℃
