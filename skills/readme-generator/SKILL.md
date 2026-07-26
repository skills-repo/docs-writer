---
name: readme-generator
description: README 自动生成：分析项目结构，生成专业 README（介绍/安装/用法/API/贡献）
source:
  type: original
  repo: skills-repo/docs-writer
  path: skills/readme-generator/SKILL.md
  version: 1.0.0
  updated: 2026-07-26
metadata:
  category: 文档
  platform: GitHub
  difficulty: 入门
---

# README 生成器

> 扫描代码库，自动生成结构清晰、内容完整的 README.md。一个好的 README 让项目在第一眼就被理解。

## 能力

- **项目结构分析**：自动识别语言、框架、入口文件、构建系统
- **README 模板**：多种风格模板（简约/minimal、完整/full、产品/product）
- **安装指南**：自动生成依赖安装、环境配置步骤
- **API 速览**：从代码中提取主要 API 端点或公开函数
- **徽章生成**：自动建议合适的 Shields.io 徽章

## 使用方式

```
/readme-generator                # 为当前项目生成 README
/readme-generator --style full   # 使用完整模板
/readme-generator --update       # 更新已有 README（保留手动内容）
```

## README 标准结构

```markdown
# 项目名
> 一句话描述

## 特性
## 快速开始
## 安装
## 用法
## API
## 配置
## 贡献
## 许可
```

## 工作流

1. 扫描项目目录结构和关键文件
2. 识别语言/框架/构建工具
3. 提取公开 API 或函数签名
4. 生成 README，填写每个 section
5. 检查已有 README，合并手动内容

## 适用场景

- 新项目初始化时需要第一个 README
- 已有 README 过时或不完整需要重写
- 开源项目发布前完善文档
- 团队需要统一的 README 风格

## 限制

- 生成的 README 需要人工审查和补充细节
- 不处理非代码项目（纯文档仓库等）的 README
- 语言检测基于常见模式，特殊项目可能需手动指定