# Codex 工作区规则工具包

一套面向 Codex、ChatGPT Work 和普通 Chat 本地文件任务的轻量工作区规则模板。它使用简短的 `AGENTS.md` 作为唯一入口，再按当前任务需要读取 `.agent` 中的专用规则，减少无关上下文、重复扫描和过度工作。

## 特点

- **渐进式读取**：只加载与当前任务有关的规则。
- **文件自动归档**：根据交付物和项目归属选择目录，新类型可按稳定需求扩展。
- **规则自动演进**：仅在真实、重复、长期的规则缺口出现时新增规则。
- **上下文连续性**：长任务在必要时维护最小恢复检查点，不逐轮保存聊天。
- **适度验证**：优先检查受影响范围，风险或证据需要时再扩大验证。
- **安全边界**：普通本地工作直接推进，高风险或不可逆操作保留确认边界。

本仓库不包含图片生成 Skill、创作路由、私人聊天原文或个人工作区内容。

## 目录结构

```text
workspace-template/
├── AGENTS.md
└── .agent/
    ├── file-routing.md
    ├── coding.md
    ├── computer-ops.md
    ├── chat-notes.md
    ├── context-continuity.md
    ├── rule-evolution.md
    └── design-principles.md
```

## 安装

1. 下载或克隆本仓库。
2. 将 `workspace-template` 内的 `AGENTS.md` 和 `.agent` 一起复制到你的工作区根目录。
3. 将该目录选为 Codex 或 ChatGPT Work 的本地工作目录。
4. 根据自己的文件分类习惯修改 `.agent/file-routing.md`；保持 `AGENTS.md` 简短。

安装后的结构示例：

```text
你的工作区/
├── AGENTS.md
├── .agent/
├── Projects/
├── Documents/
├── Chats/
└── Temp/
```

规则使用 `<WORKSPACE_ROOT>` 表示 `AGENTS.md` 所在的工作区根目录，无需使用固定盘符或用户名。

## 使用方式

正常向 Codex 描述任务即可。根入口会按任务类型选择规则，例如：

- 创建或整理文件时读取 `file-routing.md`；
- 编程、调试或测试时读取 `coding.md`；
- 操作 Windows、文件系统或本地应用时读取 `computer-ops.md`；
- 创建聊天摘要或长期笔记时读取 `chat-notes.md`；
- 长任务可能跨上下文继续时读取 `context-continuity.md`。

如果没有专用规则，Agent 应直接正常完成任务，不为了寻找规则而扫描全部文档。

## 自定义原则

- 只把稳定、重复、会改变 Agent 决策的要求写入规则。
- 不为单个扩展名、工具或一次性任务创建专用文件。
- 新规则放入 `.agent`，并在 `AGENTS.md` 增加一条简短、明确的触发条件。
- 专业能力如果需要脚本、模板、素材或复杂工作流，应制作成 Skill，而不是塞入工作区规则。
- 用户当前的明确要求和指定路径始终优先于默认规则。

更完整的维护边界见 [`workspace-template/.agent/design-principles.md`](workspace-template/.agent/design-principles.md)。

## 适用范围

这是可修改的个人工作区模板，不保证所有 Codex、ChatGPT 或第三方 Agent 环境都会以完全相同的方式自动发现 `AGENTS.md`。如果所用环境不会自动加载它，请在该环境的项目说明中明确要求先读取根目录 `AGENTS.md`。

## 许可证

本项目以 [MIT License](LICENSE) 发布。
