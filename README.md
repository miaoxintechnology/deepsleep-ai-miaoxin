# DeepSleep

DeepSleep 是一款**单文件网页版 AI 助手**，由 **喵芯科技（Miaoxin Technology）** 在 DeepSeek 基础上开发，界面与交互参考 DeepSeek 官方网页版与 DeepSeek Harness（DSH）的通用设计模式。

DeepSleep is a **single-file web AI assistant** built by **Miaoxin Technology** on top of DeepSeek, with its interface and interactions modelled on the DeepSeek web app and the shared design patterns of DeepSeek Harness (DSH).

## ✨ 特性

- 🎨 **SVG 画图**：当请求画图/绘制时，AI 以「前后缀包裹的完整 SVG」输出，对话页自动渲染为图片；每条消息支持多张图片，每张图带「📥 下载」按钮（JPEG）；思维链中的 SVG 同样按标准格式渲染
- 🎛 **对话 / 轨迹 双视图**：轨迹台账以 DSH 风格事件行（用户 / 图片 / 思考 / 记忆 / 助手，标签跟随 11 语言）实时同步，支持搜索、折叠与轮次跳转；时序图含记忆泳道
- 🧠 **轨迹存储精简**：轨迹的记忆行只保存当轮实际传入的记忆内容，不再记录完整系统提示词与上下文副本，存储占用大幅降低
- 🧠 **记忆系统**：支持保存 / 修改 / 删除记忆（更新/修改/删除前缀规约），UI 隐藏原文、显示生成状态提示，「查看纯文本」可见原文
- 🔍 **OCR 三选一**：本地 Tesseract（不消耗 API）/ 云端 OCR.space（免费）/ 识图模型（计入 token 与费用消耗，模型名可在设置中修改）
- 👁 **识图模式**：按模型类型自动路由，图片按官方多模态规范（`image_url` + `detail="original"`）直传，不压缩、不丢细节
- 🌐 **11 语言**：zhCN / zhTW / en / ja / fr / de / ko / es / ru / ar / pt 完整界面与文档（关于 / 教程 / 更新日志 / 免责声明）
- ⚡ **智能滚动（DeepSeek 网页版风格）**：生成时贴底自动跟随（即时滚动）；上滑立即停止、可自由查看历史；滚回底部自动恢复跟随
- 💰 **费用统计**：输入 / 思考 / 输出分别计费（思考按输出价），峰谷时段计费，明细面板分模型展示
- 🤖 **智能体**：自定义 AI 助手（独立模型与系统提示词、独立记忆），对话记录与用量与普通对话完全隔离
- ♾ **无数量限制**：对话轮数、会话数量、上传文件数量均无上限，唯一上限是浏览器 localStorage 配额；写满时渐进裁剪最旧会话并保留已有数据，绝不整键删除
- 🗜 **头像精简**：仅「用户头像」可设置（浅色/深色各一张），保存时自动压缩为 512px JPEG 并只存压缩结果；助手与智能体固定使用内置 LOGO，随主题自动切换深浅，不占用存储
- 🔄 **实时渲染一致**：生成过程中看到的 Markdown 与公式排版与刷新页面后完全一致，无需刷新
- 📤 **轮次跳转**：输入 `#N` 快速定位对应轮次（对话 / 轨迹视图均支持），刚生成的内容同样可跳转

## ✨ Features

- 🎨 **SVG drawing**: when a drawing is requested, the AI emits a complete SVG wrapped in dedicated prefixes/suffixes and the chat renders it as an image; each message supports multiple images, each with a "📥 Download" button (JPEG). SVGs inside the reasoning chain are rendered the same way
- 🎛 **Dual view (Chat / Trace)**: the trace ledger syncs in real time as DSH-style event rows (user / image / thinking / memory / assistant, labels following all 11 languages) with search, collapse and turn jumping; the timeline includes a memory lane
- 🧠 **Lean trace storage**: memory rows store only the memory content actually sent in that turn — no full system prompt or context copies — greatly reducing storage usage
- 🧠 **Memory system**: save / update / delete memories (prefix-based conventions); the UI hides raw text behind a generation-status hint, while "View raw text" reveals it
- 🔍 **Three OCR options**: local Tesseract (no API cost) / cloud OCR.space (free) / vision model (counts toward tokens and cost; the model name is configurable)
- 👁 **Vision mode**: routed automatically by model type; images are sent per the official multimodal spec (`image_url` + `detail="original"`) without compression or detail loss
- 🌐 **11 languages**: zhCN / zhTW / en / ja / fr / de / ko / es / ru / ar / pt — full UI and docs (About / Tutorial / Changelog / Disclaimer)
- ⚡ **Smart scrolling (DeepSeek web style)**: sticks to the bottom and follows output live; scrolling up stops it immediately so you can read history; returning to the bottom resumes following
- 💰 **Cost tracking**: input / thinking / output billed separately (thinking at the output rate), peak and off-peak pricing, with a per-model breakdown panel
- 🤖 **Agents**: custom AI assistants (own model, system prompt and memories) whose conversations and usage are fully isolated from normal chats
- ♾ **No count limits**: rounds, conversations and uploaded files are all unlimited — the only limit is the browser's localStorage quota. When it fills up, the oldest conversations are trimmed progressively with existing data preserved, never by deleting a whole key
- 🗜 **Lean avatars**: only the **user avatar** is configurable (one light and one dark); it is automatically compressed to a 512px JPEG and only the compressed result is stored. Assistant and agent avatars always use the built-in LOGO, switching light/dark with the theme and consuming no storage
- 🔄 **Live rendering matches refresh**: the Markdown and formula typesetting you see while streaming is identical to what you get after refreshing — no reload needed
- 📤 **Turn jumping**: type `#N` to jump to a turn (works in both Chat and Trace views), including content that was just generated

## 📥 下载

- **V20.2.0 Windows 便携版（exe）**：[下载 DeepSleep-26H2-13.2A-portable.exe](https://github.com/miaoxintechnology/deepsleep-ai-miaoxin/releases/download/v20.2.0/DeepSleep-26H2-13.2A-portable.exe) — **最新版**，免安装、双击即用（72.7 MB）
- **V20.2.0 源文件**：`deepsleep_26H2-13.2A(V20.2.0).HTML`（本仓库内，也可通过 [Releases · v20.2.0](https://github.com/miaoxintechnology/deepsleep-ai-miaoxin/releases/tag/v20.2.0) 或 [raw 直链](https://github.com/miaoxintechnology/deepsleep-ai-miaoxin/raw/v20.2.0/deepsleep_26H2-13.2A(V20.2.0).HTML) 下载）
- **V20.1.0 Windows 便携版（exe）**：[下载 DeepSleep-26H2-13.1A-portable.exe](https://github.com/miaoxintechnology/deepsleep-ai-miaoxin/releases/tag/v20.1.0) — 免安装、双击即用
- **V20.1.0 源文件**：`deepsleep_26H2-13.1A(V20.1.0).HTML`（本仓库内）
- **V20.0.0 Windows 便携版（exe）**：[下载 DeepSleep-26H2-13.0A-portable.exe](https://github.com/miaoxintechnology/deepsleep-ai-miaoxin/releases/tag/v20.0.0) — 旧版
- **V20.0.0 源文件**：`deepsleep_26H2-13.0A(V20.0.0).HTML`（本仓库内）

## 📥 Download

- **V20.2.0 Windows portable (exe)**: [Download DeepSleep-26H2-13.2A-portable.exe](https://github.com/miaoxintechnology/deepsleep-ai-miaoxin/releases/download/v20.2.0/DeepSleep-26H2-13.2A-portable.exe) — **latest**, no installation, just double-click (72.7 MB)
- **V20.2.0 source**: `deepsleep_26H2-13.2A(V20.2.0).HTML` (in this repository, or via [Releases · v20.2.0](https://github.com/miaoxintechnology/deepsleep-ai-miaoxin/releases/tag/v20.2.0) / [raw link](https://github.com/miaoxintechnology/deepsleep-ai-miaoxin/raw/v20.2.0/deepsleep_26H2-13.2A(V20.2.0).HTML))
- **V20.1.0 Windows portable (exe)**: [Download DeepSleep-26H2-13.1A-portable.exe](https://github.com/miaoxintechnology/deepsleep-ai-miaoxin/releases/tag/v20.1.0) — no installation, just double-click
- **V20.1.0 source**: `deepsleep_26H2-13.1A(V20.1.0).HTML` (in this repository)
- **V20.0.0 Windows portable (exe)**: [Download DeepSleep-26H2-13.0A-portable.exe](https://github.com/miaoxintechnology/deepsleep-ai-miaoxin/releases/tag/v20.0.0) — older release
- **V20.0.0 source**: `deepsleep_26H2-13.0A(V20.0.0).HTML` (in this repository)

## 🚀 使用

1. 用浏览器打开 `deepsleep_26H2-13.2A(V20.2.0).HTML`
2. 在设置中填入 API Key（以及 Base URL，默认 `https://api.deepseek.com/chat/completions`）
3. 在设置里维护模型列表（可添加 / 删除任意数量，每个模型可设名称与类型：文本 / 识图）
4. 在输入框上方的**模型胶囊**中选择本次使用的模型；识图类型的模型会自动接收图片，文本类型的模型则走 OCR
5. 按需开启深度思考、调节推理强度，即可对话

> 纯前端单文件，无需构建；运行时从 CDN 加载 `marked@15.0.4`（Markdown）、`dompurify@3.2.4`（净化）、MathJax v3（LaTeX 排版）。

## 🚀 Usage

1. Open `deepsleep_26H2-13.2A(V20.2.0).HTML` in a browser
2. Enter your API key in Settings (and the Base URL, defaulting to `https://api.deepseek.com/chat/completions`)
3. Maintain the model list in Settings (add or remove any number of models; each has a name and a type: text / vision)
4. Pick the model for this conversation from the **model pill** above the input box; vision models receive images directly, while text models go through OCR
5. Enable deep thinking and adjust the reasoning effort as needed, then start chatting

> Pure front-end, single file, no build step. At runtime it loads `marked@15.0.4` (Markdown), `dompurify@3.2.4` (sanitising) and MathJax v3 (LaTeX typesetting) from a CDN.

## 📄 文档

- 版本：**26H2-13.2A (V20.2.0)** — 正式版
- 关于 / 教程 / 更新日志 / 免责声明详见应用内底部链接（11 语言）
- 内置 **DeepSeek API 费用统计** 移植自 [dsh-deepseek-cost](https://github.com/)（MIT License，版权归喵芯科技）

## 📄 Documentation

- Version: **26H2-13.2A (V20.2.0)** — stable release
- About / Tutorial / Changelog / Disclaimer are available from the in-app footer links (11 languages)
- The built-in **DeepSeek API cost tracker** is ported from [dsh-deepseek-cost](https://github.com/) (MIT License, copyright Miaoxin Technology)

## 📜 许可

本项目基于 **MIT License (MIT 许可证)** 开源（详细条款见 [LICENSE](LICENSE)）。
版权：Copyright (c) 2026 喵芯科技（Miaoxin Technology）。完整免责声明与许可说明见应用内。

## 📜 License

This project is open source under the **MIT License** (see [LICENSE](LICENSE) for the full text).
Copyright (c) 2026 Miaoxin Technology. The complete disclaimer and licence notes are available in-app.

---

**免责声明**：本软件按 MIT 许可证授权使用，使用者自行承担使用风险；请勿用于违法用途。版权与品牌归喵芯科技所有。

**Disclaimer**: This software is provided under the MIT License and used at your own risk; do not use it for unlawful purposes. Copyright and branding belong to Miaoxin Technology.
