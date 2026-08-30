# DeepSleep

DeepSleep 是一款**单文件网页版 AI 助手**，由 **喵芯科技（Miaoxin Technology）** 在 DeepSeek 基础上开发，界面与交互参考 DeepSeek 官方网页版与 DeepSeek Harness（DSH）的通用设计模式。

## ✨ 特性

- 🎨 **SVG 画图**：当请求画图/绘制时，AI 以「前后缀包裹的完整 SVG」输出，对话页自动渲染为图片；每条消息支持多张图片，每张图带「📥 下载」按钮（JPEG）；思维链中的 SVG 同样按标准格式渲染
- 🎛 **对话 / 轨迹 双视图**：轨迹台账以 DSH 风格事件行（USER / IMAGE / ASSISTANT / THINK / SYSTEM / CONTEXT）实时同步，支持搜索、折叠与轮次跳转
- 🧠 **每轮真实 SYSTEM / CONTEXT**：轨迹记录每轮实际注入的系统提示词与传入模型的完整上下文（HTTP 请求 messages），随消息持久化到本地存储，重新打开仍可见
- 🧠 **记忆系统**：支持保存 / 修改 / 删除记忆（更新/修改/删除前缀规约），UI 隐藏原文、显示生成状态提示，「查看纯文本」可见原文
- 🔍 **OCR 三选一**：本地 Tesseract（不消耗 API）/ 云端 OCR.space（免费）/ 识图模型 `deepseek-v4-flash-vision-exp`（计入 token 与费用消耗）
- 👁 **识图模式**：官方图像理解模型 `deepseek-v4-flash-vision-exp`，图片按官方多模态规范（`image_url` + `detail="original"`）直传，不压缩、不丢细节
- 🌐 **11 语言**：zhCN / zhTW / en / ja / fr / de / ko / es / ru / ar / pt 完整界面与文档（关于 / 教程 / 更新日志 / 免责声明）
- ⚡ **智能滚动（DeepSeek 网页版风格）**：生成时贴底自动跟随（即时滚动）；上滑立即停止、可自由查看历史；滚回底部自动恢复跟随
- 💰 **费用统计**：输入 / 思考 / 输出分别计费（思考按输出价），峰谷时段计费，明细面板分模型展示
- 🤖 **智能体**：自定义 AI 助手（独立模型与系统提示词）、头像自定义（用户 / DeepSleep / 智能体，浅深各一套）
- 📤 **轮次跳转**：输入 `#N` 快速定位对应轮次（对话 / 轨迹视图均支持）

## 🚀 使用

1. 用浏览器打开 `deepsleep_26H2-13.0A(V20.0.0).HTML`
2. 在设置中填入 DeepSeek API Key
3. 即可对话；选择模式（快速 / 专家 / 识图）、开启深度思考等

> 纯前端单文件，无需构建；运行时从 CDN 加载 `marked@15.0.4` 渲染 Markdown。

## 📄 文档

- 版本：**26H2-13.0A (V20.0.0)** — 正式版
- 关于 / 教程 / 更新日志 / 免责声明详见应用内底部链接（11 语言），或在线 API 文档 `DeepSleep_Docs_V20.0.0.html`
- 内置 **DeepSeek API 费用统计** 移植自 [dsh-deepseek-cost](https://github.com/)（MIT License，版权归喵芯科技）

## 📜 许可

本项目基于 **MIT License (MIT 许可证)** 开源（详细条款见 [LICENSE](LICENSE)）。
版权：Copyright (c) 2026 喵芯科技（Miaoxin Technology）。完整免责声明与许可说明见应用内。

---
**免责声明**：本软件按 MIT 许可证授权使用，使用者自行承担使用风险；请勿用于违法用途。版权与品牌归喵芯科技所有。
