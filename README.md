# XiaoMi-Ruby-15.6-UMA-only

 Catalina 10.15.4 is supported
  
 请各位自己生成smbios的序列号，机型不要改，容易出问题。
 
 -----------------Work not well---------------------------
 
 Internal speaker can not work
  
 4K solution: Due to HDMI bandwith, you must make resolution down to 2880x1600 with 60Hz. (SwitchResX can help you setting it)
 
 Card Reader can passthrough to Virtualmachine, but not work in Mac
 
 外放无解，耳机完美，有能外放的务必告诉我
 
 读卡器为usb设备，可以通过虚拟机直通来使用
 
 --------------------Warning-------------------------------
 
 My laptop editon not have a Nvidia-MX graphic card, if you want use my EFI, you need to add DSDT-DDGPU and some boot argument (nv_disable)
 
 When install system，block ssdt-uiac to prevent kernel panic from usb
 
 安装系统usb方面可能出现问题，还没实践
 
 ---------------Hardware Recommend------------------------
 
 This laptop can use BCM94360CS2, you just need make conversion card not so long, no need to do any destroy on your laptop!
 
 This laptop can use NVME X4 SSD, it's perfect, using samsung may have problem in Mac
 
 This laptop can change display LED to N156HCE-EN1, it's only need 200RMB. Worth!
 
 网卡、蓝牙问题强烈建议使用BCM94360CS2，不需要额外驱动
 
 支持NVME
 
 屏幕可以更换72ntsc
 
 
 
 
