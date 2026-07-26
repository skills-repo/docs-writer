---
name: api-doc-generator
description: API 文档生成：OpenAPI/Swagger 规范，端点说明，请求示例，鉴权文档
source:
  type: derived
  repo: skills-repo/docs-writer
  path: skills/api-doc-generator/SKILL.md
  version: 1.0.0
  updated: 2026-07-26
  url: https://skills.sh/levnikolaevich/claude-code-skills/ln-775-api-docs-generator
metadata:
  category: 文档
  platform: Web
  difficulty: 进阶
---

# API 文档生成器

> 自动生成 API 参考文档：OpenAPI/Swagger 规范、端点说明、请求/响应示例、鉴权文档。

## 能力

- **OpenAPI 规范**：生成符合 OpenAPI 3.0 规范的 API 描述文件
- **端点文档**：路径、方法、参数、请求体、响应体的完整文档
- **鉴权文档**：API Key、Bearer Token、OAuth2 等方式的说明
- **示例生成**：请求/响应示例、错误码说明
- **格式输出**：Swagger UI、Redoc、Markdown 等多种输出

## 使用方式

```
/api-doc-generator 为这个 Express 路由生成 API 文档
/api-doc-generator 从代码注释生成 OpenAPI 规范
/api-doc-generator 更新这个 API 的请求示例
```

## 工作流

1. 扫描代码中的 API 路由定义
2. 提取端点、参数、请求/响应类型
3. 识别鉴权方式和错误处理
4. 生成 OpenAPI/Swagger 规范文件
5. 可选：渲染为可交互的 API 文档

## 适用场景

- REST API 文档化
- OpenAPI 规范补全
- API 文档从代码注释自动生成
- 第三方 API 对接文档

## 限制

- 主要覆盖 REST API，不涉及 GraphQL schema 文档
- 不涉及 SDK 文档生成
- 复杂鉴权流程需手动补充