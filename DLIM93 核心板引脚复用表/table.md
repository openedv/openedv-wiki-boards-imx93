---
title: '核心板复用表'
sidebar_position: 1
---

## AB座子

| 管脚号 | 核心板管脚名   | 出厂系统默认配置/开发板接口 | GPIO编号   | CPU球号                     | 功能描述                                                    | 管脚类型  | 电平域电压     | 可复用功能(需结合具体需求分析)  红色加粗部分表示出厂系统默认功能 |
| ------ | -------------- | --------------------------- | ---------- | --------------------------- | ----------------------------------------------------------- | --------- | -------------- | ------------------------------------------------------------ |
| A1     | GND            |                             |            |                             | 接地                                                        |           |                |                                                              |
| A2     | PMIC_ON_REQ    | PMIC_ON_REQ                 |            | A17                         | 系统信号                                                    | 输入/输出 | 1.8V           | PMIC_ON_REQ                                                  |
| A3     | PMIC_32K_OUT   | PMIC_32K_OUT                |            |                             | 系统信号                                                    | 输入/输出 | 3.3V           | PMIC_32K_OUT                                                 |
| A4     | RESET          | RESET                       |            |                             | 复位信号                                                    | 输入/输出 | 1.8V           | RESET                                                        |
| A5     | GPIO_IO12      | UART8_TX                    | GPIO2_IO12 | N20                         | 全双工通用同步/异步串行收发接口8_发送端                     | 输入/输出 | 3.3V           | GPIO2_IO12,TPM3_CH2,PDM_BIT_STREAM02,MEDIAMIX_DISP_DATA08,LPSPI8_PCS0,LPUART8_TX,LPI2C8_SDA,SAI3_RX_SYNC |
| A6     | GPIO_IO13      | UART8_RX                    | GPIO2_IO13 | N21                         | 全双工通用同步/异步串行收发接口8_接收端                     | 输入/输出 | 3.3V           | GPIO2_IO13,TPM4_CH2,PDM_BIT_STREAM03,MEDIAMIX_DISP_DATA09,LPSPI8_SIN,LPUART8_RX,LPI2C8_SCL,FLEXIO1_FLEXIO13 |
| A7     | GPIO_IO14      | UART4_TX                    | GPIO2_IO14 | P20                         | 全双工通用同步/异步串行收发接口4_发送端                     | 输入/输出 | 3.3V           | GPIO2_IO14,LPUART3_TX,MEDIAMIX_CAM_DATA06,MEDIAMIX_DISP_DATA10,LPSPI8_SOUT,LPUART8_CTS_B,LPUART4_TX,FLEXIO1_FLEXIO14 |
| A8     | GPIO_IO15      | UART4_RX                    | GPIO2_IO15 | P21                         | 全双工通用同步/异步串行收发接口4_接收端                     | 输入/输出 | 3.3V           | GPIO2_IO15,LPUART3_RX,MEDIAMIX_CAM_DATA07,MEDIAMIX_DISP_DATA11,LPSPI8_SCK,LPUART8_RTS_B,LPUART4_RX,FLEXIO1_FLEXIO15 |
| A9     | GPIO_IO10      | SPI3_MOSI                   | GPIO2_IO10 | N17                         | 串行外部设备接口3_主发从收信号                              | 输入/输出 | 3.3V           | GPIO2_IO10,LPSPI3_SOUT,MEDIAMIX_CAM_DATA04  ,MEDIAMIX_DISP_DATA06,TPM4_EXTCLK,LPUART7_CTS_B,LPI2C8_SDA,FLEXIO1_FLEXIO10 |
| A10    | GPIO_IO11      | SPI3_CLK                    | GPIO2_IO11 | N18                         | 串行外部设备接口3_串行时钟                                  | 输入/输出 | 3.3V           | GPIO2_IO11,LPSPI3_SCK,MEDIAMIX_CAM_DATA05,MEDIAMIX_DISP_DATA07,TPM5_EXTCLK  ,LPUART7_RTS_B,LPI2C8_SCL,FLEXIO1_FLEXIO11 |
| A11    | GPIO_IO09      | SPI3_MISO                   | GPIO2_IO09 | M21                         | 串行外部设备接口3_主收从发信号                              | 输入/输出 | 3.3V           | GPIO2_IO09,LPSPI3_SIN,MEDIAMIX_CAM_DATA03,MEDIAMIX_DISP_DATA05,TPM3_EXTCLK,LPUART7_RX,LPI2C7_SCL,FLEXIO1_FLEXIO09 |
| A12    | GPIO_IO08      | SPI3_CS0                    | GPIO2_IO08 | M20                         | 串行外部设备接口3_片选信号                                  | 输入/输出 | 3.3V           | GPIO2_IO08,LPSPI3_PCS0,MEDIAMIX_CAM_DATA02,MEDIAMIX_DISP_DATA04,TPM6_CH0,LPUART7_TX,LPI2C7_SDA,  FLEXIO1_FLEXIO08 |
| A13    | GND            |                             |            |                             | 接地                                                        |           |                |                                                              |
| A14    | GPIO_IO07      | CSI_RST                     | GPIO2_IO07 | L21                         | MIPI CSI复位信号                                            | 输入/输出 | 3.3V           | GPIO2_IO07,LPSPI3_PCS1,MEDIAMIX_CAM_DATA01,MEDIAMIX_DISP_DATA03,LPSPI7_SCK,LPUART6_RTS_B,LPI2C7_SCL,FLEXIO1_FLEXIO07 |
| A15    | GPIO_IO06      | CSI_PWDN                    | GPIO2_IO06 | L20                         | MIPI CSI电源控制信号                                        | 输入/输出 | 3.3V           | GPIO2_IO06,TPM5_CH0,PDM_BIT_STREAM01,MEDIAMIX_DISP_DATA02,LPSPI7_SOUT,LPUART6_CTS_B,LPI2C7_SDA,FLEXIO1_FLEXIO06 |
| A16    | GPIO_IO03      | I2C4_SCL                    | GPIO2_IO03 | K21                         | I2C总线4_时钟信号                                           | 输入/输出 | 3.3V           | GPIO2_IO03,LPI2C4_SCL,MEDIAMIX_CAM_HSYNC,MEDIAMIX_DISP_HSYNC,LPSPI6_SCK,LPUART5_RTS_B,LPI2C6_SCL,FLEXIO1_FLEXIO03 |
| A17    | GPIO_IO02      | I2C4_SDA                    | GPIO2_IO02 | K20                         | I2C总线4_数据/地址信号                                      | 输入/输出 | 3.3V           | GPIO2_IO02,LPI2C4_SDA,MEDIAMIX_CAM_VSYNC,MEDIAMIX_DISP_VSYNC,LPSPI6_SOUT,LPUART5_CTS_B,LPI2C6_SDA,FLEXIO1_FLEXIO02 |
| A18    | GPIO_IO01      | BT_REG_EN                   | GPIO2_IO01 | J20                         | 蓝牙电源使能信号                                            | 输入/输出 | 3.3V           | GPIO2_IO01,LPI2C3_SCL,MEDIAMIX_CAM_DATA00,MEDIAMIX_DISP_DE,LPSPI6_SIN,LPUART5_RX,LPI2C5_SCL,FLEXIO1_FLEXIO01 |
| A19    | GPIO_IO00      | WIFI_REG_EN                 | GPIO2_IO00 | J21                         | WIFI电源使能信号                                            | 输入/输出 | 3.3V           | GPIO2_IO00,LPI2C3_SDA,MEDIAMIX_CAM_CLK,MEDIAMIX_DISP_CLK,LPSPI6_PCS0,LPUART5_TX,LPI2C5_SDA,FLEXIO1_FLEXIO00 |
| A20    | GPIO_IO05      | LVDS_DSI_BL_PWM             | GPIO2_IO05 | L18                         | LVDS、MIPI-DSI背光信号线                                    | 输入/输出 | 3.3V           | GPIO2_IO05,TPM4_CH0,PDM_BIT_STREAM00,MEDIAMIX_DISP_DATA01,LPSPI7_SIN,LPUART6_RX,LPI2C6_SCL,FLEXIO1_FLEXIO05 |
| A21    | GPIO_IO04      | LED0                        | GPIO2_IO04 | L17                         | 用户LED灯                                                   | 输入/输出 | 3.3V           | GPIO2_IO04,TPM3_CH0,PDM_CLK,MEDIAMIX_DISP_DATA00,LPSPI7_PCS0,LPUART6_TX,LPI2C6_SDA,FLEXIO1_FLEXIO04 |
| A22    | GND            |                             |            |                             | 接地                                                        |           |                |                                                              |
| A23    | PDM_DATA0      | CAN1_RX                     | GPIO1_IO09 | J17                         | 具有灵活数据速率的控制器区域网络接口1_接收端                | 输入/输出 | 3.3V           | PDM_BIT_STREAM00,MQS1_RIGHT,LPSPI1_PCS1,TPM1_EXTCLK,LPTMR1_ALT2,GPIO1_IO09,CAN1_RX |
| A24    | PDM_DATA1      | KEY                         | GPIO1_IO10 | G18                         | 按键信号                                                    | 输入/输出 | 3.3V           | PDM_BIT_STREAM01,NMI_GLUE_NMI,LPSPI2_PCS1,TPM2_EXTCLK,LPTMR1_ALT3,GPIO1_IO10,CCMSRCGPCMIX_EXT_CLK1 |
| A25    | PDM_CLK        | CAN1_TX                     | GPIO1_IO08 | G17                         | 具有灵活数据速率的控制器区域网络接口1_发送端                | 输入/输出 | 3.3V           | PDM_CLK,MQS1_LEFT,LPTMR1_ALT1,GPIO1_IO08,CAN1_TX             |
| A26    | ONOFF          | ONOFF                       |            | A19                         | 系统信号                                                    | 输入/输出 | 1.8V           | ONOFF                                                        |
| A27    | GND            |                             |            |                             | 接地                                                        |           |                |                                                              |
| A28    | TAMPER1        | TAMPER1                     |            | F14                         | 系统信号                                                    | 输入/输出 | 1.8V           | TAMPER1                                                      |
| A29    | POR_B          | POR_B                       |            | A16                         | 系统信号                                                    | 输入/输出 | 1.8V           | POR_B                                                        |
| A30    | TAMPER0        | TAMPER0                     |            | B16                         | 系统信号                                                    | 输入/输出 | 1.8V           | TAMPER0                                                      |
| A31    | GND            |                             |            |                             | 接地                                                        |           |                |                                                              |
| A32    | USB2_VBUS      | USB2(USB_HOST)              |            | E14                         | HOST_VBUS电源                                               | 电源      | 3.3V           | USB2_VBUS                                                    |
| A33    | USB2_DN        | USB2(USB_HOST)              | A15        | USB2数据差分负信号(USB2.0)  | 输入/输出                                                   | 3.3V      | USB2_D_N       |                                                              |
| A34    | USB2_DP        | USB2(USB_HOST)              | B15        | USB2数据差分正信号(USB2.0)  | 输入/输出                                                   | 3.3V      | USB2_D_P       |                                                              |
| A35    | USB2_ID        | USB2(USB_HOST)              | E12        | OTG_ID信号                  | 输入/输出                                                   | 1.8V      | USB2_ID        |                                                              |
| A36    | GND            |                             |            |                             | 接地                                                        |           |                |                                                              |
| A37    | USB1_VBUS      | USB1(USB_OTG)               |            | F12                         | OTG_VBUS电源                                                | 电源      | 3.3V           | USB1_VBUS                                                    |
| A38    | USB1_DN        | USB1(USB_OTG)               | A14        | USB2数据差分负信号(USB2.0)  | 模拟                                                        | 3.3V      | USB1_D_N       |                                                              |
| A39    | USB1_DP        | USB1(USB_OTG)               | B14        | USB2数据差分正信号(USB2.0)  | 模拟                                                        | 3.3V      | USB1_D_P       |                                                              |
| A40    | USB1_ID        | USB1(USB_OTG)               | C11        | OTG_ID信号                  | 输入/输出                                                   | 1.8V      | USB1_ID        |                                                              |
| A41    | GND            |                             |            |                             | 接地                                                        |           |                |                                                              |
| A42    | MIPI_CSI_D0_P  | MIPI-CSI CAMERA             |            | B11                         | MIPI CSI数据通道0差分正信号                                 | 输入/输出 |                | MIPI_CSI_D0_P                                                |
| A43    | MIPI_CSI_D0_N  | MIPI-CSI CAMERA             | A11        | MIPI CSI数据通道0差分负信号 | 输入/输出                                                   |           | MIPI_CSI_D0_N  |                                                              |
| A44    | GND            | MIPI-CSI CAMERA             |            | 接地                        |                                                             |           |                |                                                              |
| A45    | MIPI_CSI_D1_P  | MIPI-CSI CAMERA             | B10        | MIPI CSI数据通道1差分正信号 | 输入/输出                                                   |           | MIPI_CSI_D1_P  |                                                              |
| A46    | MIPI_CSI_D1_N  | MIPI-CSI CAMERA             | A10        | MIPI CSI数据通道1差分负信号 | 输入/输出                                                   |           | MIPI_CSI_D1_N  |                                                              |
| A47    | GND            | MIPI-CSI CAMERA             |            | 接地                        |                                                             |           |                |                                                              |
| A48    | MIPI_CSI_CLK_P | MIPI-CSI CAMERA             | E10        | MIPI CSI时钟同步差分正信号  | 输入/输出                                                   |           | MIPI_CSI_CLK_P |                                                              |
| A49    | MIPI_CSI_CLK_N | MIPI-CSI CAMERA             | D10        | MIPI CSI时钟同步差分负信号  | 输入/输出                                                   |           | MIPI_CSI_CLK_N |                                                              |
| A50    | GND            |                             |            |                             | 接地                                                        |           |                |                                                              |
| A51    | GND            |                             |            |                             | 接地                                                        |           |                |                                                              |
| A52    | LVDS_TX3_P     | LVDS                        |            | C1                          | LVDS数据通道3差分正信号                                     | 输入/输出 | 1.8V           | LVDS_TX3_P                                                   |
| A53    | LVDS_TX3_N     | LVDS                        | B1         | LVDS数据通道3差分负信号     | 输入/输出                                                   | 1.8V      | LVDS_TX3_N     |                                                              |
| A54    | GND            | LVDS                        |            | 接地                        |                                                             |           |                |                                                              |
| A55    | LVDS_CLK_P     | LVDS                        | B3         | LVDS时钟同步差分正信号      | 输入/输出                                                   | 1.8V      | LVDS_CLK_P     |                                                              |
| A56    | LVDS_CLK_N     | LVDS                        | A3         | LVDS时钟同步差分负信号      | 输入/输出                                                   | 1.8V      | LVDS_CLK_N     |                                                              |
| A57    | GND            | LVDS                        |            | 接地                        |                                                             |           |                |                                                              |
| A58    | LVDS_TX2_P     | LVDS                        | B2         | LVDS数据通道2差分正信号     | 输入/输出                                                   | 1.8V      | LVDS_TX2_P     |                                                              |
| A59    | LVDS_TX2_N     | LVDS                        | A2         | LVDS数据通道2差分负信号     | 输入/输出                                                   | 1.8V      | LVDS_TX2_N     |                                                              |
| A60    | GND            | LVDS                        |            | 接地                        |                                                             |           |                |                                                              |
| A61    | LVDS_TX1_P     | LVDS                        | B4         | LVDS数据通道1差分正信号     | 输入/输出                                                   | 1.8V      | LVDS_TX1_P     |                                                              |
| A62    | LVDS_TX1_N     | LVDS                        | A4         | LVDS数据通道1差分负信号     | 输入/输出                                                   | 1.8V      | LVDS_TX1_N     |                                                              |
| A63    | GND            | LVDS                        |            | 接地                        |                                                             |           |                |                                                              |
| A64    | LVDS_TX0_P     | LVDS                        | B5         | LVDS数据通道0差分正信号     | 输入/输出                                                   | 1.8V      | LVDS_TX0_P     |                                                              |
| A65    | LVDS_TX0_N     | LVDS                        | A5         | LVDS数据通道0差分负信号     | 输入/输出                                                   | 1.8V      | LVDS_TX0_N     |                                                              |
| A66    | GND            |                             |            |                             | 接地                                                        |           |                |                                                              |
| A67    | MIPI_DSI_CLK_N | MIPI-DSI                    |            | D6                          | MIPI CSI时钟同步差分负信号                                  | 输入/输出 |                | MIPI_DSI_CLK_N                                               |
| A68    | MIPI_DSI_CLK_P | MIPI-DSI                    | E6         | MIPI CSI时钟同步差分正信号  | 输入/输出                                                   |           | MIPI_DSI_CLK_P |                                                              |
| A69    | GND            | MIPI-DSI                    |            | 接地                        |                                                             |           |                |                                                              |
| A70    | MIPI_DSI_D0_N  | MIPI-DSI                    | A6         | MIPI CSI数据通道0差分负信号 | 输入/输出                                                   |           | MIPI_DSI_D0_N  |                                                              |
| A71    | MIPI_DSI_D0_P  | MIPI-DSI                    | B6         | MIPI CSI数据通道0差分正信号 | 输入/输出                                                   |           | MIPI_DSI_D0_P  |                                                              |
| A72    | GND            | MIPI-DSI                    |            | 接地                        |                                                             |           |                |                                                              |
| A73    | MIPI_DSI_D1_N  | MIPI-DSI                    | A7         | MIPI CSI数据通道1差分负信号 | 输入/输出                                                   |           | MIPI_DSI_D1_N  |                                                              |
| A74    | MIPI_DSI_D1_P  | MIPI-DSI                    | B7         | MIPI CSI数据通道1差分正信号 | 输入/输出                                                   |           | MIPI_DSI_D1_P  |                                                              |
| A75    | GND            | MIPI-DSI                    |            | 接地                        |                                                             |           |                |                                                              |
| A76    | MIPI_DSI_D2_N  | MIPI-DSI                    | A8         | MIPI CSI数据通道2差分负信号 | 输入/输出                                                   |           | MIPI_DSI_D2_N  |                                                              |
| A77    | MIPI_DSI_D2_P  | MIPI-DSI                    | B8         | MIPI CSI数据通道2差分正信号 | 输入/输出                                                   |           | MIPI_DSI_D2_P  |                                                              |
| A78    | GND            | MIPI-DSI                    |            | 接地                        |                                                             |           |                |                                                              |
| A79    | MIPI_DSI_D3_N  | MIPI-DSI                    | A9         | MIPI CSI数据通道3差分负信号 | 输入/输出                                                   |           | MIPI_DSI_D3_N  |                                                              |
| A80    | MIPI_DSI_D3_P  | MIPI-DSI                    | B9         | MIPI CSI数据通道3差分正信号 | 输入/输出                                                   |           | MIPI_DSI_D3_P  |                                                              |
| A81    | GND            |                             |            |                             | 接地                                                        |           |                |                                                              |
| A82    | ADC_IN0        | ADC                         |            | B19                         | ADC输入通道0                                                | 模拟      | 1.8V           | ADC_IN0                                                      |
| A83    | ADC_IN1        | ADC                         | A20        | ADC输入通道1                | 模拟                                                        | 1.8V      | ADC_IN1        |                                                              |
| A84    | ADC_IN2        | ADC                         | B20        | ADC输入通道2                | 模拟                                                        | 1.8V      | ADC_IN2        |                                                              |
| A85    | ADC_IN3        | ADC_LCD_ID                  |            | B21                         | ADC输入通道3                                                | 模拟      | 1.8V           | ADC_IN3                                                      |
| A86    | UART2_TXD      | BOOT_MODE1                  | GPIO1_IO07 | F21                         | 引导模式选择信号线、全双工通用同步/异步串行收发接口2_发送端 | 输入/输出 | 3.3V           | LPUART2_TX,LPUART1_RTS_B,LPSPI2_SCK,TPM1_CH3,GPIO1_IO07      |
| A87    | UART2_RXD      |                             | GPIO1_IO06 | F20                         | 全双工通用同步/异步串行收发接口2_接收端                     | 输入/输出 | 3.3V           | LPUART2_RX,LPUART1_CTS_B,LPSPI2_SOUT,TPM1_CH2,SAI1_MCLK,GPIO1_IO06 |
| A88    | UART1_TXD      | BOOT_MODE0                  | GPIO1_IO05 | E21                         | 引导模式选择信号线、全双工通用同步/异步串行收发接口1_发送端 | 输入/输出 | 3.3V           | LPUART1_TX,S400_UART_TX,LPSPI2_PCS0,TPM1_CH1,GPIO1_IO05      |
| A89    | UART1_RXD      |                             | GPIO1_IO04 | E20                         | 全双工通用同步/异步串行收发接口1_接收端                     | 输入/输出 | 3.3V           | LPUART1_RX,S400_UART_RX,LPSPI2_SIN,TPM1_CH0,GPIO1_IO04       |
| A90    | SAI1_TXD0      | BOOT_MODE3                  | GPIO1_IO13 | H21                         | 引导模式选择信号线                                          | 输入/输出 | 3.3V           | SAI1_TX_DATA00,LPUART2_RTS_B,LPSPI1_SCK,LPUART1_DTR_B,CAN1_TX,GPIO1_IO13 |
| A91    | SAI1_RXD0      | TP_RST                      | GPIO1_IO14 | H20                         | LVDS、MIPI-DSI触摸屏复位信号线                              | 输入/输出 | 3.3V           | SAI1_RX_DATA00,SAI1_MCLK,LPSPI1_SOUT,LPUART2_DSR_B,MQS1_RIGHT,GPIO1_IO14 |
| A92    | SAI1_TXC       | TP_INT                      | GPIO1_IO12 | G20                         | 触摸屏中断信号线                                            | 输入/输出 | 3.3V           | SAI1_TX_BCLK,LPUART2_CTS_B,LPSPI1_SIN,LPUART1_DSR_B,CAN1_RX,GPIO1_IO12 |
| A93    | SAI1_TXFS      | BOOT_MODE2                  | GPIO1_IO11 | G21                         | 引导模式选择信号线                                          | 输入/输出 | 3.3V           | SAI1_TX_SYNC,SAI1_TX_DATA01,LPSPI1_PCS0,LPUART2_DTR_B,MQS1_LEFT,GPIO1_IO11 |
| A94    | GND            |                             |            |                             | 接地                                                        |           |                |                                                              |
| A95 | NVCC_SD2 | TF  Card |            | R16 | SD2_CD电源 | 电源 | 3.3V/1.8V | NVCC_SD2 |
| A96 | NVCC_SD2 | TF  Card |            | R16 | SD2_CD电源 | 电源 | 3.3V/1.8V | NVCC_SD2 |
| A97 | VSD_3V3 | TF  Card |            |                             | VDD电源 | 电源 | 3.3V | VSD_3V3 |
| A98 | VSD_3V3 | TF  Card |            |                             | VDD电源 | 电源 | 3.3V | VSD_3V3 |
| A99 | NVCC_AON |  |  | L16 | 系统信号 | 输入/输出 | 3.3V | NVCC_AON |
| A100 | GND |  |  |  | 接地 |  |  |  |
| B1 | VCC_5V | VCC_IN |  |  | 核心板输入电源接口 | 电源 |  |  |
| B2 | VCC_5V | VCC_IN |  |  | 核心板输入电源接口 | 电源 |  |  |
| B3 | VCC_5V | VCC_IN |  |  | 核心板输入电源接口 | 电源 |  |  |
| B4 | VCC_5V | VCC_IN |  |  | 核心板输入电源接口 | 电源 |  |  |
| B5 | GND |  |  |  | 接地 |  |  |  |
| B6 | GND |  |  |  | 接地 |  |  |  |
| B7 | GND |  |  |  | 接地 |  |  |  |
| B8 | GND |  |  |  | 接地 |  |  |  |
| B9 | GND |  |  |  | 接地 |  |  |  |
| B10 | GPIO_IO16 | SAI3_TXC | GPIO2_IO16 | R21 | 串行音频接口3_子模块A位时钟信号 | 输入/输出 | 3.3V | GPIO2_IO16,SAI3_TX_BCLK,PDM_BIT_STREAM02,MEDIAMIX_DISP_DATA12,LPUART3_CTS_B,LPSPI4_PCS2,LPUART4_CTS_B,FLEXIO1_FLEXIO16 |
| B11 | GPIO_IO17 | SAI3_MCLK | GPIO2_IO17 | R20 | 串行音频接口3_主时钟信号 | 输入/输出 | 3.3V | GPIO2_IO17,SAI3_MCLK,MEDIAMIX_CAM_DATA08,MEDIAMIX_DISP_DATA13,LPUART3_RTS_B,LPSPI4_PCS1,LPUART4_RTS_B,FLEXIO1_FLEXIO17 |
| B12 | GPIO_IO18 | AUDIO_CTRL | GPIO2_IO18 | R18 | 音频功放芯片控制信号 | 输入/输出 | 3.3V | GPIO2_IO18,SAI3_RX_BCLK,MEDIAMIX_CAM_DATA09,MEDIAMIX_DISP_DATA14,LPSPI5_PCS0,LPSPI4_PCS0,TPM5_CH2,FLEXIO1_FLEXIO18 |
| B13 | GPIO_IO19 | SAI3_TXD | GPIO2_IO19 | R17 | 串行音频接口3_子模块A数据输入\输出 | 输入/输出 | 3.3V | GPIO2_IO19,SAI3_RX_SYNC,PDM_BIT_STREAM03,MEDIAMIX_DISP_DATA15,LPSPI5_SIN,LPSPI4_SIN,TPM6_CH2,SAI3_TX_DATA00 |
| B14 | GPIO_IO20 | SAI3_RXD | GPIO2_IO20 | T20 | 串行音频接口3_子模块A数据输入\输出 | 输入/输出 | 3.3V | GPIO2_IO20,SAI3_RX_DATA00,PDM_BIT_STREAM00,MEDIAMIX_DISP_DATA16,LPSPI5_SOUT,LPSPI4_SOUT,TPM3_CH1,FLEXIO1_FLEXIO20 |
| B15 | GPIO_IO21 | HP_DETECT | GPIO2_IO21 | T21 | 音频耳机插入检测信号 | 输入/输出 | 3.3V | GPIO2_IO21,SAI3_TX_DATA00,PDM_CLK,MEDIAMIX_DISP_DATA17,LPSPI5_SCK,LPSPI4_SCK,TPM4_CH1,SAI3_RX_BCLK |
| B16 | GPIO_IO22 | ENET1_RSTN | GPIO2_IO22 | U18 | 千兆网口1_复位信号 | 输入/输出 | 3.3V | GPIO2_IO22,USDHC3_CLK,SPDIF_IN,MEDIAMIX_DISP_DATA18,TPM5_CH1,TPM6_EXTCLK,LPI2C5_SDA,FLEXIO1_FLEXIO22 |
| B17 | GPIO_IO23 | ENET1_INTN | GPIO2_IO23 | U20 | 千兆网口1_中断信号 | 输入/输出 | 3.3V | GPIO2_IO23,USDHC3_CMD,SPDIF_OUT,MEDIAMIX_DISP_DATA19,TPM6_CH1,LPI2C5_SCL,FLEXIO1_FLEXIO23 |
| B18 | GND |  |  |  | 接地 |  |  |  |
| B19 | GPIO_IO24 | ENET2_RSTN | GPIO2_IO24 | U21 | 千兆网口2_复位信号 | 输入/输出 | 3.3V | GPIO2_IO24,USDHC3_DATA0,MEDIAMIX_DISP_DATA20,TPM3_CH3,JTAG_MUX_TDO,LPSPI6_PCS1,FLEXIO1_FLEXIO24 |
| B20 | GPIO_IO25 | CAN2_TX | GPIO2_IO25 | V21 | 具有灵活数据速率的控制器区域网络接口2_发送端 | 输入/输出 | 3.3V | GPIO2_IO25,USDHC3_DATA1,CAN2_TX,MEDIAMIX_DISP_DATA21,TPM4_CH3,JTAG_MUX_TCK,LPSPI7_PCS1,FLEXIO1_FLEXIO25 |
| B21 | GPIO_IO26 | SAI3_TXFS | GPIO2_IO26 | V20 | 串行音频接口3_子模块A帧同步信号 | 输入/输出 | 3.3V | GPIO2_IO26,USDHC3_DATA2,PDM_BIT_STREAM01,MEDIAMIX_DISP_DATA22,TPM5_CH3,JTAG_MUX_TDI,LPSPI8_PCS1,SAI3_TX_SYNC |
| B22 | GPIO_IO27 | CAN2_RX | GPIO2_IO27 | W21 | 具有灵活数据速率的控制器区域网络接口2_接收端 | 输入/输出 | 3.3V | GPIO2_IO27,USDHC3_DATA3,CAN2_RX,MEDIAMIX_DISP_DATA23,TPM6_CH3,JTAG_MUX_TMS,LPSPI5_PCS1,FLEXIO1_FLEXIO27 |
| B23 | GPIO_IO28 | ENET2_INTN | GPIO2_IO28 | W20 | 千兆网口2_中断信号 | 输入/输出 | 3.3V | GPIO2_IO28,LPI2C3_SDA,FLEXIO1_FLEXIO28 |
| B24 | GPIO_IO29 |  | GPIO2_IO29 | Y21 |  | 输入/输出 | 3.3V | GPIO2_IO29,LPI2C3_SCL,FLEXIO1_FLEXIO29 |
| B25 | GND |  |  |  | 接地 |  |  |  |
| B26 | SD3_CMD | SDIO  WIFI&BLUETOOTH | GPIO3_IO21 | U16 | SD3命令线 | 输入/输出 | 1.8V | USDHC3_CMD,FLEXSPI1_A_SS0_B,FLEXIO1_FLEXIO21,GPIO3_IO21 |
| B27 | SD3_CLK | SDIO  WIFI&BLUETOOTH | GPIO3_IO20 | V16 | SD3时钟线 | 输入/输出 | 1.8V | USDHC3_CLK,FLEXSPI1_A_SCLK,FLEXIO1_FLEXIO20,GPIO3_IO20 |
| B28 | SD3_DATA0 | SDIO  WIFI&BLUETOOTH | GPIO3_IO22 | T16 | SD3数据线0 | 输入/输出 | 1.8V | USDHC3_DATA0,FLEXSPI1_A_DATA00,FLEXIO1_FLEXIO22,GPIO3_IO22 |
| B29 | SD3_DATA1 | SDIO  WIFI&BLUETOOTH | GPIO3_IO23 | V14 | SD3数据线1 | 输入/输出 | 1.8V | USDHC3_DATA1,FLEXSPI1_A_DATA01,FLEXIO1_FLEXIO23,GPIO3_IO23 |
| B30 | SD3_DATA2 | SDIO  WIFI&BLUETOOTH | GPIO3_IO24 | U14 | SD3数据线2 | 输入/输出 | 1.8V | USDHC3_DATA2,FLEXSPI1_A_DATA02,FLEXIO1_FLEXIO24,GPIO3_IO24 |
| B31 | SD3_DATA3 | SDIO  WIFI&BLUETOOTH | GPIO3_IO25 | T14 | SD3数据线3 | 输入/输出 | 1.8V | USDHC3_DATA3,FLEXSPI1_A_DATA03,FLEXIO1_FLEXIO25,GPIO3_IO25 |
| B32 | GND |  |  |  | 接地 |  |  |  |
| B33 | I2C1_SCL | CODEC ES8388 | GPIO1_IO00 | C20 | I2C总线1_时钟信号 | 输入/输出 | 3.3V | LPI2C1_SCL,I3C1_SCL,LPUART1_DCB_B,TPM2_CH0,GPIO1_IO00 |
| B34 | I2C1_SDA | CODEC ES8388                | GPIO1_IO01 | C21                         | I2C总线1_数据/地址信号                                      | 输入/输出 | 3.3V           | LPI2C1_SDA,I3C1_SDA,LPUART1_RIN_B,TPM2_CH1,GPIO1_IO01 |
| B35 | I2C1_SCL_1V8 | MIPI-CSI CAMERA |  |  | I2C总线1_1V8_时钟信号 | 输入/输出 | 1.8V | I2C1_SCL_1V8 |
| B36 | I2C1_SDA_1V8 | MIPI-CSI CAMERA |  |                             | I2C总线1_1V8_数据/地址信号                                  | 输入/输出 | 1.8V           | I2C1_SDA_1V8 |
| B37 | I2C2_SCL | RTC | GPIO1_IO02 | D20 | I2C总线2_时钟信号 | 输入/输出 | 3.3V | LPI2C2_SCL,I3C1_PUR,LPUART2_DCB_B,TPM2_CH2,SAI1_RX_SYNC,GPIO1_IO02,I3C1_PUR_B |
| B38 | I2C2_SDA | RTC                         | GPIO1_IO03 | D21                         | I2C总线2_数据/地址信号                                      | 输入/输出 | 3.3V           | LPI2C2_SDA,LPUART2_RIN_B,TPM2_CH3,SAI1_RX_BCLK,GPIO1_IO03 |
| B39 | GND |  |  |  | 接地 |  |  |  |
| B40 | CCM_CLKO1 | WIFI_WAKE_HOST | GPIO3_IO26 | AA2 | WiFi唤醒主机信号 | 输入/输出 | 1.8V | CCMSRCGPCMIX_CLKO1,FLEXIO1_FLEXIO26,GPIO3_IO26 |
| B41 | CCM_CLKO2 | BT_WAKE_HOST | GPIO3_IO27 | Y3 | 蓝牙唤醒主机信号 | 输入/输出 | 1.8V | CCMSRCGPCMIX_CLKO2,FLEXIO1_FLEXIO27,GPIO3_IO27 |
| B42 | CCM_CLKO3 | BT_WAKE | GPIO4_IO28 | U4 | 蓝牙唤醒信号 | 输入/输出 | 1.8V | CCMSRCGPCMIX_CLKO3,FLEXIO2_FLEXIO28,GPIO4_IO28 |
| B43 | CCM_CLKO4 | DSI_RESET | GPIO4_IO29 | V4 | DSI复位信号 | 输入/输出 | 1.8V | CCMSRCGPCMIX_CLKO4,FLEXIO2_FLEXIO29,GPIO4_IO29 |
| B44 | GND |  |  |  | 接地 |  |  |  |
| B45 | UART5_TX | JTAG_TDO | GPIO3_IO31 | Y2 | UART5/JTAG发送信号线 | 输入/输出 | 1.8V | JTAG_MUX_TDO,MQS2_RIGHT,CAN2_RX,FLEXIO1_FLEXIO31,GPIO3_IO31,LPUART5_TX(通过拨动开发板上SW2开关选择使用JTAG还是UART5) |
| B46 | UART5_CTS | JTAG_TCK | GPIO3_IO30 | Y1 | UART5/JTAG时钟信号线 | 输入/输出 | 1.8V | JTAG_MUX_TCK,FLEXIO1_FLEXIO30,GPIO3_IO30,LPUART5_CTS_B(通过拨动开发板上SW2开关选择使用JTAG还是UART5) |
| B47 | UART5_RTS | JTAG_TMS | GPIO3_IO29 | W2 | UART5/JTAG状态信号线 | 输入/输出 | 1.8V | JTAG_MUX_TMS,FLEXIO2_FLEXIO31,GPIO3_IO29,LPUART5_RTS_B(通过拨动开发板上SW2开关选择使用JTAG还是UART5) |
| B48 | UART5_RX | JTAG_TDI | GPIO3_IO28 | W1 | UART5/JTAG接收信号线 | 输入/输出 | 1.8V | JTAG_MUX_TDI,MQS2_LEFT,CAN2_TX,FLEXIO2_FLEXIO30,GPIO3_IO28,LPUART5_RX(通过拨动开发板上SW2开关选择使用JTAG还是UART5) |
| B49 | GND |  |  |  | 接地 |  |  |  |
| B50 | GND |  |  |  | 接地 |  |  |  |
| B51 | GND |  |  |  | 接地 |  |  |  |
| B52 | ENET2_RXC | 10/100/1000M ENET2 | GPIO4_IO23 | AA3 | 千兆网口2_接收端时钟信号 | 输入/输出 | 1.8V | ENET1_RGMII_RXC,ENET1_RX_ER,SAI2_TX_DATA01,FLEXIO2_FLEXIO23,GPIO4_IO23 |
| B53 | ENET2_RX_CTL | 10/100/1000M ENET2 | GPIO4_IO22 | Y4 | 千兆网口2_接收端使能信号 | 输入/输出 | 1.8V | ENET1_RGMII_RX_CTL,LPUART4_DSR_B,SAI2_TX_DATA00,FLEXIO2_FLEXIO22,GPIO4_IO22 |
| B54 | ENET2_RD0 | 10/100/1000M ENET2 | GPIO4_IO24 | AA4 | 千兆网口2_接收端数据线0 | 输入/输出 | 1.8V | ENET1_RGMII_RD0,LPUART4_RX,SAI2_TX_DATA02,FLEXIO2_FLEXIO24,GPIO4_IO24 |
| B55 | ENET2_RD1 | 10/100/1000M ENET2 | GPIO4_IO25 | Y5 | 千兆网口2_接收端数据线1 | 输入/输出 | 1.8V | ENET1_RGMII_RD1,SPDIF_IN,SAI2_TX_DATA03,FLEXIO2_FLEXIO25,GPIO4_IO25 |
| B56 | ENET2_RD2 | 10/100/1000M ENET2 | GPIO4_IO26 | AA5 | 千兆网口2_接收端数据线2 | 输入/输出 | 1.8V | ENET1_RGMII_RD2,LPUART4_CTS_B,SAI2_MCLK,MQS2_RIGHT,FLEXIO2_FLEXIO26,GPIO4_IO26 |
| B57 | ENET2_RD3 | 10/100/1000M ENET2 | GPIO4_IO27 | Y6 | 千兆网口2_接收端数据线3 | 输入/输出 | 1.8V | ENET1_RGMII_RD3,SPDIF_OUT,SPDIF_IN,MQS2_LEFT,FLEXIO2_FLEXIO27,GPIO4_IO27 |
| B58 | GND | 10/100/1000M ENET2 |  |  | 接地 |  |  |  |
| B59 | ENET2_TXC | 10/100/1000M ENET2 | GPIO4_IO21 | U6 | 千兆网口2_发送端时钟信号 | 输入/输出 | 1.8V | ENET1_RGMII_TXC,ENET1_TX_ER,SAI2_TX_BCLK,FLEXIO2_FLEXIO21,GPIO4_IO21 |
| B60 | ENET2_TX_CTL | 10/100/1000M ENET2 | GPIO4_IO20 | V6 | 千兆网口2_发送端使能信号 | 输入/输出 | 1.8V | ENET1_RGMII_TX_CTL,LPUART4_DTR_B,SAI2_TX_SYNC,FLEXIO2_FLEXIO20,GPIO4_IO20 |
| B61 | ENET2_TD0 | 10/100/1000M ENET2 | GPIO4_IO19 | T8 | 千兆网口2_发送端数据线0 | 输入/输出 | 1.8V | ENET1_RGMII_TD0,LPUART4_TX,SAI2_RX_DATA03,FLEXIO2_FLEXIO19,GPIO4_IO19 |
| B62 | ENET2_TD1 | 10/100/1000M ENET2 | GPIO4_IO18 | U8 | 千兆网口2_发送端数据线1 | 输入/输出 | 1.8V | ENET1_RGMII_TD1,LPUART4_RTS_B,SAI2_RX_DATA02,FLEXIO2_FLEXIO18,GPIO4_IO18 |
| B63 | ENET2_TD2 | 10/100/1000M ENET2 | GPIO4_IO17 | V8 | 千兆网口2_发送端数据线2 | 输入/输出 | 1.8V | ENET1_RGMII_TD2,ENET1_TX_CLK,SAI2_RX_DATA01,FLEXIO2_FLEXIO17,GPIO4_IO17 |
| B64 | ENET2_TD3 | 10/100/1000M ENET2 | GPIO4_IO16 | T10 | 千兆网口2_发送端数据线3 | 输入/输出 | 1.8V | ENET1_RGMII_TD3,SAI2_RX_DATA00,FLEXIO2_FLEXIO16,GPIO4_IO16 |
| B65 | GND | 10/100/1000M ENET2 |  |  | 接地 |  |  |  |
| B66 | ENET2_MDIO | 10/100/1000M ENET2 | GPIO4_IO15 | AA6 | 千兆网口2_MAC管理接口数据线 | 输入/输出 | 1.8V | ENET1_MDIO,LPUART4_RIN_B,SAI2_RX_BCLK,FLEXIO2_FLEXIO15,GPIO4_IO15 |
| B67 | ENET2_MDC | 10/100/1000M ENET2 | GPIO4_IO14 | Y7 | 千兆网口2_MAC管理接口时钟线 | 输入/输出 | 1.8V | ENET1_MDC,LPUART4_DCB_B,SAI2_RX_SYNC,FLEXIO2_FLEXIO14,GPIO4_IO14 |
| B68 | GND |  |  |  | 接地 |  |  |  |
| B69 | ENET1_RXC | 10/100/1000M ENET1 | GPIO4_IO09 | AA7 | 千兆网口1_接收端时钟信号 | 输入/输出 | 1.8V | CCM_ENET_QOS_CLOCK_GENERATE_RX_CLK,ENET_QOS_RX_ER,FLEXIO2_FLEXIO09,GPIO4_IO09 |
| B70 | ENET1_RX_CTL | 10/100/1000M ENET1 | GPIO4_IO08 | Y8 | 千兆网口1_接收端使能信号 | 输入/输出 | 1.8V | ENET_QOS_RGMII_RX_CTL,LPUART3_DSR_B,HSIOMIX_OTG_PWR2,FLEXIO2_FLEXIO08,GPIO4_IO08 |
| B71 | ENET1_RD0 | 10/100/1000M ENET1 | GPIO4_IO10 | AA8 | 千兆网口1_接收端数据线0 | 输入/输出 | 1.8V | ENET_QOS_RGMII_RD0,LPUART3_RX,FLEXIO2_FLEXIO10,GPIO4_IO10 |
| B72 | ENET1_RD1 | 10/100/1000M ENET1 | GPIO4_IO11 | Y9 | 千兆网口1_接收端数据线1 | 输入/输出 | 1.8V | ENET_QOS_RGMII_RD1,LPUART3_CTS_B,LPTMR2_ALT1,FLEXIO2_FLEXIO11,GPIO4_IO11 |
| B73 | ENET1_RD2 | 10/100/1000M ENET1 | GPIO4_IO12 | AA9 | 千兆网口1_接收端数据线2 | 输入/输出 | 1.8V | ENET_QOS_RGMII_RD2,LPTMR2_ALT2,FLEXIO2_FLEXIO12,GPIO4_IO12 |
| B74 | ENET1_RD3 | 10/100/1000M ENET1 | GPIO4_IO13 | Y10 | 千兆网口1_接收端数据线3 | 输入/输出 | 1.8V | ENET_QOS_RGMII_RD3,LPTMR2_ALT3,FLEXIO2_FLEXIO13,GPIO4_IO13 |
| B75 | GND | 10/100/1000M ENET1 |  |  | 接地 |  |  |  |
| B76 | ENET1_TXC | 10/100/1000M ENET1 | GPIO4_IO07 | U10 | 千兆网口1_发送端时钟信号 | 输入/输出 | 1.8V | CCM_ENET_QOS_CLOCK_GENERATE_TX_CLK，ENET_QOS_TX_ER,FLEXIO2_FLEXIO07,GPIO4_IO07 |
| B77 | ENET1_TX_CTL | 10/100/1000M ENET1 | GPIO4_IO06 | V10 | 千兆网口1_发送端使能信号 | 输入/输出 | 1.8V | ENET_QOS_RGMII_TX_CTL,LPUART3_DTR_B,FLEXIO2_FLEXIO06,GPIO4_IO06 |
| B78 | ENET1_TD0 | 10/100/1000M ENET1 | GPIO4_IO05 | W11 | 千兆网口1_发送端数据线0 | 输入/输出 | 1.8V | ENET_QOS_RGMII_TD0,LPUART3_TX,FLEXIO2_FLEXIO05,GPIO4_IO05 |
| B79 | ENET1_TD1 | 10/100/1000M ENET1 | GPIO4_IO04 | T12 | 千兆网口1_发送端数据线1 | 输入/输出 | 1.8V | ENET_QOS_RGMII_TD1,LPUART3_RTS_B,I3C2_PUR,HSIOMIX_OTG_OC1,FLEXIO2_FLEXIO04,GPIO4_IO04,I3C2_PUR_B |
| B80 | ENET1_TD2 | 10/100/1000M ENET1 | GPIO4_IO03 | U12 | 千兆网口1_发送端数据线2 | 输入/输出 | 1.8V | ENET_QOS_RGMII_TD2,CCM_ENET_QOS_CLOCK_GENERATE_REF_CLK,CAN2_RX,HSIOMIX_OTG_OC2,FLEXIO2_FLEXIO03,GPIO4_IO03 |
| B81 | ENET1_TD3 | 10/100/1000M ENET1 | GPIO4_IO02 | V12 | 千兆网口1_发送端数据线3 | 输入/输出 | 1.8V | ENET_QOS_RGMII_TD3,CAN2_TX,HSIOMIX_OTG_ID2,FLEXIO2_FLEXIO02,GPIO4_IO02 |
| B82 | GND | 10/100/1000M ENET1 |  |  | 接地 |  |  |  |
| B83 | ENET1_MDIO | 10/100/1000M ENET1 | GPIO4_IO01 | AA10 | 千兆网口1_MAC管理接口数据线 | 输入/输出 | 1.8V | ENET_QOS_MDIO,LPUART3_RIN_B,I3C2_SDA,HSIOMIX_OTG_PWR1,FLEXIO2_FLEXIO01,GPIO4_IO01 |
| B84 | ENET1_MDC | 10/100/1000M ENET1 | GPIO4_IO00 | AA11 | 千兆网口1_MAC管理接口时钟线 | 输入/输出 | 1.8V | ENET_QOS_MDC,LPUART3_DCB_B,I3C2_SCL,HSIOMIX_OTG_ID1,FLEXIO2_FLEXIO00,GPIO4_IO00 |
| B85 | GND |  |  |  | 接地 |  |  |  |
| B86 | SD2_CD | TF Card | GPIO3_IO00 | Y17 | TF卡检测信号 | 输入/输出 | 3.3V/1.8V | USDHC2_CD_B,ENET_QOS_1588_EVENT0_IN,I3C2_SCL,FLEXIO1_FLEXIO00,GPIO3_IO00 |
| B87 | SD2_DATA1 | TF Card | GPIO3_IO04 | AA18 | TF卡数据信号线1 | 输入/输出 | 3.3V/1.8V | USDHC2_DATA1,ENET1_1588_EVENT1_IN,CAN2_RX,FLEXIO1_FLEXIO04,GPIO3_IO04 |
| B88 | SD2_DATA0 | TF Card | GPIO3_IO03 | Y18 | TF卡数据信号线0 | 输入/输出 | 3.3V/1.8V | USDHC2_DATA0,ENET1_1588_EVENT0_OUT,CAN2_TX,FLEXIO1_FLEXIO03,GPIO3_IO03,CCMSRCGPCMIX_OBSERVE2 |
| B89 | SD2_CLK | TF Card | GPIO3_IO01 | AA19 | TF卡时钟信号线 | 输入/输出 | 3.3V/1.8V | USDHC2_CLK,ENET_QOS_1588_EVENT0_OUT,I3C2_SDA,FLEXIO1_FLEXIO01,GPIO3_IO01 |
| B90 | SD2_CMD | TF Card | GPIO3_IO02 | Y19 | TF卡命令信号线 | 输入/输出 | 3.3V/1.8V | USDHC2_CMD,ENET1_1588_EVENT0_IN,I3C2_PUR,I3C2_PUR_B,FLEXIO1_FLEXIO02,GPIO3_IO02,CCMSRCGPCMIX_OBSERVE1 |
| B91 | SD2_DATA3 | TF Card | GPIO3_IO06 | AA20 | TF卡数据信号线3 | 输入/输出 | 3.3V/1.8V | USDHC2_DATA3,LPTMR2_ALT1,MQS2_LEFT,FLEXIO1_FLEXIO06,GPIO3_IO06 |
| B92 | SD2_DATA2 | TF Card | GPIO3_IO05 | Y20 | TF卡数据信号线2 | 输入/输出 | 3.3V/1.8V | USDHC2_DATA2,ENET1_1588_EVENT1_OUT,MQS2_RIGHT,FLEXIO1_FLEXIO05,GPIO3_IO05 |
| B93 | GND |  |  |  | 接地 |  |  |  |
| B94 | GND |  |  |  | 接地 |  |  |  |
| B95 | GND |  |  |  | 接地 |  |  |  |
| B96 | GND |  |  |  | 接地 |  |  |  |
| B97 | VCC_5V | VCC_IN |  |  | 核心板输入电源接口 | 电源 |  |  |
| B98 | VCC_5V | VCC_IN |  |  | 核心板输入电源接口 | 电源 |  |  |
| B99 | VCC_5V | VCC_IN |  |  | 核心板输入电源接口 | 电源 |  |  |
| B100 | VCC_5V | VCC_IN |  |  | 核心板输入电源接口 | 电源 |  |  |

