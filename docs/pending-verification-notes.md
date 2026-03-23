# 待核对条目：本地二次核对记录

> 这份文档只记录**本机已经找到的证据**，不把“有痕迹”偷换成“已完整验证可安装”。

## 状态口径

- `部分核对`：已经找到本地同名痕迹、同族上游或运行态证据，能补来源 / 依赖 / 风险说明，但还没核到独立 `SKILL.md` 或完整安装链路。
- `待核对`：目前仍主要来自旧路线图名字，尚未补到足够的一手资料。

## 本轮命中的 8 个条目

### `clawhub`

- 本地证据：`/home/node/.openclaw/workspace/.clawhub/lock.json`
- 当前判断：本机确实存在安装锁与已装 skill 记录，所以 `clawhub` 不是纯空名词；但目前只核到安装锁，不足以证明公开 registry、发布流程或独立 skill 规范已经稳定。
- 安装 / 依赖：当前仓库 README 里保留 `clawhub install <skill-slug>` 作为安装流入口；更细的安装说明还需要继续补。
- 风险备注：涉及安装、发布和供应链时，必须把来源与权限边界写清楚。

### `feishu-doc`

- 本地证据：`/home/node/.npm/_npx/be1a8fd12ade5f98/node_modules/@larksuite/openclaw-lark/package.json` 与 `src/tools/oapi/search/doc-search.js`、`src/tools/oapi/drive/doc-comments.js`、`src/tools/oapi/drive/doc-media.js`
- 当前判断：本地包已经覆盖 doc 搜索、评论和媒体相关实现，因此 `feishu-doc` 更像飞书文档总入口，而不是和 `feishu-create-doc` / `fetch` / `update` 完全并列的新独立能力。
- 安装 / 依赖：来源是本机缓存的 `@larksuite/openclaw-lark`，安装入口写在包内 `openclaw.install.npmSpec`；实际使用仍依赖飞书 OAuth 和相应 scope。
- 风险备注：涉及文档读取、评论和媒体处理，应该持续强调“读写范围”和“是否对他人可见”。

### `feishu-drive`

- 本地证据：`/home/node/.npm/_npx/be1a8fd12ade5f98/node_modules/@larksuite/openclaw-lark/src/tools/oapi/drive`
- 当前判断：本地已经能确认 drive 相关实现存在，因此不是纯猜测条目；但仓库里暂时还没核到同名 `SKILL.md`，所以先维持 `部分核对`。
- 安装 / 依赖：依赖 `@larksuite/openclaw-lark` 包和飞书 OAuth；包依赖里可见 `@larksuiteoapi/node-sdk`。
- 风险备注：涉及云盘文件时，最重要的是权限范围、文件可见性与批量操作的透明度。

### `feishu-perm`

- 本地证据：`/home/node/.npm/_npx/be1a8fd12ade5f98/node_modules/@larksuite/openclaw-lark/src/tools/oauth.js`、`oauth-batch-auth.js`、`src/tools/oapi/helpers.js`
- 当前判断：本地包已经有授权、批量授权和权限错误处理代码，所以“权限管理”并不是凭空想象；但它更像插件级能力，不该被轻描淡写地包装成低风险 skill。
- 安装 / 依赖：依赖飞书 OAuth、应用 scope 开通和账号匹配校验。
- 风险备注：这是这轮最该保守处理的条目之一；涉及权限提升、scope 开通和跨账号误授权风险。

### `feishu-wiki`

- 本地证据：`/home/node/.npm/_npx/be1a8fd12ade5f98/node_modules/@larksuite/openclaw-lark/src/tools/oapi/wiki`
- 当前判断：本地可以确认 wiki / space / node 相关实现存在，因此条目有真实来源支撑；但仍需继续核对对外暴露方式和最终操作边界。
- 安装 / 依赖：与其他飞书能力一样，依赖 `@larksuite/openclaw-lark` 安装链路和 OAuth。
- 风险备注：知识库结构操作容易影响多人协作空间，公开推荐时必须把“导航”和“修改结构”区分开。

### `notion`

- 本地证据：`/home/node/.codex/vendor_imports/skills` 里的 `notion-knowledge-capture`、`notion-meeting-intelligence`、`notion-research-documentation`、`notion-spec-to-implementation`
- 当前判断：本机能直接回到 4 个 Notion 家族 skill 的 `SKILL.md`，所以“Notion 生态入口”这个判断是可靠的；但通用名 `notion` 本身更像集合标签，不宜冒充成一个已经完全核对的独立 skill。
- 安装 / 依赖：这些本地 `SKILL.md` 都要求先接上 `Notion MCP`，典型步骤是 `codex mcp add notion --url https://mcp.notion.com/mcp`、启用 `rmcp_client`、再执行 `codex mcp login notion` 并重启 Codex。
- 风险备注：一旦允许写入页面 / 数据库，就要明确工作区访问范围、页面更新策略和意外覆盖风险。

### `canvas`

- 本地证据：`/home/node/.openclaw/canvas/index.html`
- 当前判断：本机确实存在 `OpenClaw Canvas` 交互页，但当前证据指向的是运行时 surface，而不是一个已经打包好的独立 skill。
- 安装 / 依赖：从页面内容看，它依赖 OpenClaw 的 action bridge 和移动端 / 节点侧 canvas 能力。
- 风险备注：UI surface 本身不高危，但如果把它当成通用 skill 推广，必须补清楚宿主环境前提。

### `gemini`

- 本地证据：`/home/node/.openclaw/agents/gemini/sessions/sessions.json`
- 当前判断：本机存在同名 agent 运行痕迹，说明 `gemini` 至少在本地运行态中是真实入口；但目前还没有核到独立 skill 包或安装说明。
- 安装 / 依赖：更像 provider / agent 层接入，预期会依赖外部模型服务配置。
- 风险备注：涉及第三方模型时，应把外部调用、数据出境和成本边界讲清楚。

## 暂时不升级为 `已核对` 的原因

- 这 8 个条目里，有些只有运行态痕迹，没有独立 `SKILL.md`
- 有些能确认“家族存在”，但通用名本身更像集合入口，不宜硬当成一个独立 skill
- 有些直接碰到权限、授权或外部服务，贸然升级会拉低仓库可信度

## 下一步最值得做什么

- 优先继续补剩余 43 个 `待核对` 条目的一手来源
- 从这 8 个 `部分核对` 条目里挑最容易闭环的几项，继续补安装方式与触发说明
- 对涉及授权、写入、发布的条目，先写清楚风险，再决定要不要升级为 `已核对`
