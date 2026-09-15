# 文件归档与目录扩展

仅在任务实际创建、保存、移动、整理或交付文件时应用本规则。`<WORKSPACE_ROOT>` 表示根目录 `AGENTS.md` 所在位置。

## 基础目录

- 软件、网站、脚本、代码仓库及多文件项目：`<WORKSPACE_ROOT>\Projects\<项目名称>\`
- Word、PDF、表格、演示文稿和普通文本：`<WORKSPACE_ROOT>\Documents\<类型>\<主题或项目>\`
- 音频和视频：`<WORKSPACE_ROOT>\Media\<Audio|Video>\<主题或项目>\`
- 可重复使用的提示词：`<WORKSPACE_ROOT>\Prompts\<用途>\<主题>\`
- 普通聊天、调研、计划、排障和创意笔记：`<WORKSPACE_ROOT>\Chats\<General|Research|Planning|Troubleshooting|Creative>\`
- 临时下载、中间产物和可丢弃文件：`<WORKSPACE_ROOT>\Temp\<任务名称>\`

不要把交付文件直接放在工作区根目录。用户没有命名时，任务目录使用 `YYYY-MM-DD-简短主题`；名称应简短、清晰，并与相邻目录风格一致。

## 新类型

现有映射不是封闭清单。优先放入具体项目，其次复用准确匹配的现有分类。只有新类型与现有分类明显不同且具有长期或重复使用价值时，才创建新的、名称稳定的根分类，并在本文件的“基础目录”中追加对应关系。

不要为一次性文件创建根分类。无法可靠判断时，先放入 `<WORKSPACE_ROOT>\Temp\Needs-Review\<任务名称>` 并告诉用户。不要创建大小写、单复数、缩写或同义词不同的重复目录。

创建新根分类时说明原因、路径和适用内容。凡创建了文件，最终回复说明主要交付文件的路径。
