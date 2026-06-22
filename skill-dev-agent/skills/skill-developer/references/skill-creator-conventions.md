# Skill 规范约定（参考 skill-creator）

汇总技能（Skill）的格式规范，开发时对照。权威来源为 skill-creator 技能；如有出入以 skill-creator 为准。

## SKILL.md 结构
顶部 YAML frontmatter，字段：
- name（必填）：技能唯一标识，kebab-case 全小写，如 weather-query。
- description（必填）：功能 + 触发条件 + 关键词，用于检索匹配。不得为空。
- license（选填）：MIT / Apache-2.0 / Proprietary。
frontmatter 之下为面向执行的操作指南正文（建议 <500 行）。

## 目录约定
- references/：详细参考文档（大段说明、示例、边界情况）。
- scripts/：可执行辅助脚本（确定性重逻辑）。
- assets/：静态数据/配置。

## 渐进式披露
SKILL.md 只放最小可用信息；细节按需下沉到子文件，运行时才加载，避免上下文膨胀。