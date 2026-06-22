# 女娲智能体平台 Agent 配置

本仓库存放女娲智能体平台（testagent.xspaceagi.com）上两个项目开发 Agent 的编排配置。

## 目录结构

```
.
├── README.md
├── skill-dev-agent/      # 技能开发 Agent (agent/2844)
│   └── config.md
└── plugin-dev-agent/     # 插件开发 Agent (agent/2845)
    └── config.md
```

## Agent 说明

### 技能开发 Agent (agent/2844)

- 模型：glm-5.1-anthropic-QC
- 职责：按平台 Skill 规范，专职负责技能的开发、编辑、维护与生成
- 挂载技能：skill-developer、skill-creator
- 挂载工具：context7、Fetch 网页内容抓取、Markdown 万能转换

### 插件开发 Agent (agent/2845)

- 模型：glm-5-openai-QC
- 职责：帮助用户完成插件（Plugin）的开发、配置、测试与发布
- 挂载技能：plugin-api
- 挂载工具：context7、Fetch 网页内容抓取

## 平台地址

- https://testagent.xspaceagi.com/space/1136

## 注意事项

配置中的系统提示词为纯文本备份，如需修改请同步到平台编排页面。
