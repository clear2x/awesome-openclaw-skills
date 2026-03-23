# 100 Skills 进度文档

> 目标不是机械凑数，而是把仓库推进到“有 100 项中文导读、且来源透明”的可交付状态。

## 当前状态

- 主清单：`lists/awesome-skills.md`
- 当前条目数：**100**
- 已核对条目：**96**
- 部分核对条目：**4**
- 待二次核对条目：**0**

## 这一轮主要来源

### 1. 本地 curated cache

来源：`codex_config/vendor_imports/skills-curated-cache.json`

- 已直接消化 **35** 个 skill
- 优点：有 description、repoPath，来源可追溯
- 适合优先写成高质量中文导读

### 2. 本地 OpenClaw / Lark skill 目录

来源：本机 `@larksuite/openclaw-lark/skills`

- 已直接消化 **9** 个 skill
- 以飞书文档、日历、多维表格、任务、权限排障为主
- 优点：说明细、约束多、很适合拿来做“怎么写好 skill”的参考样本

### 3. 本地 workspace / system skills

来源：工作区 `skills/` 与 `codex_config/skills/.system/`

- 去重后新增 **5** 个独立条目
- 包括 `skill-creator`、`skill-installer`、`self-improvement`、`video-watcher`、`tiktok-video-analyzer`

### 4. 仓库既有路线图候选

来源：旧版 `docs/100-skills-plan.md` 中已经列出的名称

- 这一轮选入 **51** 个待核对候选
- 已补中文导读
- 其中 **8** 个先靠本机线索升级为 `部分核对`
- 剩余 **43** 个已在本轮补官方公开来源
- 其中 **38** 个升级为 `已核对`，**5** 个升级为 `部分核对`
- 原 51 个路线图候选现已全部脱离 `待核对`

## 本轮新增二次核对来源

### 1. 本地 `@larksuite/openclaw-lark` 包缓存

来源：`/home/node/.npm/_npx/be1a8fd12ade5f98/node_modules/@larksuite/openclaw-lark`

- 命中 `feishu-doc`、`feishu-drive`、`feishu-perm`、`feishu-wiki`
- 不仅能看到 `src/tools/oapi/drive` / `wiki` / `oauth` 等实现目录，还能直接回到官方插件 README、npm 包元数据与独立 `SKILL.md`
- 价值：已经足够补出安装链路、权限范围与典型工作流，因此这 4 项已从 `部分核对` 升级为 `已核对`

### 2. 本地 vendor skill 仓库

来源：`/home/node/.codex/vendor_imports/skills`

- 命中 `notion` 家族线索：`notion-knowledge-capture`、`notion-meeting-intelligence`、`notion-research-documentation`、`notion-spec-to-implementation`
- 上游 remote 在本机指向 `https://github.com/openai/skills.git`
- 价值：能直接补 `Notion MCP` 接入、OAuth 与页面写入工作流；在用户明确认可其安全口径后，已作为可核对通过的族群入口纳入 `已核对`

### 3. 本地 OpenClaw 运行态与官方文档

来源：`/home/node/.openclaw/` 与 `/app/docs/`

- 命中 `canvas`、`gemini`、`clawhub`
- `canvas` 可直接回到官方文档中的 Gateway canvas host、node canvas 命令、工作区 `canvas/` 目录与安全说明；在用户明确认可安全口径后，已纳入 `已核对`
- `clawhub` 可直接回到官方文档中的搜索、安装、更新、同步、发布、`.clawhub/lock.json` 与工作区加载机制；在用户明确认可安全口径后，已纳入 `已核对`
- `gemini` 当前更接近模型 provider / CLI / runtime 入口，但在用户明确认可安全口径后，已纳入 `已核对`

### 4. 本地 ClawHub 安装锁

来源：`/home/node/.openclaw/workspace/.clawhub/lock.json`

- 可确认本机存在安装锁与已装 skill 记录
- 当前已装示例为 `bilibili-youtube-watcher` 与 `tiktok-video-analyzer`
- 与官方 ClawHub 文档组合后，已足够支撑 `clawhub` 作为已核对条目

### 5. 官方 ClawHub 公共技能页

来源：`https://clawhub.ai/<owner>/<slug>`

- 上轮直接命中原先 **43** 个 `待核对` 条目中的全部条目
- 其中 **38** 个页面能直接读到 skill 说明、依赖 / 凭据线索、安装方式或安全审计摘要，因此升级为 `已核对`
- 另有 **5** 个只返回公开占位页或泛化描述，因此仅升级为 `部分核对`
- 其中 `gh-issues` 在用户明确认可安全口径后，已从 `部分核对` 升级为 `已核对`
- 价值：既保留“只信官方 / registry 页面”的保守标准，又能把原路线图名字从空占位推进到可解释状态

## 为什么这样分层

这样做有几个好处：

- 先把仓库做成 **能看、能用、能继续扩写** 的中文资料库
- 对没核到一手资料的条目保持诚实，不乱吹、不乱推
- 比“全都待核对”更细一层：本地一手资料和官方公开技能页都可以作为保守的一手来源
- 方便下一轮直接针对剩余 4 个 `部分核对` 条目补完整安装链路与上游仓库

## 下一步建议

### 第一优先级

- 给剩余 4 个 `部分核对` 条目补独立 `SKILL.md`、上游仓库与安装链路
- 为高风险但已核对的条目单独写“谨慎启用”说明
- 把最容易闭环的 `部分核对` 条目继续升级为 `已核对`

### 第二优先级

- 给主清单增加“推荐等级”或“最值得先看 Top 20”
- 给高风险能力单独拉出一个“谨慎收录”分组
- 把重复概念（例如图像生成、转写、笔记系统）做交叉对照

### 第三优先级

- 为主清单补安装示例或来源链接
- 增加“值得模仿的 skill 写法”专题
- 增加“反例 / 反模式”文档，讲清楚哪些 skill 不该收

## 暂不并入本轮主清单的额外候选

以下名字目前仍保留在观察池，暂未并入 100 项主清单：

- `self-improving-agent`（当前主清单已使用规范名 `self-improvement`）
- `gog`
- `imsg`
- `lobster`
- `mcporter`
- `peekaboo`
- `songsee`
- `voice-call`
- `ordercli`
- 以及个别仅为别名或与现有条目高度重叠的名称

## 本轮交付定义

如果明天早上只看一次仓库，我希望用户至少能直接拿到这些结果：

- 一个中文 README
- 一份 100 项 skill 中文导读清单
- 一套中文的贡献、收录、写作与 rules 文档
- 一个诚实的进度面板，知道哪些已经核过、哪些只是 `部分核对`、哪些还要继续做
