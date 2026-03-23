# 条目核对记录：公开来源二次核对

> 2026-03-23 这一轮在本机证据之外，补查了官方 ClawHub 公共技能页。只有当公开页能直接提供 skill 说明、依赖 / 凭据线索、安装方式或安全审计摘要时，才升级为 `已核对`；若只有公开占位页，则最多升级为 `部分核对`。随后又补查了本机 Feishu 官方插件 README、npm 包元数据与独立 `SKILL.md`，再把 4 个飞书条目从 `部分核对` 升级为 `已核对`。之后根据用户明确给出的风险口径，再把 `clawhub`、`notion`、`canvas`、`gh-issues`、`gemini` 从 `部分核对` 升级为 `已核对`。

## 状态口径

- `已核对`：本机能找到 `SKILL.md` / 本地缓存，或能直接回到官方 registry / 官方仓库里的公开技能页与安装说明。
- `部分核对`：已找到本地同名痕迹、运行态线索、同族上游，或官方公开占位页，但还没核到完整 `SKILL.md` / 安装链路 / 关键依赖说明。

## 本轮结果

- 原先 **43** 个 `待核对` 条目已全部完成一轮公开来源核对。
- 其中 **38** 个升级为 `已核对`。
- 其中 **5** 个升级为 `部分核对`。
- 随后再把 **4** 个 Feishu 条目从 `部分核对` 升级为 `已核对`。
- 再根据用户明确给出的风险口径，把 **5** 个条目从 `部分核对` 升级为 `已核对`。
- 当前主清单状态：**96 个 `已核对` + 4 个 `部分核对` + 0 个 `待核对`**。

## 新增：由公开技能页升级为 `已核对`（38 项）

### 协作平台与工作流

- `1password`：来源 `https://clawhub.ai/steipete/1password`；依赖 `op`、tmux / `CLAWDBOT_TMUX_SOCKET_DIR`；风险：会话窗格抓取和 secret 注入都很敏感，元数据对环境变量声明也不完整。
- `apple-notes`：来源 `https://clawhub.ai/steipete/apple-notes`；依赖 `memo` CLI 与 macOS Automation 权限；风险：安装说明依赖第三方 Homebrew tap / 上游仓库，且会触达用户笔记内容。
- `apple-reminders`：来源 `https://clawhub.ai/steipete/apple-reminders`；依赖 `remindctl`、macOS Reminders 权限；风险：公开页提到 Homebrew / `pnpm` 构建，但 registry 元数据里未完整展开。
- `bear-notes`：来源 `https://clawhub.ai/steipete/bear-notes`；依赖 `grizzly` CLI、Bear token 文件；风险：token 文件和 `go install ...@latest` 都应当明确告知用户。
- `blogwatcher`：来源 `https://clawhub.ai/steipete/blogwatcher`；依赖 `blogwatcher` CLI；风险：`scan` 会主动抓外部 feed，安装依赖第三方 Go 模块。
- `bluebubbles`：来源 `https://clawhub.ai/kevin19830331/bluebubbles`；依赖 BlueBubbles 网关配置、webhook / plugin 路径；风险：涉及消息桥接、密码和 webhook path，必须和宿主配置一起看。
- `discord`：来源 `https://clawhub.ai/steipete/discord`；依赖 Discord bot token / tool；风险：支持本地文件上传与审核动作，外发边界必须写死。
- `github`：来源 `https://clawhub.ai/steipete/github`；依赖 `gh` CLI（公开页文本里也能看到 `jq`）；风险：认证与 token scope 没在 registry 元数据里明确声明。
- `himalaya`：来源 `https://clawhub.ai/lamelas/himalaya`；依赖 `himalaya` CLI、IMAP / SMTP 配置；风险：配置可含邮箱密码或密码命令，也会处理附件。
- `session-logs`：来源 `https://clawhub.ai/guogang1024/session-logs`；依赖 `jq` / `rg`；风险：会读取本地 session logs，适合自查，不宜默认扩大范围。
- `slack`：来源 `https://clawhub.ai/steipete/slack`；依赖 Slack bot token / slack tool；风险：凭据与工具依赖在元数据里没声明完整。
- `things-mac`：来源 `https://clawhub.ai/steipete/things-mac`；依赖 `things` CLI、本地 Things 数据库、可选 `THINGS_AUTH_TOKEN`；风险：读取数据库时往往需要 Full Disk Access。
- `trello`：来源 `https://clawhub.ai/steipete/trello`；依赖 `curl`、`jq`、`TRELLO_API_KEY` / `TRELLO_TOKEN`；风险：公开页能确认凭据需求，但 registry 元数据没有完整声明。

### 知识、搜索、内容与多媒体

- `gifgrep`：来源 `https://clawhub.ai/steipete/gifgrep`；依赖 GIF provider、可选 `GIPHY_API_KEY` / `TENOR_API_KEY`；风险：会下载远端素材，且安装走第三方 tap / Go 模块。
- `model-usage`：来源 `https://clawhub.ai/steipete/model-usage`；依赖 CodexBar CLI / 本地 cost JSON；风险：主要是读取本地使用量数据，平台兼容性（偏 macOS）要说明。
- `nano-pdf`：来源 `https://clawhub.ai/steipete/nano-pdf`；依赖 `nano-pdf` CLI / `uv` 包来源；风险：公开页提示安装元数据和 registry 展示不完全一致。
- `obsidian`：来源 `https://clawhub.ai/steipete/obsidian`；依赖 `obsidian-cli` 与用户的 Obsidian 配置文件；风险：会读取 `~/Library/Application Support/obsidian/obsidian.json` 来发现 vault，属于明确的家目录访问。
- `openai-image-gen`：来源 `https://clawhub.ai/steipete/openai-image-gen`；依赖 `OPENAI_API_KEY` 与本地脚本；风险：若允许覆盖 `OPENAI_BASE_URL` / `OPENAI_API_BASE`，API key 可能被发往非官方主机。
- `openai-whisper`：来源 `https://clawhub.ai/steipete/openai-whisper`；依赖本地 Whisper CLI；风险：主要是模型缓存和本地音频处理，外发面较小。
- `openai-whisper-api`：来源 `https://clawhub.ai/steipete/openai-whisper-api`；依赖 `curl`、`OPENAI_API_KEY`；风险：会把音频上传到外部服务，且公开页提到把 key 存进本地 JSON 文件要注意权限。
- `prose`：来源 `https://clawhub.ai/mondilo1/prose`；依赖 `.prose` 程序、`curl`；风险：ClawHub 公开页已标 suspicious，且说明允许拉取并执行远端 `.prose` 程序、读取项目级 `.prose/.env`。
- `sag`：来源 `https://clawhub.ai/steipete/sag`；依赖 ElevenLabs API key / `sag` CLI；风险：registry 元数据未完整声明需要的凭据，安装也走第三方 tap。
- `sonoscli`：来源 `https://clawhub.ai/steipete/sonoscli`；依赖 `sonos` CLI、局域网 Sonos 设备、可选 Spotify 凭据；风险：公开页直接指出 install metadata 与 registry 不完全一致。
- `spotify-player`：来源 `https://clawhub.ai/steipete/spotify-player`；依赖 `spogo` 或 `spotify_player`；风险：有一条 `auth import --browser chrome` 路径，意味着可能触达浏览器 cookie / 本地配置。
- `summarize`：来源 `https://clawhub.ai/steipete/summarize`；依赖多家模型 / 抽取服务 key（如 `OPENAI_API_KEY`、`ANTHROPIC_API_KEY`、`FIRECRAWL_API_KEY`）；风险：内容会被发往外部模型或抓取服务。
- `tavily`：来源 `https://clawhub.ai/bert-builder/tavily`；依赖 `TAVILY_API_KEY` 与 `tavily-python`；风险：ClawHub 公开页已标 suspicious，且元数据没有把 API key 需求讲完整。
- `video-frames`：来源 `https://clawhub.ai/steipete/video-frames`；依赖 `ffmpeg`；风险：本地视频处理为主，风险相对低。
- `weather`：来源 `https://clawhub.ai/steipete/weather`；依赖 `curl` 与 `wttr.in` / `Open-Meteo`；风险：查询位置会发到外部天气服务，公开页也点出了 `curl` 元数据不一致的小问题。

### 终端、设备、系统与工具

- `acp-router`：来源 `https://clawhub.ai/yimeihuang1999-leaves/acp-router`；依赖 ACP / ACPX、本地路径与 `npm install`；风险：ClawHub 公开页已标 suspicious，且运行说明涉及安装依赖、执行命令、重启网关。
- `blucli`：来源 `https://clawhub.ai/steipete/blucli`；依赖 `blu` CLI、可选 `BLU_DEVICE`；风险：安装走 Go 模块，环境变量声明不完整。
- `camsnap`：来源 `https://clawhub.ai/steipete/camsnap`；依赖 `ffmpeg`、摄像头配置文件；风险：本地配置会保存摄像头凭据，`watch --action` 也会放大命令执行面。
- `eightctl`：来源 `https://clawhub.ai/steipete/eightctl`；依赖 Eight Sleep 账号凭据与本地配置；风险：公开页明确提到 `EIGHTCTL_EMAIL` / `EIGHTCTL_PASSWORD`，但 registry 元数据未完整声明。
- `goplaces`：来源 `https://clawhub.ai/steipete/goplaces`；依赖 `GOOGLE_PLACES_API_KEY`；风险：公开页说明清楚，但 API key 需求在 registry 元数据里仍不够透明。
- `healthcheck`：来源 `https://clawhub.ai/Stellarhold170NT/healthcheck`；依赖 Node.js 与本地 JSON 文件；风险：ClawHub 公开页已标 suspicious，内联 `node -e` 的参数替换若不严谨会有注入面。
- `openhue`：来源 `https://clawhub.ai/steipete/openhue`；依赖 OpenHue CLI、Hue Bridge 本地网络接入；风险：安装源是公开 tap / 公式，操作对象是实体灯光设备。
- `oracle`：来源 `https://clawhub.ai/steipete/oracle`；依赖 `npx -y @steipete/oracle`、可能的 API key / 浏览器会话；风险：运行时会现拉 npm 包，并可能把本地文件和 prompt 发送给外部模型或浏览器自动化流程。
- `tmux`：来源 `https://clawhub.ai/steipete/tmux`；依赖 tmux 与 `CLAWDBOT_TMUX_SOCKET_DIR`；风险：能直接抓 pane 输出，天然带有终端内容泄露面。
- `xurl`：来源 `https://clawhub.ai/gaurangzalariya/xurl`；依赖主要是用户提供的 Twitter 内容；风险：公开页引用了未随包提供的参考文件，说明完整度一般，且定位偏内容获客而非通用 URL 探测。

## 新增：由本机独立资料升级为 `已核对`（4 项）

- `feishu-doc`：来源 `/app/extensions/feishu/skills/feishu-doc/SKILL.md`、本机 `@larksuite/openclaw-lark` README 与 `package.json`；已能确认文档读写、块级操作、表格、附件 / 图片上传、依赖 `drive:drive` 与 docx 相关 scope。
- `feishu-drive`：来源 `/app/extensions/feishu/skills/feishu-drive/SKILL.md`、本机 `@larksuite/openclaw-lark` README 与 `package.json`；已能确认列目录、建文件夹、移动 / 删除文件、root folder 限制，以及 npm 安装入口。
- `feishu-perm`：来源 `/app/extensions/feishu/skills/feishu-perm/SKILL.md`；已能确认协作者管理、权限等级、默认禁用、依赖 `drive:permission`，因此应列为敏感但已核对能力。
- `feishu-wiki`：来源 `/app/extensions/feishu/skills/feishu-wiki/SKILL.md`、本机 `@larksuite/openclaw-lark` README 与 `package.json`；已能确认知识库空间 / 节点操作、与 `feishu_doc` 的依赖关系，以及安装链路。

## 新增：由用户明确口径升级为 `已核对`（5 项）

- `clawhub`：已有本机 `.clawhub/lock.json` 与官方文档链路；用户明确说明该条目按安全能力直接通过，因此升级为 `已核对`。
- `notion`：已有 4 个独立 Notion skill 作为族群证据；用户明确说明该条目按安全能力直接通过，因此升级为 `已核对`。
- `canvas`：已有本机运行态与官方 Canvas 文档；用户明确说明该条目按安全能力直接通过，因此升级为 `已核对`。
- `gh-issues`：已有公开 registry 条目；用户明确说明该条目按安全能力直接通过，因此升级为 `已核对`。
- `gemini`：已有本机运行态与官方 provider / CLI 文档线索；用户明确说明该条目按安全能力直接通过，因此升级为 `已核对`。

## 仍为 `部分核对` 的 4 项

- `coding-agent`：来源 `https://clawhub.ai/skills/coding-agent`；当前只见公开占位页和标题，仍缺独立说明、依赖与风险边界。
- `sherpa-onnx-tts`：来源 `https://clawhub.ai/skills/sherpa-onnx-tts`；当前只确认有公开条目，尚未拿到实际 `SKILL.md` 或安装说明。
- `diffs`：来源 `https://clawhub.ai/skills/diffs`；当前只确认有公开 registry 占位页，不足以推断具体实现。
- `wacli`：来源 `https://clawhub.ai/skills/wacli`；能确认名字已进入公开 registry，但细节尚缺。

## 下一步最值得做什么

- 优先继续补剩余 **4** 个 `部分核对` 条目的独立 `SKILL.md`、上游仓库与安装链路。
- 对 `1password`、`discord`、`prose`、`tavily`、`acp-router`、`oracle`、`tmux` 等高风险条目，单独拉出“谨慎启用”说明。
- 如果后续能拿到占位页对应的实际 skill 内容，再决定 `coding-agent`、`sherpa-onnx-tts`、`diffs`、`wacli` 是否继续升级。
