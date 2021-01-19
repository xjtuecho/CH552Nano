# 固件说明

## prgmr1.0a3u3.hex

编程器固件，使用WCHISPTool写入CH552，运行频率24M，需要5V供电。

## CH552_MinPro-I_3V3_16M.hex

编程器固件，使用WCHISPTool写入CH552，运行频率16M，支持3.3/5V供电。

## N76E003_ICP_Loader.hex

N76E003 ICP固件，使用WCHISPTool写入CH552。

## USBJTAG_38400_v20.10.26.hex

TangNano开发板上的USBJTAG固件，使用WCHISPTool写入CH552。主要参数如下：

- 输入时钟24M，CH552使用内部24M时钟
- C51运行频率16M，兼容3.3V和5V电平
- TCK频率2.667M
- USBTTL波特率固定38400
- P1.0输出频率4M
- LED0固定1Hz闪烁

## TangNano.fs

TangNano开发板内置的GW1N-1 FPGA测试固件，内部将TXD和RXD短接，用于测试USBTTL自发自收。