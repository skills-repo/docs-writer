---
name: changelog-writer
description: Changelog 与 Release Notes 生成：基于 Commit 历史、Keep a Changelog 格式、语义化版本
source:
  type: derived
  repo: skills-repo/docs-writer
  path: skills/changelog-writer/SKILL.md
  version: 1.0.0
  updated: 2026-07-26
  url: https://skills.sh/patricio0312rev/skills/changelog-writer
metadata:
  category: 文档
  platform: 通用
  difficulty: 入门
---

# Changelog 与 Release Notes 生成器

> 从 Git 提交历史自动生成结构化的 Changelog 和 Release Notes，遵循 Keep a Changelog 标准。

## 能力

- **Commit 解析**：识别 Conventional Commits 格式（feat/fix/docs/refactor）
- **变更分类**：Added/Changed/Fixed/Deprecated/Removed/Security
- **Breaking Change 识别**：标记不兼容变更
- **版本建议**：基于变更内容推荐语义化版本号
- **Release Notes**：生成用户友好的发布摘要

## 使用方式

```
/changelog-writer 为最近 50 个提交生成 Changelog
/changelog-writer 为 v1.0.0 到 v1.5.0 生成 Release Notes
/changelog-writer 审查这个 Changelog 的格式
```

## 工作流

1. 解析 Git 提交历史（自上次发布以来）
2. 按类型分类变更（feat→Added, fix→Fixed, BREAKING→Breaking）
3. 识别关键变更和亮点
4. 按 Keep a Changelog 格式组织
5. 建议语义化版本号

## 适用场景

- 开源项目版本发布
- 内部项目变更追踪
- CI/CD 自动发布流程
- 用户沟通的 Release Notes

## 限制

- 依赖 Conventional Commits 格式，非标准提交需手动分类
- 不涉及自动化发布流程（npm publish/git tag）
- 不涉及多语言 Release Notes