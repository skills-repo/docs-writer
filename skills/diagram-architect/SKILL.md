---
name: diagram-architect
description: 架构图与流程图：Mermaid/PlantUML 描述系统架构、数据流、时序、ER 关系
source:
  type: original
  repo: skills-repo/docs-writer
  path: skills/diagram-architect/SKILL.md
  version: 1.0.0
  updated: 2026-07-26
metadata:
  category: 文档
  platform: 通用
  difficulty: 入门
---

# 图表架构师

> 用代码画图。描述你的系统结构，输出 Mermaid/PlantUML 图表。一图胜千言。

## 能力

- **架构图**：系统组件、服务间调用关系、部署拓扑
- **流程图**：业务流程、审批流、状态机
- **时序图**：API 调用链、微服务交互、消息传递
- **ER 图**：数据库表关系、实体属性
- **多格式输出**：Mermaid（Markdown 内嵌）、PlantUML、ASCII 图

## 使用方式

```
/diagram-architect 画出这个微服务系统的架构图
/diagram-architect 生成用户登录流程的时序图
/diagram-architect 根据这个 schema 画 ER 图
```

## 图表类型速查

| 需求 | 图表类型 | 推荐工具 |
|------|---------|---------|
| 系统组件关系 | 架构图 (C4) | Mermaid |
| 业务步骤流转 | 流程图 | Mermaid |
| API 调用顺序 | 时序图 | Mermaid |
| 状态变化 | 状态图 | Mermaid |
| 数据表关系 | ER 图 | Mermaid/PlantUML |
| 类继承关系 | 类图 | Mermaid |
| 部署拓扑 | 部署图 | PlantUML |

## 工作流

1. 描述系统结构或业务流程
2. AI 选择合适的图表类型
3. 生成 Mermaid/PlantUML 代码
4. 渲染预览（支持 GitHub/GitLab 原生渲染）
5. 调整布局和标注

## 适用场景

- 系统设计文档需要架构图
- API 文档需要调用时序图
- 数据库设计需要 ER 图
- 流程文档需要可视化

## 限制

- 不生成像素级 UI 设计稿
- 复杂系统可能需要多张图而非一张大图
- GitHub 对 Mermaid 的渲染有少数语法限制