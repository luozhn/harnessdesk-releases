# HarnessDesk Beta

HarnessDesk 是一个 Windows 桌面 Coding Agent 工作台，用一个界面管理多个原生 Agent 的项目与会话。

这个仓库只用于 **HarnessDesk Beta 安装包发布和公开反馈**。主开发仓库与源代码不在这里公开。

## 目前能做什么

当前 Beta 版本主要包括：

- Codex 集成
- Claude Code 集成
- Project / 原生 Session 管理
- 原生会话历史显示与继续对话
- Agent 回复 Markdown 渲染
- Changes / Diff 文件改动查看
- Project Context（例如 `AGENTS.md` / `CLAUDE.md`）
- 原生接口允许时的历史搜索
- 原生 Slash Command / Skills 能力（视 Agent 支持情况）

HarnessDesk 不重新实现 Agent Loop。Codex / Claude Code 仍然负责自己的推理、工具调用、权限、登录状态和原生会话。

## 下载

请在本仓库右侧或顶部的 **Releases** 中下载最新 Windows 安装包。

> 第一个公开 Beta 安装包正在准备。如果暂时还没有 Release，说明安装包尚未上传完成。

## 安装前请注意

HarnessDesk 当前仍是 **Beta 测试版**：

- 重要项目请使用 Git 或其他版本控制。
- 当前 Windows 安装包尚未进行代码签名，Windows SmartScreen 可能显示“未知发布者”等提示。
- HarnessDesk 不包含 Codex 或 Claude Code。本机需要先安装并登录你要使用的原生 Agent。
- HarnessDesk 不把 Codex / Claude 的认证 Token 保存成自己的账号凭据。

## 基本使用

1. 安装 HarnessDesk。
2. 确保本机已经安装并登录 Codex 和/或 Claude Code。
3. 打开 HarnessDesk。
4. 添加或打开一个项目文件夹。
5. 选择已有原生会话，或创建新会话。
6. 在 Conversation 中继续工作，在 Changes 中检查 Agent 对文件的修改。

更完整的测试步骤见 [BETA_TESTING.md](./BETA_TESTING.md)。

## 当前已知限制

详见 [KNOWN_ISSUES.md](./KNOWN_ISSUES.md)。

目前比较重要的限制：

- Stable Codex 可以打开单个会话并显示历史，但暂不支持 HarnessDesk 的全文历史索引，因为稳定原生接口还没有提供我们要求的有界分页历史契约。
- Codex 当前无法保证与 TUI 的所有 Slash Command 完全一致，只暴露已经确认可用的稳定原生映射。
- 安装包尚未代码签名，因此部分电脑会出现 SmartScreen / reputation 警告。
- 跨版本升级行为仍需要更多真实机器验证。

## 如何反馈 Bug

请直接使用本仓库的 **Issues**。

建议提供：

- HarnessDesk 版本
- Windows 版本
- 使用的 Agent（Codex / Claude Code）
- 预期发生什么
- 实际发生什么
- 可复现步骤
- 必要时附截图
- 必要时附 HarnessDesk Diagnostics 信息

**请勿在公开 Issue 中上传密码、API Key、认证 Token、私人源码或其他敏感信息。**

## Beta 状态

HarnessDesk 仍在持续开发。Beta 期间可能根据真实使用反馈调整 UI、协议和安装方式。
