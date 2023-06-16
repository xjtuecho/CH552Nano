# 固件说明

## CH552_Blaster_v22.2.27.hex

- 增加TCK频率设置功能，默认8MHz。
- 使能外部时钟，方便使用无源晶振对外提供时钟，CH552本身仍然使用内部16M时钟。
- **USB-Blaster驱动**请使用`Quartus II 13.0sp1`版本，本目录有下载，新版本驱动可能有问题。

## CH552_Blaster_v21.11.9.hex

- 再次优化性能，下载速度提高到原始版本的5.46倍。

## CH552_Blaster_v21.11.6.hex

- 修改LED的控制逻辑，忙时低电平点亮，闲时高电平熄灭。
- 优化性能，下载速度提高到原始版本的3.88倍。

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


## CH552_JTAG_SMT2.hex

- Digilent JTAG SMT2下载器固件，用于Xilinx的FPGA/CPLD下载调试。
- 来自：[CH552 模拟 Digilent JTAG-SMT2](https://whycan.com/t_8631.html)

### 管脚分配

- P1.4 TMS
- P1.5 TDI
- P1.6 TDO
- P1.7 TCK

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