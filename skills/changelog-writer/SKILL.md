---
name: changelog-writer
description: Changelog 自动化：从 Git commit 历史生成结构化变更日志，遵循 Keep a Changelog 规范
source:
  type: original
  repo: skills-repo/docs-writer
  path: skills/changelog-writer/SKILL.md
  version: 1.0.0
  updated: 2026-07-26
metadata:
  category: 文档
  platform: GitHub
  difficulty: 入门
---

# Changelog 编写器

> 从 Git commit 历史自动生成结构化的 CHANGELOG.md。不是把所有 commit 复制过来，而是分类、聚合、用人话写。

## 能力

- **Commit 分析**：读取 git log，按 Conventional Commits 分类（feat/fix/docs/refactor）
- **变更聚合**：合并同类变更，生成用户可读的条目
- **Keep a Changelog**：遵循 keepachangelog.com 1.0.0 规范
- **版本推断**：根据 commit 类型自动建议语义化版本号
- **已有内容合并**：更新已有 CHANGELOG 时保留手动编写的内容

## 使用方式

```
/changelog-writer                  # 从上次 tag 到现在的变更生成 CHANGELOG
/changelog-writer v1.0.0..HEAD     # 指定范围
/changelog-writer --release 2.0.0  # 为新版本生成 release entry
```

## 输出格式

```markdown
# Changelog

## [1.2.0] - 2026-07-26

### Added
- 用户头像上传功能
- 暗色模式支持

### Fixed
- 修复登录页面密码框不显示的问题

### Changed
- API 响应格式统一为 JSON:API
```

## 工作流

1. 读取 `git log --oneline` 自上次 tag 的变更
2. 按 Conventional Commits 分类（feat→Added, fix→Fixed, refactor→Changed, docs→Documentation）
3. 合并同类型、同模块的变更
4. 生成或更新 CHANGELOG.md
5. 建议语义化版本号

## 适用场景

- 项目发布前整理变更日志
- 自动化 release workflow 中的 changelog 生成
- 团队需要标准化 changelog 格式
- 从混乱的 commit 历史中提取用户可读的发布说明

## 限制

- 依赖 commit message 遵循规范（无规范时分类准确度下降）
- 重大变更（breaking changes）需要人工标注
- 不处理 monorepo 多包 changelog