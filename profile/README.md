# numas-ai

> 把 AI Agent 的内核、服务与界面拆开，各自独立演进，最终交到用户自己手里。

## 核心项目

### [numas](https://github.com/numas-ai/numas) · 带编程智能体的 Web IDE

numas 以 **OpenSumi** 为 IDE 内核，由 **`@opencode/sdk`** 在服务端进程内提供智能体能力。前后端独立部署，后端地址由前端运行期配置，不写死在构建产物里。

- **三种运行模式**：本地 / 云端 / 实验，平级、独立、场景隔离；
- **本地优先**：本地模式内置 OpenZiti 出站隧道，无需对公网暴露本机；
- **插件化**：业务能力以 VSIX 插件接入，按数据文件驱动渲染（如 `*.vendor` 全景图），底座不做业务定制。

[产品设计](https://github.com/numas-ai/numas/blob/main/docs/design.md) · [工程约定](https://github.com/numas-ai/numas/blob/main/AGENTS.md)

## 仓库一览

| 仓库 | 定位 | 说明 |
| --- | --- | --- |
| [**numas**](https://github.com/numas-ai/numas) | **核心** · Web IDE | OpenSumi + `@opencode/sdk`；三种运行模式；VSIX 插件与数据驱动 |
| [openziti](https://github.com/numas-ai/openziti) | 隧道验证 | 本地 quickstart、运维脚本与 Node SDK `bind` / `dial` 示例（不含二进制与凭据） |
| [vscode-opencode](https://github.com/numas-ai/vscode-opencode) | 容器化工作台 | VS Code + opencode 的 Dockerfile、docker 配置与 VSIX 扩展 |
| [pi](https://github.com/numas-ai/pi) | AI agent toolkit（fork） | 统一的 LLM API、agent loop、TUI 与 coding agent CLI |
| [opencode](https://github.com/numas-ai/opencode) | 开源 coding agent（fork） | 本地优先的 Agent 服务基座，提供 API / SSE / PTY 能力 |

> `pi` 与 `opencode` 为上游开源项目的 fork，版权与许可归其原作者与社区所有。

## 我们在做什么

- **Agent 内核**：把工具、权限、会话与模型接入收敛到清晰的边界，而不是堆进一个黑盒；
- **本地优先的服务化**：内核与部署环境解耦，可跑在本机、VM 或容器，也支持进程内嵌入；
- **产品化界面**：前后端分离，交互由前端按业务定义，服务端只提供 API 支撑。

## 参与协作

- **Issue**：附环境信息、复现步骤与期望结果，越具体越好；
- **PR**：保持单一语义，说明改动动机与验证方式；
- **讨论**：优先在 Issue 中进行，避免上下文分散。

## 联系

- 组织主页：[github.com/numas-ai](https://github.com/numas-ai)
- 项目动态与问题反馈：请通过对应仓库的 Issue 联系。

## 加入交流群

扫码加入 NuMas 交流群（群号：1130109735）。

![NuMas 交流群](https://raw.githubusercontent.com/numas-ai/.github/main/profile/qq-group.jpg)

---

感谢来访，欢迎一起把 Agent 能力做得更开放、更可掌控。
