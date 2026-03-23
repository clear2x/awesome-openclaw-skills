# Awesome OpenClaw Skills

> 一个尽量诚实、尽量中文、尽量低风险的 OpenClaw skill 精选仓库。

这个项目做三件事：

- 精选值得研究、安装或改写的 skill
- 用中文说明 skill 为什么有价值、什么时候该用、什么时候别乱用
- 沉淀 OpenClaw / AgentSkills 的写法、收录标准与风险边界

## 当前进度

- 主清单已扩到 **100 项 skill 中文导读**：见 `lists/awesome-skills.md`
- 其中 **96 项已核对**：既包含本机 `SKILL.md` / 本地缓存，也包含能直接回到官方公开技能页的一手资料
- 另有 **4 项保留为 `部分核对`**：能确认名称、族群或公开 registry 条目存在，但还缺完整 `SKILL.md` / 安装链路 / 关键依赖说明
- 原先 **43 项 `待核对`** 已在上轮全部完成一轮公开来源核对：其中 **38 项升级为 `已核对`**、**5 项升级为 `部分核对`**；本轮再把 **4 项飞书条目** 和 **5 项用户明确判定可直接通过的条目** 从 `部分核对` 升级为 `已核对`
- 文档已补为中文优先：README、贡献说明、写作指南、rules 指南、收录标准、进度文档均已同步
- 本轮公开 / 本地混合核对记录：`docs/pending-verification-notes.md`

## 这个仓库的立场

这不是一个“把所有 skill 链接全扔进来”的大杂烩。

我更在意的是：

- **是否真有用**
- **是否讲得清楚**
- **是否低风险或至少把风险说清楚**
- **是否适合公开推荐**

所以这里会同时收录两类内容：

1. **优先推荐**：已核对、质量较高、边界相对清晰的 skill（既包括本地一手资料，也包括官方公开技能页可回溯的条目）
2. **观察候选**：已经纳入路线图、但还需要继续补来源或复核依赖的 skill（其中一部分已做到 `部分核对`）

如果某个 skill 名称本身是英文，仓库里仍然保留英文名；但解释、导读、判断尽量统一为中文。

## 优先来源

本仓扩充仍然优先使用本地资料；当本地不足时，再补官方 registry / 官方仓库的一手页面：

- 本地 `@larksuite/openclaw-lark` 包缓存
- 本地已安装的 workspace skills
- 本地 system skills
- 本地 vendor skill 仓库：`/home/node/.codex/vendor_imports/skills`
- 本地 `.openclaw/` 运行态痕迹与 `.clawhub/lock.json`
- 官方 ClawHub 公共技能页：`https://clawhub.ai/<owner>/<slug>`
- 仓库既有的 `docs/100-skills-plan.md`

这样做的好处是：

- 可追溯
- 不容易误收危险 skill
- 公开来源也尽量落在 registry / 官方页面，不靠低信任二手转述
- 便于后续继续核对依赖、触发条件与维护状态

## 仓库结构

- `lists/awesome-skills.md`：主清单，当前为 100 项中文导读
- `docs/100-skills-plan.md`：进度、来源拆分、下一步计划
- `docs/pending-verification-notes.md`：本轮公开 / 本地混合核对的来源、依赖与风险备注
- `docs/curation-policy.md`：收录 / 排除标准
- `docs/skill-writing-guide.md`：怎么写一个好 skill
- `docs/rules-guide.md`：怎么写具体、可执行的 rules
- `docs/research-memo.md`：本仓当前判断与来源备忘
- `examples/example-skill.md`：最小中文示例
- `CONTRIBUTING.md`：贡献方式与提交流程

## 快速开始

### 先看主清单

- `lists/awesome-skills.md`

### 再看方法文档

- `docs/curation-policy.md`
- `docs/skill-writing-guide.md`
- `docs/rules-guide.md`

### OpenClaw 相关命令

```bash
openclaw skills list
openclaw skills list --eligible
openclaw skills check
```

如果你的环境支持 ClawHub / skill 安装流，也可以参考：

```bash
clawhub install <skill-slug>
```

## 收录时我优先看什么

我更倾向于优先收这些：

- 文档与知识处理
- GitHub / 开发工作流
- 系统诊断与排障
- 协作平台集成
- 轻量多媒体与格式处理

我会谨慎对待这些：

- 凭据读取或秘密操作边界不清的 skill
- 大规模外发 / 骚扰式自动化
- 对系统有破坏性却没有保护栏的 skill
- 把“高风险自动化”包装成“高效率”的 skill

## 接下来还会补什么

- 为剩余 **4 个 `部分核对`** 条目继续补独立 `SKILL.md` / 上游仓库 / 安装链路
- 给高风险但已核对的条目单独拉出“谨慎启用”分组
- 给更多 skill 补安装前置条件与风险标签
- 增加“适合抄写的 skill 写法模板”
- 给观察候选做更明确的推荐 / 不推荐判断

## 贡献

欢迎提 PR，但请把重点放在“质量、清晰度、安全边界”，不是只堆名字。

贡献前建议先看：

- `CONTRIBUTING.md`
- `docs/curation-policy.md`

## License

MIT
