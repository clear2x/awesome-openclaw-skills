# Awesome OpenClaw Skills 中文清单

> 当前版本：**100 项 skill 中文导读**。

## 状态说明

- `已核对`：本机能找到 `SKILL.md`、本地缓存，或能直接回到官方 registry / 官方仓库里的公开技能页与安装说明
- `部分核对`：已找到本地同名痕迹、同族上游、运行态证据，或官方公开占位页，但还没核到完整 `SKILL.md` / 安装链路 / 关键依赖说明
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

- 本节现在混合两类条目：能直接回到公开 ClawHub 技能页并补足说明的 `已核对`，以及只核到公开占位页 / 本地族群线索的 `部分核对`。

- [已核对][高注意] `1password`：围绕 1Password CLI（`op`）做安装、登录、多账户切换与 secret 读取 / 注入；很实用，但必须防止 tmux pane 捕获或日志泄露敏感信息。
- [已核对][中] `apple-notes`：通过 `memo` CLI 在 macOS 创建、搜索、移动、导出 Apple Notes，适合轻量笔记整理。
- [已核对][中] `apple-reminders`：通过 `remindctl` 在 macOS 管理提醒事项，支持列表、日期过滤与 JSON 输出。
- [已核对][中] `bear-notes`：通过 `grizzly` CLI 创建、搜索和管理 Bear 笔记；依赖 Bear token，公开推荐时要把 token 文件说明写清楚。
- [已核对][低] `blogwatcher`：用 `blogwatcher` CLI 跟踪 RSS / Atom / 博客更新，适合订阅源观察。
- [已核对][中] `bluebubbles`：面向 BlueBubbles 外部频道插件的构建与更新，适合 iMessage 桥接接入。
- [部分核对][中] `clawhub`：本机已见 `.clawhub/lock.json` 安装锁；能确认本地确有安装流，但暂未核到独立 skill 包或发布规范。
- [部分核对][低] `coding-agent`：官方 ClawHub 已有同名公开页，但当前只见占位信息；能确认名称存在，仍缺具体说明、依赖与风险边界。
- [已核对][高注意] `discord`：通过 Discord 工具发消息、反应、投票、线程 / 权限 / 审核与媒体上传；涉及 bot token 和本地文件上传时要严格防外发。
- [部分核对][低] `feishu-doc`：本地 `@larksuite/openclaw-lark` 已含 doc 搜索与 doc comment/media 相关实现；当前更像文档能力总入口，与 `feishu-create-doc` / `feishu-fetch-doc` / `feishu-update-doc` 同族。
- [部分核对][中] `feishu-drive`：本地 `@larksuite/openclaw-lark` 源码已含 `src/tools/oapi/drive`；安装链路走 `npm` 包，依赖飞书 OAuth 与对应 scope。
- [部分核对][高注意] `feishu-perm`：本地包已含 `oauth` / `oauth-batch-auth` 与权限报错处理；价值高，但必须持续强调 scope、授权卡片与账号一致性。
- [部分核对][中] `feishu-wiki`：本地 `@larksuite/openclaw-lark` 源码已含 `src/tools/oapi/wiki`；与飞书知识库节点、空间操作同族。
- [部分核对][中] `gh-issues`：官方 ClawHub 已有同名公开页，但当前只见占位信息；能确认这是 registry 条目，仍未核到具体操作范围。
- [已核对][中] `github`：通过 `gh` CLI 处理仓库、PR、issue、Actions 与高级 API 查询，适合通用研发协作。
- [已核对][高注意] `himalaya`：基于 `himalaya` CLI 管理 IMAP / SMTP 邮件，支持读信、写信、回复、转发和附件；涉及账号配置与密码命令时要格外谨慎。
- [部分核对][中] `notion`：本机已找到 4 个 OpenAI curated Notion skill；因此这个名字更适合作为族群入口，而不是单独包装成已核对 skill。
- [已核对][低] `session-logs`：用 `jq` / `rg` 搜索并分析自己的 session logs，适合回放、复盘与审计。
- [已核对][中] `slack`：通过 Slack 工具做反应、置顶等频道操作；价值明确，但 token 与工具依赖需要提前声明。
- [已核对][中] `things-mac`：通过 `things` CLI 读写 Things 3 任务、项目与标签；读取本地数据库时要注意 Full Disk Access。
- [已核对][中] `trello`：通过 Trello REST API 管理看板、列表与卡片；依赖 API key / token 与 `jq`。

## E. 知识、搜索、内容与多媒体候选

- [部分核对][中] `canvas`：本机已见 `.openclaw/canvas/index.html` 的 OpenClaw Canvas 交互页；当前更像运行时 surface，不足以当作独立 skill 推荐。
- [部分核对][中] `gemini`：本机已见 `.openclaw/agents/gemini/sessions/` 运行痕迹；能确认存在 agent/runtime 入口，但尚未核到独立 skill 包。
- [已核对][低] `gifgrep`：用 `gifgrep` 搜索 GIF、下载素材并抽取静帧 / 雪碧图，适合内容工作流。
- [已核对][低] `model-usage`：基于 CodexBar 本地 cost JSON 汇总模型使用量与成本，适合按模型做用量拆分。
- [已核对][低] `nano-pdf`：通过 `nano-pdf` CLI 用自然语言编辑 PDF，适合轻量单页改动。
- [已核对][中] `obsidian`：通过 `obsidian-cli` 操作 Obsidian vault；会读取用户的 Obsidian 配置和 vault 路径，需明确文件边界。
- [已核对][中] `openai-image-gen`：通过 OpenAI Images API 批量生成图片并输出本地 gallery；依赖 API key，且 Base URL 覆盖要谨慎。
- [已核对][低] `openai-whisper`：用本地 Whisper CLI 做语音转写，不依赖 API key。
- [已核对][中] `openai-whisper-api`：通过 OpenAI Audio Transcriptions API 转写音频；依赖 `OPENAI_API_KEY`，且会把音频上传到外部服务。
- [已核对][高注意] `prose`：OpenProse / VM 风格 skill pack，支持拉取并执行 `.prose` 程序；公开页已被 ClawHub 标成 suspicious，必须谨慎。
- [已核对][中] `sag`：通过 ElevenLabs 做 TTS，走 `sag` CLI 的 `say` 风格体验；依赖 API key。
- [部分核对][低] `sherpa-onnx-tts`：官方 ClawHub 已有同名公开页，但当前只见占位信息；能确认条目存在，仍缺实现与安装细节。
- [已核对][中] `sonoscli`：通过 `sonos` CLI 控制 Sonos 音箱的发现、播放、分组与音量；可选接 Spotify 搜索。
- [已核对][低] `spotify-player`：用 `spogo` 或 `spotify_player` 做终端内 Spotify 搜索与播放控制。
- [已核对][中] `summarize`：通过 `summarize` CLI 总结 URL、PDF、图片、音频与 YouTube 内容；依赖外部模型 / 提取服务 key。
- [已核对][高注意] `tavily`：基于 Tavily Search API 做搜索与摘要；公开页已被 ClawHub 标成 suspicious，且 API key 元数据声明不完整。
- [已核对][低] `video-frames`：用 `ffmpeg` 从视频里抽帧或截短片段，适合视觉回顾。
- [已核对][低] `weather`：通过 `curl` 调 `wttr.in` / `Open-Meteo` 查询天气，无需 API key，但会把位置查询发到外网。

## F. 终端、设备、系统与工具候选

- [已核对][高注意] `acp-router`：面向 ACP / ACPX / OpenClaw runtime 的请求路由与修复工作流；公开页已被 ClawHub 标成 suspicious，且运行时会触发 `npm install`、命令执行与网关重启。
- [已核对][低] `blucli`：通过 BluOS CLI（`blu`）做设备发现、播放、分组与音量控制。
- [已核对][中] `camsnap`：抓取 RTSP / ONVIF 摄像头帧图或短片段；价值明确，但本地配置可能保存摄像头凭据，`watch --action` 也会放大执行面。
- [部分核对][低] `diffs`：官方 ClawHub 已有同名公开页，但当前只见占位信息；能确认条目存在，仍缺具体实现说明。
- [已核对][中] `eightctl`：控制 Eight Sleep pod 的状态、温度、闹钟与排程；依赖账号凭据，公开说明里必须把凭据边界讲清楚。
- [已核对][中] `goplaces`：通过 `goplaces` CLI 调 Google Places API（新接口）做搜索、详情、resolve 与 review 查询。
- [已核对][高注意] `healthcheck`：本质是本地 JSON 的饮水 / 睡眠跟踪器，但公开页已被 ClawHub 标成 suspicious，且运行说明依赖内联 `node -e`，应谨慎使用。
- [已核对][中] `openhue`：通过 OpenHue CLI 控制 Philips Hue 灯光与场景，偏家庭 / 办公环境自动化。
- [已核对][高注意] `oracle`：通过 `@steipete/oracle` CLI 打包 prompt 与相关文件，交给第二模型做 review / 调试 / 交叉验证；运行时会 `npx` 下载代码并可能把文件发到外部服务。
- [已核对][高注意] `tmux`：通过 `tmux` 发送按键、抓 pane 输出和等待文本，适合操控交互式 CLI；但也能读到终端里的敏感内容。
- [部分核对][低] `wacli`：官方 ClawHub 已有同名公开页，但当前只见占位信息；能确认它是公开 registry 条目，但功能边界仍未展开。
- [已核对][中] `xurl`：分析 Twitter 内容里的 WordPress / Shopify 客户痛点并产出选题 / 获客线索，偏内容运营而不是通用抓取工具。

## 当前结论

- 这 100 项已经从“路线图占位”推进到“本地资料 + 官方公开技能页混合核对”的中文导览阶段。
- 这一轮已把原来的 43 个 `待核对` 条目全部吃掉：其中 **38** 个升级为 `已核对`，**5** 个升级为 `部分核对`。
- 下一步最值得做的是：继续为 **13** 个 `部分核对` 条目补独立 `SKILL.md` / 上游仓库 / 安装链路，并给高风险条目单独拉出警示分组。
