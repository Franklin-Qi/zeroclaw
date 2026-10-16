# ZeroClaw 技术框架笔记

> **用途：** 个人学习 / 远程仓库记录分支（`notes/tech-framework`）。  
> **不是** 上游文档、**不会** 开 PR。正式权威仍以 `docs/book/` 与 `AGENTS.md` 为准。  
> **对齐 revision：** 基于 `upstream/master` @ `ae9b84be0`（工作区版本约 `0.8.5`）。

本目录是一份「从仓库结构读出的」技术框架速览：分层、核心能力、请求路径、以及该去哪读官方细节。

| 文档 | 内容 |
|---|---|
| [01-overview.md](./01-overview.md) | 产品定位、分层总图、二进制与 apps |
| [02-crates-and-traits.md](./02-crates-and-traits.md) | Crate 分层、`zeroclaw-api` 内核 ABI、依赖方向 |
| [03-request-and-security.md](./03-request-and-security.md) | 一次对话的生命周期、安全与自治、工具回执 |
| [04-subsystems.md](./04-subsystems.md) | Channel / Provider / Tool / Memory / Gateway / SOP / Plugin / 调度 |
| [05-data-and-ops.md](./05-data-and-ops.md) | Config、持久化、日志、CI/功能开关、延伸阅读 |

## 一句话

**ZeroClaw = 可自托管的个人 AI Agent Runtime（Rust）**：用户经 CLI / 消息通道 / Gateway / IDE(ACP) 进来；Runtime 驱动模型循环与工具调用；边沿 crate 对接 LLM、聊天平台、硬件与 WASM 插件。

## 官方入口（优先）

- 架构总览：`docs/book/src/architecture/overview.md`
- Crate 说明：`docs/book/src/architecture/crates.md`
- 变更路由图：`docs/book/src/contributing/architecture-map.md`
- 微内核愿景：`docs/book/src/foundations/fnd-001-intentional-architecture.md`（RFC #5574）
- 仓库契约：根目录 `AGENTS.md`
