---
name: readme-generator
description: README 文档生成：项目徽章、安装说明、API 概览、贡献指南，专业级模板
source:
  type: derived
  repo: skills-repo/docs-writer
  path: skills/readme-generator/SKILL.md
  version: 1.0.0
  updated: 2026-07-26
  url: https://skills.sh/patricio0312rev/skills/readme-generator
metadata:
  category: 文档
  platform: 通用
  difficulty: 入门
---

# README 生成器

> 自动生成专业 README 文档：项目介绍、徽章、安装说明、API 概览、贡献指南。

## 能力

- **项目分析**：识别项目类型和技术栈，生成对应的文档结构
- **徽章生成**：版本、构建状态、覆盖率、许可等自动生成
- **安装指南**：前置条件、包管理器、从源码构建
- **使用说明**：基本用法、API 文档、配置选项
- **贡献指南**：开发流程、代码规范、PR 模板

## 使用方式

```
/readme-generator 为这个项目生成 README
/readme-generator 更新 README 中的 API 文档部分
/readme-generator 为这个 TypeScript 库生成文档
```

## 工作流

1. 分析项目结构和 package.json/配置文件
2. 识别项目类型和技术栈
3. 生成对应的 README 模板
4. 填入项目具体信息
5. 输出完整文档

## 适用场景

- 新项目文档初始化
- 现有项目文档更新
- 开源项目文档完善
- 多语言项目文档

## 限制

- 模板化输出，特殊项目需手动调整
- 不涉及 API 参考文档的详细生成
- 不涉及多语言翻译