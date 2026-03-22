# 中文示例 Skill

这是一个尽量干净、低膨胀的最小参考 skill。

```text
example-skill/
└── SKILL.md
```

```markdown
---
name: example-skill
description: 当用户要总结纯文本报告并提取前三个行动项时使用。
metadata: { "openclaw": { "requires": { "bins": ["sed"] } } }
---

# Example Skill

## 何时使用

- 用户要求总结纯文本报告
- 用户要求抽取行动项

## 何时不要用

- 二进制文件
- 需要 OCR 的 PDF
- 电子表格或幻灯片

## 工作流

1. 读取文件。
2. 找到主目标。
3. 提取前三个行动项。
4. 先返回短摘要，再返回 bullet。
5. 如果文件不是纯文本，就停止并说明原因。
```
