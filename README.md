# STM32-Full-Stack-Embedded-Development
基于STM32F10x系列MCU的嵌入式全栈学习仓库，覆盖GPIO、TIM、ADC、DMA、USART、I2C/SPI通信、RTC、低功耗、看门狗、FLASH等核心外设驱动开发，包含MPU6050、W25Q64等常用传感器/存储芯片的软硬件实现，配套完整学习笔记与可运行工程。
# STM32F10x-AIoT-Embedded-Learning

<div align="center">
<img src="https://img.shields.io/badge/STM32-F10x-blue?style=for-the-badge&logo=stmicroelectronics" alt="STM32">
<img src="https://img.shields.io/badge/Embedded-C-orange?style=for-the-badge&logo=c" alt="C">
<img src="https://img.shields.io/badge/AIoT-Embedded-green?style=for-the-badge&logo=iot" alt="AIoT">
<img src="https://img.shields.io/badge/Keil-MDK-yellow?style=for-the-badge&logo=keil" alt="Keil MDK">
</div>

## 🎯 项目简介
本仓库是基于**STM32F103系列MCU**的嵌入式全栈学习与实践项目，完整覆盖STM32核心外设驱动、通信协议、传感器开发、低功耗设计等AIoT嵌入式开发核心技能，包含可直接运行的工程源码、配套详细学习笔记，是从入门到精通STM32开发的完整实践体系。

## 📂 仓库结构
```plantext
├── Note/                          # 完整学习笔记（PDF/HTML双版本，HTML含实验动图）
│   ├── STM32全模块学习笔记.pdf     # 静态离线版，适合归档查阅
│   └── STM32全模块学习笔记.html    # 动态交互版，含实验演示动图（推荐）
└── STM32Projects/                      # 可直接编译运行的STM32工程源码（标准库V3.5.0）
    ├── 1-基础工程与工具
    │   ├── 1-1 接线图/             # 所有实验硬件接线参考
    │   ├── 1-2 keilkill批处理/     # Keil工程清理脚本
    │   ├── 1-3 Delay函数模块/      # 延时函数通用模块
    │   ├── 1-4 OLED驱动函数模块/   # OLED显示屏通用驱动
    │   └── 2-1 STM32工程模板/      # 标准库工程初始化模板
    ├── 3-GPIO输入输出实验
    │   ├── 3-1 LED闪烁/
    │   ├── 3-2 LED流水灯/
    │   ├── 3-3 蜂鸣器/
    │   ├── 3-4 按键控制LED/
    │   └── 3-5 光敏传感器控制蜂鸣器/
    ├── 4-OLED显示实验
    │   └── 4-1 OLED显示屏/
    ├── 5-EXTI外部中断实验
    │   ├── 5-1 对射式红外传感器计次/
    │   └── 5-2 旋转编码器计次/
    ├── 6-TIM定时器实验
    │   ├── 6-1 定时器定时中断/
    │   ├── 6-2 定时器外部时钟/
    │   ├── 6-3 PWM驱动LED呼吸灯/
    │   ├── 6-4 PWM驱动舵机/
    │   ├── 6-5 PWM驱动直流电机/
    │   ├── 6-6 输入捕获模式测频率/
    │   ├── 6-7 PWMI模式测频率占空比/
    │   └── 6-8 编码器接口测速/
    ├── 7-ADC模数转换实验
    │   ├── 7-1 AD单通道/
    │   └── 7-2 AD多通道/
    ├── 8-DMA数据转运实验
    │   ├── 8-1 DMA数据转运/
    │   └── 8-2 DMA+AD多通道/
    ├── 9-USART串口通信实验
    │   ├── 9-1 串口发送/
    │   ├── 9-2 串口发送+接收/
    │   ├── 9-3 串口收发HEX数据包/
    │   └── 9-4 串口收发文本数据包/
    ├── 10-I2C通信与MPU6050实验
    │   ├── 10-1 软件I2C读写MPU6050/
    │   └── 10-2 硬件I2C读写MPU6050/
    ├── 11-SPI通信与W25Q64实验
    │   ├── 11-1 软件SPI读写W25Q64/
    │   └── 11-2 硬件SPI读写W25Q64/
    ├── 12-BKP与RTC实时时钟实验
    │   ├── 12-1 读写备份寄存器/
    │   └── 12-2 实时时钟/
    ├── 13-PWR电源与低功耗实验
    │   ├── 13-1 修改主频/
    │   ├── 13-2 睡眠模式+串口发送+接收/
    │   ├── 13-3 停止模式+对射式红外传感器计次/
    │   └── 13-4 待机模式+实时时钟/
    ├── 14-WDG看门狗实验
    │   ├── 14-1 独立看门狗/
    │   └── 14-2 窗口看门狗/
    ├── 15-FLASH存储实验
    │   ├── 15-1 读写内部FLASH/
    │   └── 15-2 读取芯片ID/
    ├── STM32F10x_StdPeriph_Lib_V3.5.0/  # STM32F10x标准库源码
    └── 工具软件/                        # 配套开发调试工具
```


## ✨ 核心内容覆盖
### 🔹 基础外设与输入输出
- GPIO输入输出：LED控制、蜂鸣器驱动、按键检测、光敏传感器应用
- EXTI外部中断：对射式红外传感器计次、旋转编码器计次
- TIM定时器：定时中断、外部时钟、PWM输出（呼吸灯/舵机/电机驱动）、输入捕获（频率/占空比测量）、编码器接口测速

### 🔹 数据采集与传输
- ADC模数转换：单/多通道AD采集、DMA+AD多通道数据转运
- USART串口通信：串口收发、HEX/文本数据包解析
- I2C通信：软件/硬件I2C实现、MPU6050六轴姿态传感器驱动
- SPI通信：软件/硬件SPI实现、W25Q64 FLASH存储芯片驱动

### 🔹 系统与低功耗设计
- RTC实时时钟：Unix时间戳、BKP备份寄存器、RTC时钟配置
- PWR电源管理：主频修改、睡眠/停止/待机低功耗模式实践
- WDG看门狗：独立看门狗、窗口看门狗应用
- FLASH闪存：内部FLASH读写、芯片ID读取

### 🔹 配套学习笔记
笔记完整覆盖上述所有模块，包含**原理详解、代码逐行注释、实验步骤、接线说明**，HTML版本支持实验动图展示，直观呈现实验效果，同时提供API函数总览，方便快速查阅。

## 🛠️ 开发环境
- **MCU**：STM32F103C8T6
- **IDE**：Keil MDK-ARM v5
- **库版本**：STM32F10x Standard Peripherals Library V3.5.0
- **调试工具**：ST-Link/V2

## 🚀 快速开始
1. 克隆仓库到本地：`git clone https://github.com/YY-Z-Z/STM32F10x-AIoT-Embedded-Learning.git`
2. 打开`STM32Projects/`下对应实验工程，使用Keil MDK编译
3. 参考`Note/`中的笔记，查看原理说明
4. 烧录程序到STM32开发板，运行实验

## 📌 项目亮点
- ✅ **全栈覆盖**：从底层外设到通信协议，完整覆盖AIoT嵌入式开发核心技能
- ✅ **工程可运行**：所有源码均经过实际测试，可直接编译烧录运行
- ✅ **笔记体系化**：配套完整学习笔记，原理+实践结合，适合学习与复盘
- ✅ **模块化设计**：驱动代码模块化，可直接复用至实际项目
- ✅ **AIoT场景适配**：包含传感器、通信、低功耗等AIoT产品核心技术点
