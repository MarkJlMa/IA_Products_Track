# OCPP 开源协议栈汇总

## 概述

OCPP (Open Charge Point Protocol) 是开放充电点协议，由开放充电联盟 (OCA, Open Charge Alliance) 制定，用于电动汽车充电桩与中央管理系统之间的通信。目前主流版本为 OCPP 1.6 和 OCPP 2.0.1。

---

## 协议版本对比

| 特性 | OCPP 1.6 | OCPP 2.0.1 |
|------|----------|------------|
| 通信方式 | SOAP (JSON over WebSocket 可选) | JSON over WebSocket |
| 安全性 | 基础安全 | 内置安全配置文件 (TLS, 证书管理) |
| 智能充电 | 基本支持 | 增强的智能充电功能 |
| ISO 15118 | 不支持 | 支持 PnC (Plug & Charge) |
| 交易管理 | 简单 | 完善的交易和计费机制 |
| 状态管理 | 基础 | 更细粒度的状态监控 |

---

## 开源实现汇总

### Java 实现

#### 1. ChargeTimeEU / Java-OCA-OCPP
- **GitHub**: https://github.com/ChargeTimeEU/Java-OCA-OCPP
- **支持版本**: OCPP 1.6
- **协议**: MIT License
- **特点**:
  - 支持 JSON 和 SOAP 两种通信方式
  - 可作为充电桩 (Charge Point) 或中央系统 (Central System) 使用
  - 基于 WebSocket 实现
  - 社区活跃，文档完善
- **适用场景**: 充电桩开发、中央管理系统开发

#### 2. ChargeTimeEU / OCA-OCPP-Java
- **GitHub**: https://github.com/ChargeTimeEU/OCA-OCPP-Java
- **支持版本**: OCPP 2.0.1
- **协议**: MIT License
- **特点**:
  - 支持 OCPP 2.0.1 最新特性
  - 支持 ISO 15118 PnC
  - 完善的安全配置文件
- **适用场景**: 新一代充电桩开发

#### 3. SteVe
- **GitHub**: https://github.com/RWTH-i5-IDSG/steve
- **支持版本**: OCPP 1.6 (主要)
- **协议**: GPLv3
- **特点**:
  - 完整的中央管理系统 (CSMS) 实现
  - Web 管理界面
  - 支持多种数据库 (MySQL, MariaDB, PostgreSQL)
  - 生产级稳定性
- **适用场景**: 充电网络运营商、测试环境

---

### Python 实现

#### 1. The Mobility House / ocpp
- **GitHub**: https://github.com/mobilityhouse/ocpp
- **支持版本**: OCPP 1.6, OCPP 2.0.1
- **协议**: MIT License
- **特点**:
  - 纯 Python 实现
  - 异步架构 (基于 asyncio)
  - 支持 JSON over WebSocket
  - 类型注解完善
  - 可扩展性强
- **适用场景**: 快速原型开发、测试工具、嵌入式系统

#### 2. ocpp-go (Go 语言)
- **GitHub**: https://github.com/lorenzodonini/ocpp-go
- **支持版本**: OCPP 1.6, OCPP 2.0.1
- **协议**: MPL-2.0
- **特点**:
  - Go 语言实现
  - 高性能、低资源占用
  - 支持充电桩和中央系统角色
  - 完善的测试覆盖
- **适用场景**: 云原生部署、边缘计算

---

### C/C++ 实现

#### 1. NewMotion / OCPP
- **GitHub**: https://github.com/NewMotion/ocpp
- **支持版本**: OCPP 1.6
- **协议**: Apache 2.0
- **特点**:
  - C++ 实现
  - 嵌入式友好
  - 低资源占用
- **适用场景**: 嵌入式充电桩控制器

#### 2. EVerest
- **官网**: https://everest.li/
- **GitHub**: https://github.com/EVerest/everest
- **支持版本**: OCPP 1.6, OCPP 2.0.1
- **协议**: Apache 2.0 / GPLv3
- **特点**:
  - LF Energy 项目
  - 模块化架构
  - 支持多种充电标准
  - 硬件抽象层
- **适用场景**: 充电桩完整解决方案

---

### Rust 实现

#### 1. ocpp-rs
- **GitHub**: https://github.com/tuxedo/ocpp-rs
- **支持版本**: OCPP 2.0.1
- **协议**: MIT/Apache 2.0
- **特点**:
  - 内存安全
  - 高性能
  - 适合嵌入式场景
- **适用场景**: 安全关键型充电系统

---

### .NET / C# 实现

#### 1. OCPP.NET
- **GitHub**: https://github.com/derwish-pro/OCPP.NET
- **支持版本**: OCPP 1.6
- **协议**: MIT License
- **特点**:
  - .NET Standard 支持
  - 易于集成到 Windows 环境
- **适用场景**: Windows 平台开发

---

## 选型建议

| 场景 | 推荐方案 |
|------|----------|
| 快速原型/测试 | Python (mobilityhouse/ocpp) |
| 企业级中央系统 | Java (SteVe) |
| 嵌入式充电桩 | C++ (NewMotion) 或 EVerest |
| 云原生/微服务 | Go (ocpp-go) |
| 安全关键系统 | Rust (ocpp-rs) |
| 新项目 (OCPP 2.0.1) | Java (OCA-OCPP-Java) 或 Python (mobilityhouse) |

---

## 关键技术要点

### 通信架构
```
┌─────────────┐                    ┌─────────────────┐
│  充电桩      │◄─── WebSocket ───►│  中央管理系统    │
│ (Charge     │    (JSON/SOAP)     │ (Central System │
│  Point)     │                    │  / CSMS)        │
└─────────────┘                    └─────────────────┘
```

### OCPP 2.0.1 主要消息类型
- **BootNotification**: 充电桩启动通知
- **Heartbeat**: 心跳保活
- **StatusNotification**: 状态更新
- **Authorize**: 授权请求
- **StartTransaction/StopTransaction**: 交易管理
- **MeterValues**: 电量数据上报
- **RemoteStartTransaction/RemoteStopTransaction**: 远程控制

### 安全配置文件 (OCPP 2.0.1)
1. **No Security**: 无安全 (仅测试用)
2. **Basic Authentication**: 基础认证
3. **TLS with Client Certificates**: TLS + 客户端证书
4. **TLS with Mutual Authentication**: 双向 TLS 认证

---

## 参考资源

- **开放充电联盟官网**: https://www.openchargealliance.org/
- **OCPP 规范下载**: https://www.openchargealliance.org/protocols/ocpp-201/
- **OCPP 测试工具**: https://github.com/ChargeTimeEU/OCA-OCPP-Java (含测试框架)
- **EVerest 项目**: https://everest.li/

---

## 许可证说明

| 项目 | 许可证 | 商业使用 |
|------|--------|----------|
| Java-OCA-OCPP | MIT | ✅ |
| mobilityhouse/ocpp | MIT | ✅ |
| ocpp-go | MPL-2.0 | ✅ |
| SteVe | GPLv3 | ⚠️ 需开源 |
| EVerest | Apache 2.0/GPLv3 | ✅ (部分模块) |
| NewMotion/ocpp | Apache 2.0 | ✅ |

---

*文档生成日期: 2026-05-19*
