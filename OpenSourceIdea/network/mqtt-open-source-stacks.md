# MQTT 开源协议栈总结

## 1. MQTT 简介

MQTT（Message Queuing Telemetry Transport）是一种轻量级发布/订阅消息协议，设计用于低带宽、不可靠网络和受限设备之间的通信。它具有低开销、易于实现、支持 QoS 等级和保留消息机制，广泛应用于 IoT、工业物联网、远程监控、传感器网络等场景。

MQTT 协议栈通常包括两个部分：

- Broker：消息服务器，负责接收、存储、分发主题消息，并管理客户端会话与订阅。
- Client：发布者/订阅者，负责连接 Broker、发送消息、接收订阅消息和保持心跳。

开源 MQTT 实现覆盖多种语言、平台和性能需求，从嵌入式设备到云端服务均有大量成熟方案。

## 2. 主流开源 MQTT Broker

### 2.1 Eclipse Mosquitto

- 官方地址：`https://mosquitto.org/` / `https://github.com/eclipse/mosquitto`
- 许可证：EPL-2.0
- 语言：C
- 平台：Linux、Windows、macOS、嵌入式

#### 特点

- 轻量、稳定，适合资源受限系统。
- 支持 MQTT v3.1、v3.1.1 和部分 v5.0 功能。
- 支持持久化存储、TLS/SSL、用户名/密码、ACL、桥接等。
- 常用于边缘网关、嵌入式 IoT 网关和小型消息中间件部署。

#### 适用场景

- 边缘计算、嵌入式设备网关、小型工业现场网关。
- 快速部署 MQTT Broker 进行功能验证和系统集成。

### 2.2 EMQX

- 官方地址：`https://www.emqx.io/` / `https://github.com/emqx/emqx`
- 许可证：Apache-2.0
- 语言：Erlang/Elixir（核心）
- 平台：Linux、macOS、Docker、Kubernetes

#### 特点

- 高性能、高可用、可扩展，支持百万级连接。
- 支持 MQTT v3.1、v3.1.1、v5.0、CoAP、WebSocket、STOMP 等协议。
- 提供集群部署、规则引擎、身份认证、ACL、插件扩展等功能。

#### 适用场景

- 企业级 IoT 平台、大规模工业物联网系统。
- 需要横向扩展、高可用和多协议接入的场景。

### 2.3 VerneMQ

- 官方地址：`https://vernemq.com/` / `https://github.com/vernemq/vernemq`
- 许可证：Apache-2.0
- 语言：Erlang
- 平台：Linux、Docker、Kubernetes

#### 特点

- 面向高吞吐、分布式部署和集群管理。
- 支持 MQTT v3.1、v3.1.1、v5.0、WebSocket。
- 支持消息持久化、ACL、插件和监控接口。

#### 适用场景

- 大规模工业通信、云原生 IoT 平台、跨数据中心部署。

## 3. 主流开源 MQTT Client 库

### 3.1 Eclipse Paho

- 官方地址：`https://www.eclipse.org/paho/` / `https://github.com/eclipse/paho.mqtt.python` 等
- 许可证：EPL-2.0
- 语言：Java、Python、C、C++、JavaScript、Go 等多种语言
- 平台：跨平台、嵌入式、桌面、云端

#### 特点

- 官方 Eclipse MQTT 客户端系列，覆盖多语言实现。
- 支持 MQTT v3.1、v3.1.1、v5.0、TLS、安全连接。
- 适合与 Broker 集成、开发设备端或应用端客户端。

#### 适用场景

- 多语言开发环境下的 MQTT 客户端集成。
- IoT 设备、网关和应用系统连接 Broker。

### 3.2 MQTT.js

- 官方地址：`https://github.com/mqttjs/MQTT.js`
- 许可证：MIT
- 语言：JavaScript/Node.js
- 平台：Node.js、浏览器

#### 特点

- 轻量、常用于 Web 与 Node.js 应用。
- 支持 MQTT over WebSocket、TLS、QoS、遗嘱消息等。
- 适用于云应用、可视化平台、浏览器终端、边缘服务。

#### 适用场景

- 基于 Node.js 的云服务或 Web 应用与 MQTT Broker 集成。
- 浏览器端 MQTT 数据展示或远程监控应用。

### 3.3 libmosquitto / mosquitto_client

- 官方地址：`https://github.com/eclipse/mosquitto`
- 许可证：EPL-2.0
- 语言：C
- 平台：Linux、Windows、嵌入式

#### 特点

- Mosquitto 提供的客户端库与命令行工具。
- 支持基本 MQTT 客户端操作、QoS、持久会话等。
- 适合嵌入式设备与 C/C++ 项目。

#### 适用场景

- 需要高性能 C 客户端或直接嵌入终端设备的 MQTT 访问。

## 4. 其他开源 MQTT 项目与生态

### 4.1 HiveMQ Community Edition

- 官方地址：`https://www.hivemq.com/` / `https://github.com/hivemq/hivemq-community-edition`
- 许可证：Apache-2.0
- 语言：Java
- 平台：Linux、Docker、Kubernetes

#### 特点

- 企业特性与社区版本并存，支持 MQTT 集群、WebSocket、插件。
- 适合 Java 生态系统与大规模消息代理部署。

### 4.2 NanoMQ

- 官方地址：`https://github.com/emqx/nanomq`
- 许可证：Apache-2.0
- 语言：C
- 平台：Linux、Docker、嵌入式

#### 特点

- 面向边缘计算与嵌入式设备的轻量 MQTT Broker。
- 支持 MQTT-SN、WebSocket、TLS、集成 EMQX 管理。

### 4.3 EdgeX Foundry MQTT 组件

- 官方地址：`https://www.edgexfoundry.org/`
- 许可证：Apache-2.0
- 语言：Go、Java
- 平台：边缘网关、工业物联网平台

#### 特点

- 作为 EdgeX 平台的一部分，提供 MQTT 发布/订阅能力。
- 适合工业边缘通信与设备数据汇聚。

## 5. 主要协议栈比较

| 项目 | 类型 | 语言 | 许可证 | 适用场景 |
|---|---|---|---|---|
| Eclipse Mosquitto | Broker | C | EPL-2.0 | 轻量 Broker、嵌入式网关、边缘部署 |
| EMQX | Broker | Erlang | Apache-2.0 | 大规模、高可用、企业 IoT 平台 |
| VerneMQ | Broker | Erlang | Apache-2.0 | 分布式、云原生、集群部署 |
| Eclipse Paho | Client 库 | 多语言 | EPL-2.0 | 多语言客户端开发 |
| MQTT.js | Client 库 | JavaScript | MIT | Web/Node.js 应用、可视化平台 |
| libmosquitto | Client 库 | C | EPL-2.0 | 嵌入式设备、原生 C/C++ 客户端 |

## 6. 选型建议

- 需要简单、轻量 Broker 时，优先选择 `Eclipse Mosquitto`。
- 需要高并发、集群、企业功能时，推荐 `EMQX` 或 `VerneMQ`。
- 在 Java 环境下构建 Broker，`HiveMQ Community Edition` 是可靠选项。
- 设备端客户端开发可优先使用 `Eclipse Paho` 系列或 `libmosquitto`。
- Web/Node.js 场景下，`MQTT.js` 是最常用的开源客户端库。
- 在工业物联网边缘方案中，可结合 `NanoMQ` 与 `EMQX` 进行网关与云端联接。

## 7. 参考资料

- MQTT 官方网站: https://mqtt.org/
- Eclipse Mosquitto: https://mosquitto.org/
- EMQX: https://www.emqx.io/
- VerneMQ: https://vernemq.com/
- HiveMQ Community Edition: https://www.hivemq.com/
- Eclipse Paho: https://www.eclipse.org/paho/
