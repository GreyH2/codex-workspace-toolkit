# 工作区规则入口

本文件所在目录是当前工作区根目录，以下规则使用 `<WORKSPACE_ROOT>` 表示该目录。

只读取当前任务实际需要的规则文件，不要预读全部 `.agent` 文档，也不要在同一任务中重复读取未变化的规则。

## 按需规则

- 创建、保存、移动、整理或交付文件，以及判断输出目录：读取 [`.agent/file-routing.md`](.agent/file-routing.md)。
- 编程、调试、测试或软件项目：读取 [`.agent/coding.md`](.agent/coding.md)。
- 操作本机、操作系统、文件系统、应用、存储空间、清理或维护：读取 [`.agent/computer-ops.md`](.agent/computer-ops.md)。
- 上网搜索、查询实时信息、下载公开资料，或登录、上传、发布、发送及修改远程数据：读取 [`.agent/external-services.md`](.agent/external-services.md)。
- 从聊天或任务中创建本地笔记、摘要或长期记录：读取 [`.agent/chat-notes.md`](.agent/chat-notes.md)。
- 普通问答、解释、建议或状态说明：读取 [`.agent/conversation-efficiency.md`](.agent/conversation-efficiency.md)。
- 长任务、上下文接近上限、发生上下文压缩，或需要跨对话恢复未完成工作：读取 [`.agent/context-continuity.md`](.agent/context-continuity.md)。
- 当前任务不被已有规则覆盖，而且可能形成稳定、重复使用的新工作流规则：读取 [`.agent/rule-evolution.md`](.agent/rule-evolution.md)。

一个任务确实涉及多类职责时，只读取对应的几份规则。没有专用规则适用时直接正常完成任务。

用户当前的明确要求和指定输出路径优先于这些默认规则。除非用户明确要求，否则不要移动或重组已有文件。
