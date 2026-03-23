# Awesome OpenClaw Skills 中文清单

> 当前版本：**100 项 skill 中文导读**。

## 状态说明

- `已核对`：本机能找到 `SKILL.md`、本地缓存，或能直接回到本地一手资料
- `部分核对`：已找到本地同名痕迹、同族上游或运行态证据，但还没核到独立 `SKILL.md` / 完整安装链路
- `待核对`：已经纳入本仓路线图，先补中文导读，后续继续核对来源 / 依赖 / 维护状态
- 风险标签是仓库视角的公开推荐风险，不代表 skill 本身绝对安全

## A. 已核对：OpenClaw / 系统 / 工作区技能

- [已核对][低] `skill-creator`：用于创建或重构 skill，重点是触发描述、目录结构和渐进披露。
- [已核对][低] `skill-installer`：用于列出或安装技能仓库里的 skill，适合做本地能力扩展。
- [已核对][低] `openai-docs`：查询 OpenAI 官方文档与 API 用法，适合 docs-first 的最新核对。
- [已核对][低] `self-improvement`：把错误、纠正和能力缺口写入学习日志，方便 agent 持续改进。
- [已核对][低] `video-watcher`：抓取 YouTube / Bilibili 视频字幕并做总结、问答或信息抽取。
- [已核对][低] `tiktok-video-analyzer`：对 TikTok、YouTube、Instagram 等视频做转录和内容分析。
- [已核对][中] `feishu-bitable`：管理飞书多维表格的表、字段、视图与批量记录操作。
- [已核对][中] `feishu-calendar`：管理飞书日历与日程，适合会议安排、忙闲查询与参会人处理。
- [已核对][低] `feishu-channel-rules`：给飞书频道补行为规则与上下文约束，减少 agent 在群聊里失真。
- [已核对][中] `feishu-create-doc`：新建飞书文档并初始化内容结构，适合模板化文档起草。
- [已核对][低] `feishu-fetch-doc`：读取飞书文档内容，适合总结、问答与内容核对。
- [已核对][中] `feishu-im-read`：读取飞书消息与上下文，适合做会话整理和消息理解。
- [已核对][中] `feishu-task`：管理飞书任务与任务清单，适合分派、跟进和任务流整理。
- [已核对][低] `feishu-troubleshoot`：专门排查飞书插件与权限问题，适合授权异常和连接故障定位。
- [已核对][中] `feishu-update-doc`：按追加、覆盖、替换、定位插入等模式更新飞书文档内容。

## B. 已核对：开发、部署与工程化

- [已核对][低] `aspnet-core`：围绕 ASP.NET Core 应用的构建、重构、性能、认证与部署给出官方导向建议。
- [已核对][低] `chatgpt-apps`：用于搭建或排查 ChatGPT Apps SDK 项目，覆盖 MCP server 与 widget UI。
- [已核对][中] `cloudflare-deploy`：把应用部署到 Cloudflare Workers / Pages 及相关平台服务。
- [已核对][低] `develop-web-game`：为网页小游戏提供“改一点、测一点、看截图、查控制台”的稳定循环。
- [已核对][低] `figma`：通过 Figma MCP 拉设计上下文、变量、截图和资产，再翻译成代码。
- [已核对][低] `figma-implement-design`：强调 1:1 落地 Figma 设计稿，适合像素级实现组件或页面。
- [已核对][低] `gh-address-comments`：针对当前分支的 GitHub PR 评论做集中处理与回复修订。
- [已核对][中] `gh-fix-ci`：用 `gh` 排查 GitHub Actions 失败原因，再按批准后的方案修复。
- [已核对][中] `linear`：读取、创建和更新 Linear 任务、项目与协作流程。
- [已核对][中] `netlify-deploy`：把网站或前端项目部署到 Netlify，适合预览和正式发布。
- [已核对][低] `notion-knowledge-capture`：把聊天、决定和知识点沉淀到结构化 Notion 页面。
- [已核对][低] `notion-meeting-intelligence`：结合 Notion 背景资料准备会议议程、预读材料和上下文。
- [已核对][低] `notion-research-documentation`：跨多个 Notion 页面做调研并整理成结构化文档。
- [已核对][低] `notion-spec-to-implementation`：把 Notion 规格说明拆成实现计划、任务和跟踪项。
- [已核对][低] `playwright`：在终端里驱动真实浏览器，适合导航、截图、抓数据和 UI 流调试。
- [已核对][中] `playwright-interactive`：保留可持续交互的浏览器会话，适合迭代式 UI 排障。
- [已核对][中] `render-deploy`：分析代码库并生成 Render 部署蓝图或 Dashboard deeplink。
- [已核对][低] `sentry`：以只读方式查看 Sentry 报错、事件和健康信息。
- [已核对][中] `security-best-practices`：只在用户明确要求时做安全最佳实践审查与改进建议。
- [已核对][中] `security-ownership-map`：基于 Git 历史做敏感代码归属、bus factor 与安全 ownership 分析。
- [已核对][中] `security-threat-model`：围绕仓库实际代码做威胁建模、资产与缓解措施梳理。
- [已核对][中] `vercel-deploy`：将应用发布到 Vercel，适合快速上线和预览部署。
- [已核对][低] `winui-app`：围绕 WinUI 3 应用的搭建、调试、导航、主题和打包给出指导。
- [已核对][中] `yeet`：在用户明确要求时，一次性完成 stage、commit、push 和 PR 打开流程。

## C. 已核对：文档、格式、多模态

- [已核对][低] `doc`：读取、创建或编辑 `.docx` 文档，尤其适合重视版式与布局的场景。
- [已核对][低] `pdf`：处理 PDF 的读取、生成、抽取和渲染检查，适合版面敏感任务。
- [已核对][中] `screenshot`：在系统级截全屏、窗口或区域截图，适合工具自身无截图能力时兜底。
- [已核对][低] `slides`：创建或修改 `.pptx` 幻灯片，适合演示稿生成与版式诊断。
- [已核对][低] `spreadsheet`：处理 `.xlsx` / `.csv` / `.tsv`，适合公式、格式和数据分析型工作流。
- [已核对][中] `imagegen`：调用 OpenAI 图片能力做生成、编辑、抠图或批量变体。
- [已核对][中] `sora`：调用 Sora 视频接口做生成、remix、查询、下载和删除。
- [已核对][中] `speech`：把文本转成语音旁白，适合配音、可访问性朗读与批量播报。
- [已核对][低] `transcribe`：把音视频转成文本，并可选做说话人区分与已知说话人提示。
- [已核对][低] `jupyter-notebook`：创建或整理 `.ipynb`，适合实验、教程和探索式分析。

## D. 协作平台与工作流候选

> 本节按 `部分核对` / `待核对` 分层：前者已补到本地来源线索，后者仍以路线图占位为主。

- [待核对][高注意] `1password`：大概率用于密码库或凭据读取，公开推荐时必须把权限边界写清楚。
- [待核对][中] `apple-notes`：适合把 Apple Notes 作为轻量笔记来源或写入目标。
- [待核对][中] `apple-reminders`：适合读取、创建和管理 Apple Reminders 待办事项。
- [待核对][低] `bear-notes`：面向 Bear 笔记的读取、整理或知识摘录流程。
- [待核对][低] `blogwatcher`：更像博客更新跟踪器，适合定期观察订阅源或作者动态。
- [待核对][中] `bluebubbles`：适合围绕 BlueBubbles / iMessage 桥接做消息整合。
- [部分核对][中] `clawhub`：本机已见 `.clawhub/lock.json` 安装锁；能确认本地确有安装流，但暂未核到独立 skill 包或发布规范。
- [待核对][低] `coding-agent`：更偏“编码代理工作流封装”，适合把常见研发步骤打包。
- [待核对][中] `discord`：适合 Discord 频道、消息和社群协作自动化，但要严格控制外发行为。
- [部分核对][低] `feishu-doc`：本地 `@larksuite/openclaw-lark` 已含 doc 搜索与 doc comment/media 相关实现；当前更像文档能力总入口，与 `feishu-create-doc` / `feishu-fetch-doc` / `feishu-update-doc` 同族。
- [部分核对][中] `feishu-drive`：本地 `@larksuite/openclaw-lark` 源码已含 `src/tools/oapi/drive`；安装链路走 `npm` 包，依赖飞书 OAuth 与对应 scope。
- [部分核对][高注意] `feishu-perm`：本地包已含 `oauth` / `oauth-batch-auth` 与权限报错处理；价值高，但必须持续强调 scope、授权卡片与账号一致性。
- [部分核对][中] `feishu-wiki`：本地 `@larksuite/openclaw-lark` 源码已含 `src/tools/oapi/wiki`；与飞书知识库节点、空间操作同族。
- [待核对][中] `gh-issues`：面向 GitHub issue 的查看、创建、分派与追踪。
- [待核对][中] `github`：面向 GitHub 仓库、PR、issue、release 的通用研发协作入口。
- [待核对][低] `himalaya`：从名字看更像邮件客户端集成，适合邮件读取或草稿辅助。
- [部分核对][中] `notion`：本机已找到 4 个 OpenAI curated Notion skill；因此这个名字更适合作为族群入口，而不是单独包装成已核对 skill。
- [待核对][低] `session-logs`：适合整理 agent 会话日志，便于回放、复盘或审计。
- [待核对][中] `slack`：适合 Slack 频道与消息流自动化，但必须避免打扰式或代理式发言。
- [待核对][中] `things-mac`：看名字更像 Things for Mac 的任务管理集成。
- [待核对][中] `trello`：面向 Trello 卡片、列表与看板的管理与同步。

## E. 知识、搜索、内容与多媒体候选

- [部分核对][中] `canvas`：本机已见 `.openclaw/canvas/index.html` 的 OpenClaw Canvas 交互页；当前更像运行时 surface，不足以当作独立 skill 推荐。
- [部分核对][中] `gemini`：本机已见 `.openclaw/agents/gemini/sessions/` 运行痕迹；能确认存在 agent/runtime 入口，但尚未核到独立 skill 包。
- [待核对][低] `gifgrep`：更像 GIF 搜索、筛选或素材定位工具，适合内容工作流。
- [待核对][低] `model-usage`：适合统计模型调用量、成本、配额或使用趋势。
- [待核对][低] `nano-pdf`：名字提示它更像轻量 PDF 处理器，可能适合小型抽取或拆分任务。
- [待核对][中] `obsidian`：围绕 Obsidian vault 的知识组织、链接和笔记整合。
- [待核对][中] `openai-image-gen`：与图像生成相关，但应继续核对其与 `imagegen` 的差异与定位。
- [待核对][低] `openai-whisper`：偏向 Whisper 本地/CLI 版语音转写能力。
- [待核对][低] `openai-whisper-api`：偏向基于 API 的语音转写或音频理解流程。
- [待核对][中] `prose`：更像面向写作润色、改写和风格调整的文字工具。
- [待核对][中] `sag`：已在原路线图中出现，通常与语音合成或播报相关，需继续核对具体实现。
- [待核对][低] `sherpa-onnx-tts`：更像本地 TTS 能力封装，适合离线语音生成场景。
- [待核对][低] `sonoscli`：面向 Sonos 音响控制与播放状态查询。
- [待核对][低] `spotify-player`：适合查询或控制 Spotify 播放器状态。
- [待核对][低] `summarize`：通用摘要 skill，适合长文、页面或日志的快速浓缩。
- [待核对][中] `tavily`：通常与搜索 API 集成有关，适合检索增强型工作流。
- [待核对][低] `video-frames`：从视频中抽取关键帧，适合做内容回顾与视觉分析。
- [待核对][低] `weather`：天气查询类轻量 skill，适合演示“范围小但触发清晰”的写法。

## F. 待核对：终端、设备、系统与工具候选

- [待核对][中] `acp-router`：更像多 agent / 多工具之间的路由与协议桥接能力，后续应补一手来源说明。
- [待核对][低] `blucli`：从名字看像蓝牙设备管理或扫描的命令行工具封装。
- [待核对][低] `camsnap`：倾向于摄像头抓拍或图像采集，需继续核对权限边界。
- [待核对][低] `diffs`：更偏差异比较、文件比对或变更摘要。
- [待核对][低] `eightctl`：看命名像内部控制台或运维 CLI 封装，需要后续补来源说明。
- [待核对][低] `goplaces`：可能围绕地点搜索、路线或地理位置候选列表构建。
- [待核对][中] `healthcheck`：系统健康检查与问题定位类 skill，通常价值高但需要保护栏。
- [待核对][中] `openhue`：大概率面向智能灯或家庭设备集成。
- [待核对][低] `oracle`：从命名看更像 Oracle 数据库相关操作入口，后续应核对是否适合公开推荐。
- [待核对][低] `tmux`：适合多终端会话编排、面板管理和会话恢复。
- [待核对][低] `wacli`：名字提示它是某个命令行客户端包装器，后续需补一手定义。
- [待核对][低] `xurl`：适合对 URL 做请求、探测或内容抓取。

## 当前结论

- 这 100 项已经足够把仓库从“方向说明”推进到“可读的中文导览”阶段。
- 这一轮已把原 51 个候选拆成 `8 个部分核对 + 43 个待核对`，信任边界比只写“待核对”更清楚。
- 下一步最值得做的是：继续给剩余 43 个待核对条目补一手来源和依赖，再把其中一部分升级为 `部分核对` 或 `已核对`。
