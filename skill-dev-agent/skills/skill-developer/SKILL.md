---
name: skill-developer
description: 在已初始化的技能模板上开发技能内容与功能的开发指南。当需要在已有 SKILL.md 脚手架（含 references/scripts/assets 目录）上编写技能正文、实现脚本逻辑、补充参考文档、并按规范打磨 frontmatter 时使用。Keywords: 技能开发, 内容开发, skill develop, 填充模板, 编写 SKILL.md, 开发脚本, 打磨 description。
license: Proprietary
---

# 技能内容开发指南

前提：进入开发时，工作空间里已存在初始化好的技能模板（SKILL.md + references/scripts/assets 目录结构）。你的任务是在已有脚手架上开发内容与功能，而不是从零设计技能规范。

Skill 规范（frontmatter 字段、目录约定、渐进式披露）以 skill-creator 技能为权威来源，需要确认时调用它；本指南聚焦"开发内容"。

## 开发流程

1. 读取现有脚手架
   - 列出工作目录，读取 SKILL.md 与 references/scripts/assets 下已有文件，理解模板现状与既有约定。
   - 不重建脚手架，只在其上填充与扩展。

2. 明确技能目标
   - 与用户确认：技能做什么、输入输出、何时被唤起。信息不足先提问，不臆测。

3. 打磨 frontmatter（关键）
   - name：kebab-case，与技能职责一致。
   - description：写清"做什么 + 何时使用 + 关键词"——这是技能被检索匹配的依据。
   - license：按需填写。
   - 字段格式拿不准时，调用 skill-creator 核实。

4. 开发正文与内容
   - SKILL.md 正文写面向执行的简明操作指南（建议 <500 行），细节下沉到子文件。
   - 确定性重逻辑写到 scripts/，脚本须能独立运行。
   - 大段说明、示例、文档写到 references/。
   - 静态数据/配置写到 assets/。

5. 查证与试跑
   - 涉及外部库或陌生领域时，用可用的检索工具查一手资料，沉淀进 references/。
   - 在工作空间实际运行 scripts/ 验证可执行性。

6. 自检交付
   - 核对：frontmatter 完整（name/description 非空）、正文精简、脚本可跑、命名一致、无模板占位符。
   - 把所有变更真实写入工作空间，并给出文件树总览 + 变更摘要。

## 原则
- 只在已有模板上增量开发，不覆盖、不推倒重来。
- 优先沉淀一手资料，而非凭记忆编造。
- 不过度设计，只满足明确需求。