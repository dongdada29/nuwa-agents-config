# 女娲平台 Agent 配置

女娲智能体平台（testagent.xspaceagi.com）上两个项目开发 Agent 的编排配置：系统提示词、用户提示词、技能与工具挂载。

## Agent 一览

| Agent | ID | 模型 | 核心技能 |
|-------|-----|------|---------|
| 技能开发 | [2844](https://testagent.xspaceagi.com/space/1136/agent/2844) | glm-5.1-anthropic-QC | skill-developer, skill-creator |
| 插件开发 | [2845](https://testagent.xspaceagi.com/space/1136/agent/2845) | glm-5-openai-QC | plugin-api |

## 文件结构

```
.
├── package.json
├── README.md
├── skill-dev-agent/              # 技能开发 Agent (2844)
│   ├── system-prompt.md          # 系统提示词
│   ├── user-prompt.md            # 用户提示词
│   ├── tools.md                  # 工具与技能挂载配置
│   └── skills/
│       ├── skill-developer/SKILL.md
│       └── skill-creator/SKILL.md
└── plugin-dev-agent/             # 插件开发 Agent (2845)
    ├── system-prompt.md
    ├── user-prompt.md
    ├── tools.md
    └── skills/
        └── plugin-api/SKILL.md
```

## 修改流程

1. 修改本仓库对应文件
2. 复制 `system-prompt.md` / `user-prompt.md` 内容到平台编排页
3. 在平台「工具 / 技能」面板同步挂载配置（参考 `tools.md`）
4. 更新 `package.json` 的 `version`
