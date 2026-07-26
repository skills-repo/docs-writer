---
name: diagram-architect
description: 图表架构设计：Mermaid 流程图、时序图、ERD、架构图，支持 Markdown 嵌入
source:
  type: derived
  repo: skills-repo/docs-writer
  path: skills/diagram-architect/SKILL.md
  version: 1.0.0
  updated: 2026-07-26
  url: https://skills.sh/patricio0312rev/skills/mermaid-diagram-generator
metadata:
  category: 文档
  platform: Web
  difficulty: 入门
---

# 图表架构师

> Mermaid 图表生成：流程图、时序图、ERD、架构图，Markdown 原生支持。

## 能力

- **流程图**：决策树、业务流程、状态机
- **时序图**：API 调用时序、消息传递、交互流程
- **ERD 图**：实体关系、表结构、外键关联
- **架构图**：系统架构、微服务拓扑、网络拓扑
- **子图与分组**：嵌套子图、Colored 分组、自定义样式

## 使用方式

```
/diagram-architect 为这个登录流程画一个时序图
/diagram-architect 生成数据库 ER 图
/diagram-architect 用流程图描述这个审核流程
```

## 工作流

1. 理解业务逻辑或代码结构
2. 选择合适的图表类型（流程图/时序图/ERD/架构图）
3. 构建节点、连接、标签
4. 应用样式（颜色、形状、方向）
5. 输出 Mermaid 语法，可直接嵌入 Markdown

## 适用场景

- 技术文档中的流程图
- API 对接的时序设计
- 数据库设计文档
- 系统架构文档

## 限制

- 仅输出 Mermaid 语法，不生成图片
- 复杂图表需手动美化布局
- 不涉及非 Mermaid 图表格式（PlantUML/Graphviz）