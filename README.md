# AI Fullstack Lab

这是一条新的、独立的学习路径：面向前端工程师，目标是转向 **AI 全栈工程师**。

它是一个自包含学习目录，不依赖其他学习路径。正式学习时只需要跟随这个目录里的 `ai-fullstack-learning` skill 和进度文件。

这条路线只有一条单主线：

- 用 Node/TypeScript、HTTP、数据库、认证授权、测试和部署打工程地基。
- 用真实业务功能承载 AI：流式交互、结构化输出、工具调用、RAG、evals、安全、成本和可观测性。
- 用一个长期产品项目贯穿，不让学习变成零散 demo。

## 目录结构

```text
ai-fullstack-lab/
  README.md
  AI_FULLSTACK_PROGRESS.md
  ai-fullstack-learning/      # Codex skill：学习协议、自动化和课程大纲
    SKILL.md
    agents/openai.yaml
    references/
```

后续学习时，skill 会按需创建：

```text
ai-fullstack-lab/
  ai-fullstack-labs/          # 独立单元练习、状态文件、完成记录
  workbench-ai/               # 长期 AI 全栈产品项目
```

## 快速开始

在 Codex 里说：

```text
使用 $ai-fullstack-learning，开始 U01
```

继续上次学习：

```text
使用 $ai-fullstack-learning，继续
```

检查当前单元是否完成：

```text
使用 $ai-fullstack-learning，检查
```

## 设计原则

- 只维护一个当前学习状态，避免在多个学习方向之间来回切换。
- 每个单元都有可交付物、checkpoint、验证方式和完成边界。
- 不按天数推进，只按 unit 完成情况推进。
- 默认由 Codex 创建 starter、记录进度、判断完成，不把协调负担丢给学习者。
- 每 2-3 个单元都有一个可见产品能力，降低放弃感。
- Codex 是学习时的主引导；README/TODO 文件只是记录、验收和恢复上下文的支持材料。
- 没有 `paused` 状态。一个单元没完成就是 `in progress`，完成边界达成就是 `completed`。
