# Profinet 开源协议栈总结

## 1. Profinet 简介

Profinet 是由 Profibus & Profinet International（PI）制定的工业以太网标准，旨在实现自动化系统中实时、确定性的数据交换。它分为三个类别：RT（实时）、IRT（等时实时）和 NRT（非实时），广泛用于 PLC、传感器、执行器、运动控制与工厂总线集成。

Profinet 协议栈可以分为两类：

- 控制器（Controller）/主站协议栈：实现设备发现、连接管理、IO 数据交换和实时调度。
- 设备（Device）/从站协议栈：实现设备描述、参数化、IO 数据映射以及实时通信。

开源社区的 Profinet 实现主要集中在 Linux 平台和嵌入式设备上，通常基于实时 Linux 或专用网络处理器。

## 2. 主流开源 Profinet 主站协议栈

### 2.1 PROFIdrive Open Source 实现

- 官方地址：`https://github.com/`（社区开源项目，需具体搜索）
- 许可证：多为 Apache 2.0 / MIT / GPL（视实现具体项目而定）
- 语言：C/C++
- 平台：Linux、嵌入式系统

#### 特点

- 面向 Profinet IO 设备与驱动器应用。
- 支持设备发现、连接管理、实时 IO 交换。
- 常用于基于标准以太网控制器或专用硬件的实现。

#### 适用场景

- 需要在开源环境中验证 Profinet IO 控制器功能。
- 工业机器人、变频器、伺服驱动器等控制器开发。

### 2.2 PROFINET IO Controller on Linux

- 参考地址：`https://github.com/siemens/profinet-linux`（示例仓库）
- 许可证：多为 Apache 2.0 或 MIT
- 语言：C
- 平台：Linux（包括实时内核）

#### 特点

- 依赖 Linux 协议栈与实时扩展进行 IO 数据交换。
- 支持 Profinet 控制器与设备之间的连接管理和周期通信。

#### 适用场景

- 工业 PC 或嵌入式 Linux 控制器。
- 需要与 Profinet 设备互操作的自定义控制器。

## 3. 主流开源 Profinet 从站协议栈

### 3.1 OpenIEC61850 Profinet 设备实现

- 官方地址：`https://github.com/mz-automation/openiec61850`（包含部分 Profinet 集成组件）
- 许可证：Apache 2.0
- 语言：C/C++
- 平台：Linux、嵌入式

#### 特点

- 重点是工业协议栈与网络功能集成。
- 可用于设备参数化与 IO 数据映射。

#### 适用场景

- 需要将 Profinet 设备与 IEC 61850/IEC 61131 系统集成的应用场景。

### 3.2 Open-Source Profinet Device Stack

- 官方地址：`https://github.com/`（社区实现，需检索具体项目）
- 许可证：GPL、Apache 2.0 或 MIT 等
- 语言：C
- 平台：ARM、x86、专用以太网 SoC

#### 特点

- 以设备对象模型为核心，实现 GSDML、IO 交换、诊断等功能。
- 常结合工业以太网 MAC 硬件或 FPGA 来处理实时帧。

#### 适用场景

- 需要快速开发 Profinet 从站设备的传感器、执行器、IO 模块。
- 嵌入式设备、现场总线网关。

## 4. 其他开源资源与实现

### 4.1 Open Source 工具与库

- `libprofinet` / `libpn`：一些社区项目提供基础 Profinet 报文解析与报文生成库。
- `Wireshark` Profinet dissector：用于抓包分析 Profinet 通信。

### 4.2 厂商开源参考

- Siemens、Phoenix Contact、Hilscher 等厂商在其生态中提供了部分开源示例或协议参考。
- 这些资源通常附带设备配置文件、GSDML 模板和参考实现。

## 5. 主要协议栈比较

| 项目 | 类型 | 平台 | 许可证 | 适用场景 |
|---|---|---|---|---|
| Profinet Linux Controller 示例 | 主站 | Linux/RT Linux | Apache/MIT | 自定义控制器、工业 PC |
| Open Source Profinet Device Stack | 从站 | 嵌入式 ARM/x86 | GPL/Apache | 设备开发、IO 模块 |
| OpenIEC61850 Profinet 集成 | 设备/系统 | Linux/嵌入式 | Apache 2.0 | 协议集成、网络设备 |

## 6. 选型建议

- 若要快速搭建 Profinet 控制器原型，可优先寻找 Apache 2.0 或 MIT 开源实现。
- 若要实现可商用设备，建议从厂商参考实现入手，结合开源库做验证和测试。
- 需关注 Profinet IRT 是否必须，若需要高性能同步则应选择支持 IRT 或专用硬件的实现。
- 在商业发布中，注意协议栈许可证与 GSDML 配置文件的使用约束。

## 7. 参考资料

- PI Profinet 官方网站: https://www.profibus.com/
- Profinet 标准与规范文档
- Wireshark Profinet 解码器
- Open Source Profinet 项目仓库搜索
