# 固件说明

## CH552_Blaster_v21.10.21.hex

USB-Blaster固件，调试烧录Altera的FPGA和CPLD，使用WCHISPTool写入CH552。主要参数如下:

- 支持Altera和AGM公司的FPGA和CPLD
- 支持JTAG和AS两种下载方式
- 使用MCU内部时钟，运行频率16MHz，无需外部晶振。
- 3.3V供电，IO电平为3.3V
- 所有IO全部使用到
- 支持串口命令行

### 管脚分配

- P1.1 板载LED
- P1.4 NCS
- P1.5 TDI
- P1.6 TDO
- P1.7 TCK
- P3.2 TMS
- P3.3 ASDO
- P3.4 NCE

注意：

- JTAG接口只需要连接TCK、TMS、TDI、TDO四个信号
- AS接口除了JTAG的四个信号还需要连接ASDO、NCS、NCE三个信号
- AG1280Q48下载FLASH需要使用AS接口，NCE信号不接
- P3.0和P3.1为UART接口，波特率38400，可以使用超级终端连接
- P3.6和P3.7为USB接口

## prgmr1.0a3u3.hex

编程器固件，使用WCHISPTool写入CH552，运行频率24M，需要5V供电。

## CH552_MinPro-I_3V3_16M.hex

编程器固件，使用WCHISPTool写入CH552，运行频率16M，支持3.3/5V供电。

## N76E003_ICP_Loader.hex

N76E003 ICP固件，使用WCHISPTool写入CH552。

## USBJTAG_38400_v20.10.26.hex

TangNano开发板上的USBJTAG固件，使用WCHISPTool写入CH552。主要参数如下：

- 输入时钟24M，CH552使用内部24M时钟
- MCU运行频率16M，兼容3.3V和5V电平
- TCK频率2.667M
- USBTTL波特率固定38400
- P1.0输出频率4M
- LED0固定1Hz闪烁

## TangNano.fs

TangNano开发板内置的GW1N-1 FPGA测试固件，内部将TXD和RXD短接，用于测试USBTTL自发自收。