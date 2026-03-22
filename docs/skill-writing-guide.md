# Skill 写作指南

这份文档面向 OpenClaw / AgentSkills 的作者，目标不是写“很会说话”的 prompt，而是写 **可触发、可维护、可审计** 的 skill。

## 1. Skill 是什么

一个 skill 通常至少包含一个 `SKILL.md`，也可以带：

```text
my-skill/
├── SKILL.md
├── scripts/
├── references/
└── assets/
```

最小有效 skill 的关键不是字多，而是：

- 名称清楚
- description 清楚
- 工作流清楚

## 2. 一个最小可用的 `SKILL.md`

```markdown
---
name: example-skill
description: 当用户要总结纯文本报告并提取行动项时使用此 skill。
metadata: { "openclaw": { "requires": { "bins": ["sed"] } } }
---

# Example Skill

## 何时使用

- 用户要总结纯文本报告
- 用户要提取行动项

## 何时不要用

- 二进制文件
- 需要 OCR 的 PDF

## 工作流

1. 读取输入。
2. 确认目标。
3. 提取前三个行动项。
4. 先给短摘要，再给 bullet。
```

## 3. 最重要的是 description

OpenClaw 选择 skill 时，最先看的就是 `name` 和 `description`。

所以一个差 description 会直接让 skill 触发失败。

### 不好的写法

```yaml
description: Helps with files.
```

问题：

- 太泛
- 没说清什么时候触发
- 没说清文件类型

### 更好的写法

```yaml
description: 读取、整理并总结 PDF 发票。当用户提到发票抽取、金额汇总、到期日或发票分类时使用。
```

## 4. 好 skill 的四个特征

### 触发清楚

一看 description 就知道：

- 什么时候该用
- 什么时候别用
- 它到底解决什么问题

### 内容克制

不要把模型本来就知道的常识全塞进去。

`SKILL.md` 应该主要放：

- 领域限制
- 特殊工作流
- 容易踩的坑
- 需要优先使用的工具

### 写工作流，不写气氛组文案

差 skill 常见写法：

- 要有帮助
- 要认真
- 要准确

更好的写法：

- 先看本地文件
- 先验证依赖是否存在
- 优先使用某个脚本
- 有副作用时先确认

### 明写安全边界

如果 skill 会写数据、发消息、改配置、删文件，就要写出来。

例如：

- 删除前确认
- 外发前确认
- 先做只读检查
- 不要把原始用户输入直接拼进 shell 命令

## 5. 什么时候该拆到 `scripts/`

当某段逻辑：

- 经常重复
- 很脆弱
- 正确性要求高
- 用 shell one-liner 很容易翻车

就别硬写在 prose 里了，直接上脚本。

常见场景：

- PDF 处理
- 文档转换
- 稳定解析
- API 封装

## 6. 什么时候该拆到 `references/`

当你有大段说明、schema、示例、表格时，不要全部塞进 `SKILL.md`。

可以把：

- 长文档
- API 参考
- 错误码表
- 详细示例

放到 `references/`，只在需要时再读取。

## 7. OpenClaw 里几个容易忽略的点

### frontmatter 要尽量简单

尤其是 `metadata`，最好保持简单、紧凑、清晰。

### 常见 gating 信息

常见字段包括：

- `requires.bins`
- `requires.anyBins`
- `requires.env`
- `requires.config`
- `install`
- `os`
- `homepage`

这些信息很重要，因为它们直接影响 skill 是否 eligible。

### 会话对 skill 有快照行为

当 session 已经开始后，skill 文件或配置改了，不一定会立即生效。

很多情况下需要：

- 新开 session
- 刷新 skills
- 或重启 gateway

## 8. 常见反模式

### 反模式 1：万能 prompt

什么都想做，最后什么都触发不准。

### 反模式 2：把风险藏起来

明明会写、会删、会外发，却一句不提。

### 反模式 3：把常识写成大段废话

占上下文，不增加信息量。

### 反模式 4：不写失败路径

一个好 skill 不只说明顺利时怎么做，也要说明什么时候该停。

## 9. 一个简单 checklist

提交 skill 前，问自己：

- description 是否足够具体？
- 何时使用 / 不使用是否清楚？
- 是否写清依赖、环境变量和副作用？
- 是否把脆弱逻辑拆到了脚本？
- 是否给后来者留下了可维护的结构？
