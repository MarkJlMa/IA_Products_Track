# EtherCAT 开源协议栈总结

## 1. EtherCAT 简介

EtherCAT（Ethernet for Control Automation Technology）是德国 Beckhoff 提出的实时工业以太网协议。它以“处理即转发”的方式实现低延迟、高精度、高同步性的现场总线通讯，广泛应用于伺服控制、运动控制、机器人、PLC、工业机器人等领域。

EtherCAT 协议栈通常分为两个部分：

- 主站（Master）协议栈：负责调度、帧生成、同步和实时数据管理。
- 从站（Slave）协议栈：实现从站设备的帧解析、过程数据对象（PDO）映射、同步管理等。

在开源社区，EtherCAT 常见的开源协议栈主要集中在 Linux 平台，涵盖 PC 端 EtherCAT 主站、嵌入式从站以及工具链。

## 2. 主流开源 EtherCAT 主站协议栈

### 2.1 SOEM（Simple Open EtherCAT Master）

- 官方地址：`https://github.com/OpenEtherCATsociety/SOEM`
- 许可证：GPLv2
- 语言：C
- 平台：Linux、Windows、RTOS、嵌入式 MCU

#### 特点

- 轻量、可移植，适合嵌入式平台和实时系统。
- 支持基本 EtherCAT 主站功能：发现拓扑、PDO 映射、SM/FOE、同步（DC）等。
- 支持基于原始套接字（raw socket）和驱动层访问。
- 社区活跃，Open EtherCAT Society 官方维护。

#### 适用场景

- 需要开源 EtherCAT 主站实现的工业 PC 或嵌入式控制器。
- 以太网硬件支持原始帧发送/接收的系统。
- 开发自定义 EtherCAT 控制系统或实验平台。

### 2.2 IgH EtherCAT Master

- 官方地址：`https://github.com/etherlab/ethercat-master`
- 许可证：GPLv2
- 语言：C
- 平台：Linux（主要为实时 Linux，如 PREEMPT_RT）

#### 特点

- 基于 RTLinux/RTX 和 POSIX 环境，适合实时性能要求高的控制系统。
- 拥有成熟的驱动程序与用户空间接口。
- 支持 Distributed Clocks（DC）同步、高精度时序、过程数据实时交换。

#### 适用场景

- 需要在标准 Linux 平台上部署实时 EtherCAT 主站的系统。
- 高端自动化控制、运动控制、机器人控制等。

### 2.3 SOES（Simple Open EtherCAT Slave）

- 官方地址：`https://github.com/OpenEtherCATsociety/SOES`
- 许可证：GPLv2
- 语言：C
- 平台：STM32、ARM、PIC 等多种 MCU

#### 特点

- 轻量从站协议栈，适用于嵌入式设备实现 EtherCAT 从站功能。
- 提供从站对象字典、PDO/SDO 支持。
- 可与硬件网卡或 FPGA 接口结合，快速构建 EtherCAT 从站设备。

#### 适用场景

- 需要实现 EtherCAT 从站功能的传感器、I/O 模块、驱动器和终端设备。
- 嵌入式 EtherCAT 设备原型开发。

## 3. 其他开源 EtherCAT 协议栈与工具

### 3.1 IgH Open EtherCAT Slave Stack

- 官方地址：`https://github.com/etherlab/ethercat-slave`
- 许可证：GPLv2
- 语言：C
- 平台：嵌入式 MCU、FPGA、自定义硬件

#### 特点

- 适用于定制 EtherCAT 从站硬件，实现标准从站状态机。
- 通常与 EtherCAT 物理接口/硬件控制器结合使用。

### 3.2 EtherLab 项目套件

- 官方地址：`https://www.etherlab.org/`
- 项目包括 Linux EtherCAT Master、Slave Stack、开发工具、驱动。

#### 特点

- 成熟的 EtherCAT 生态系统，包含多种 Linux 实时扩展支持。
- 提供文档、示例和社区支持。

### 3.3 Open EtherCAT Society 资源

- 官方地址：`https://www.ethercatsociety.org/`
- 提供 EtherCAT 标准、认证、开发者社区和开源项目入口。

## 4. 主要协议栈比较

| 项目 | 类型 | 平台 | 许可证 | 适用场景 |
|---|---|---|---|---|
| SOEM | 主站 | Linux/Windows/嵌入式 | GPLv2 | 轻量主站、嵌入式控制器、实验系统 |
| IgH EtherCAT Master | 主站 | Linux（RT） | GPLv2 | 实时控制、高精度同步系统 |
| SOES | 从站 | MCU/嵌入式 | GPLv2 | 嵌入式从站设备、传感器/执行器 |
| IgH EtherCAT Slave | 从站 | 嵌入式/FPGA | GPLv2 | 自定义从站硬件 |

## 5. 选型建议

- 如果目标是快速搭建 EtherCAT 主站并进行工程验证，推荐使用 `SOEM`。
- 如果需要在 Linux 上实现高实时性能主站，推荐 `IgH EtherCAT Master`。
- 如果要实现嵌入式 EtherCAT 从站，推荐 `SOES` 或 `IgH EtherCAT Slave Stack`。
- 在商业项目中，注意 GPLv2 许可证对整体软件发布的要求，尤其是与专有代码混合时。

## 6. 参考资料

- Open EtherCAT Society GitHub: https://github.com/OpenEtherCATsociety
- EtherLab GitHub: https://github.com/etherlab
- EtherCAT 官方网站: https://www.ethercatsociety.org/
- EtherCAT 技术手册与规范文档
