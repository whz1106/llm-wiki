# 操作日志

## [2026-05-23] init | 初始化 Wiki
- 根据 [[wiki.md]] 的 LLM Wiki 模式构建三层架构
- 新建：`AGENTS.md`（Schema）、`index.md`（索引）、`log.md`（日志）
- 新建目录：`raw/`、`wiki/concepts/`、`wiki/entities/`、`wiki/sources/`

## [2026-05-23] ingest | 保存原始链接
- 源文件：`raw/testerhome-article-42005.md`
- 说明：TesterHome 文章链接，暂不可用（500），待后续处理

## [2026-05-23] archive | TesterHome Article #42005
- 源文件：`raw/testerhome-article-42005.html`
- 新页面：`raw/testerhome-article-42005-archive-note.md`
- 说明：尝试归档原文时，源站返回 `HTTP 500`；已保留错误页快照，并补充文章来源与归档状态说明，待后续补抓正文

## [2026-05-23] ingest | 通往专家之路，三万字长文详解大模型性能测试
- 源文件：`raw/2025-04-16-testerhome-42005-recovered.md`
- 新页面：`wiki/sources/2025-04-16-llm-performance-testing.md`
- 更新页面：`wiki/concepts/llm-performance-testing.md`、`wiki/concepts/prefill-decode.md`、`wiki/concepts/pd-separation.md`、`wiki/entities/sun-gaofei.md`、`index.md`
- 说明：基于可读取缓存页恢复文章结构与关键内容，完成 Wiki 摘要、概念页与作者实体页的初始建档

## [2026-05-23] maintain | 清理失败归档
- 删除文件：`raw/testerhome-article-42005.md`、`raw/testerhome-article-42005.html`、`raw/testerhome-article-42005-archive-note.md`
- 更新页面：`index.md`
- 说明：早期失败抓取记录已被恢复版原始资料替代，保留 `raw/2025-04-16-testerhome-42005-recovered.md` 作为当前唯一原始资料入口

## [2026-05-25] query | 大模型性能测试指标清单
- 更新页面：`wiki/concepts/llm-performance-testing.md`、`index.md`
- 说明：将现有概念页扩展为指标清单入口，补充效果、指令遵循、鲁棒性、性能、成本、安全与业务结果等维度
