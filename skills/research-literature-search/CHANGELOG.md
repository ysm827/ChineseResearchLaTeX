# Changelog

## [1.0.0] - 2026-09-02

### Added

- 新增独立 `research-literature-search` Skill 与 `rls.v1` manifest/candidate 契约。
- 提供 `run`、`enrich-abstracts`、`validate` 稳定命令。
- 支持 OpenAlex 主力、Semantic Scholar/Crossref 补充，以及 MCP/duckduckgo 显式 skipped 审计。
- 输出 raw、normalized、deduped、provenance、dedupe map 和兼容 Search Log。

### Fixed

- 对输出 scope 越界、非法 provider 返回值和不安全错误文本执行 fail-closed 处理，并补充 provider policy 指纹与语言/开放获取过滤。
- 去重合并保留两侧 identifiers；摘要补全成功时不再错误追加 `missing_abstract` 警告；bundle validator 严格校验 artifact hash、字节数和查询计数。
