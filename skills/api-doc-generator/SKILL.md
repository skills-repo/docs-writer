---
name: api-doc-generator
description: API 文档生成：从代码中提取端点，生成 OpenAPI/Swagger 规范文档，含请求/响应示例
source:
  type: original
  repo: skills-repo/docs-writer
  path: skills/api-doc-generator/SKILL.md
  version: 1.0.0
  updated: 2026-07-26
metadata:
  category: 文档
  platform: 通用
  difficulty: 进阶
---

# API 文档生成器

> 从代码中的路由定义自动生成 API 文档。支持 REST 和 GraphQL，输出 OpenAPI 3.0 规范。

## 能力

- **路由提取**：从 Express/FastAPI/Next.js/Go 等框架中提取路由定义
- **OpenAPI 生成**：自动生成 OpenAPI 3.0 spec（paths、parameters、responses、schemas）
- **请求/响应示例**：根据类型定义推断请求体和响应体示例
- **错误码文档**：提取错误处理逻辑，生成错误码表
- **多格式输出**：YAML/JSON spec 文件、HTML 文档页、Markdown API 参考

## 使用方式

```
/api-doc                    # 为当前项目的 API 路由生成文档
/api-doc src/routes/        # 指定路由目录
/api-doc --format markdown  # 输出 Markdown 格式
```

## 支持的框架

| 框架 | 路由识别方式 |
|------|-------------|
| Express.js | `app.get/post/put/delete(...)` |
| FastAPI | `@app.get/post(...)` + type hints |
| Next.js | `route.ts` 文件 |
| Go (net/http) | `http.HandleFunc(...)` |
| Flask | `@app.route(...)` |

## 工作流

1. 扫描路由文件，提取 HTTP 方法和路径
2. 从类型定义/注释中提取参数和返回值类型
3. 生成 OpenAPI paths 和 components/schemas
4. 补充请求/响应示例
5. 输出文档文件

## 适用场景

- 新 API 上线前补齐文档
- 已有 API 无文档需要生成初始版本
- 前后端协作需要统一的 API spec
- 向第三方暴露 API 时提供参考文档

## 限制

- 生成的文档准确度依赖代码中类型定义的完整性
- 非标准路由写法可能无法正确识别
- 不处理 WebSocket/gRPC 等非 REST 协议