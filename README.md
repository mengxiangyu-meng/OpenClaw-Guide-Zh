# 🦞 OpenClaw 中文全栈教程

> 你的私人 AI 助手网关，接入微信/Telegram/Discord/飞书随时随地聊天

[![OpenClaw](https://img.shields.io/badge/OpenClaw-v2026.2-blue?style=flat-square)](https://github.com/openclaw/openclaw)
[![Stars](https://img.shields.io/github/stars/openclaw/openclaw?style=flat-square)](https://github.com/openclaw/openclaw)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

---

## 📖 这是什么？

**OpenClaw** 是一个开源的 AI 助手网关框架，简单来说：

> 它让你的 AI 助手可以在各种聊天软件里跟你聊天

想象一下：
- 在 **微信** 里跟 AI 助手对话
- 在 **Telegram** 召唤 AI 帮你查资料
- 在 **Discord** 群聊里用 AI 编程
- 在 **飞书** 里让 AI 帮你处理工作

**一个网关，全部搞定。**

---

## ✨ 为什么选 OpenClaw？

| 特性 | 说明 |
|------|------|
| 🏠 自托管 | 运行在你的机器上，数据完全可控 |
| 🌐 多平台 | 微信/Telegram/Discord/飞书/iMessage 同时在线 |
| 🤖 Agent 原生 | 专为 AI 助手设计，会话/记忆/工具/多代理 |
| 📱 移动端 | 支持 iOS/Android 节点，拍照/语音都能用 |
| 🆓 开源免费 | MIT 协议，社区活跃 |
| 🎨 Web 控制台 | 浏览器直接管理所有会话 |

---

## 📚 教程目录

| 序号 | 章节标题 | 难度 | 描述 |
|:---:|---------|:---:|------|
| 01 | [项目介绍](/docs/openclaw/01-项目介绍.md) | 🟢 | OpenClaw 是什么？发展历史/核心架构 |
| 02 | [安装部署](/docs/openclaw/02-安装部署.md) | 🟢 | macOS / Linux / Windows 全平台安装 |
| 03 | [快速开始](/docs/openclaw/03-快速开始.md) | 🟢 | 5 分钟跑起第一个对话 |
| 04 | [模型配置](/docs/openclaw/04-模型配置.md) | 🟡 | 接入 Claude / GPT / Ollama 等 29 个模型 |
| 05 | [消息平台](/docs/openclaw/05-消息平台接入.md) | 🟡 | 微信 / Telegram / Discord / 飞书连接 |
| 06 | [技能系统](/docs/openclaw/06-技能系统.md) | 🟡 | 50+ 内置技能 + 自定义技能开发 |
| 07 | [记忆系统](/docs/openclaw/07-记忆系统.md) | 🟡 | AI 如何记住你的偏好和上下文 |
| 08 | [多代理协作](/docs/openclaw/08-多代理协作.md) | 🔴 | 一个网关跑多个独立 AI 助手 |
| 09 | [Docker 部署](/docs/openclaw/09-Docker部署.md) | 🔴 | 容器化部署 / VPS 远程访问 |
| 10 | [安全配置](/docs/openclaw/10-安全配置.md) | 🔴 | Token 保护 / 权限管理 / 安全加固 |

> 🕐 预计学习时间：**新手 2 小时 → 熟练 1 天 → 部署生产 1 周**

---

## 🚀 快速开始

```bash
# 1. 安装 OpenClaw
npm install -g openclaw@latest

# 2. 初始化配置
openclaw onboard --install-daemon

# 3. 登录消息平台（以 Telegram 为例）
openclaw channels login

# 4. 启动网关
openclaw gateway --port 18789
```

然后打开浏览器访问 `http://127.0.0.1:18789/` 就能看到控制台啦！

---

## 📌 学习路线

### ⚡ 新手速通（30分钟）
```
01 项目介绍 → 02 安装部署 → 03 快速开始
```
完成 ✅ 能跑起来、能和 AI 对话

### 💪 日常使用（2-3小时）
```
03 → 04 模型配置 → 05 消息平台 → 06 技能系统
```
完成 ✅ 接好聊天软件、配置好用的模型

### 🎯 深度定制（1-2天）
```
06 → 07 记忆系统 → 08 多代理协作
```
完成 ✅ 打造专属你的 AI 助手

### 🏢 生产部署（1周）
```
09 Docker 部署 → 10 安全配置
```
完成 ✅ 部署到服务器、保证安全

---

## 🎯 适合谁？

- ✅ 想在微信/Telegram里用 AI 助手的人
- ✅ 技术人员想搭建自己的 AI 助手服务
- ✅ 团队想要统一 AI 协作平台
- ✅ 开发者想探索 AI Agent 边界

---

## 🔧 环境要求

| 项目 | 要求 |
|------|------|
| Node.js | 22.12.0+ 或 22 LTS (22.16+) |
| 系统 | macOS / Linux / Windows (WSL2) |
| API Key | OpenAI / Anthropic / Google 等 |
| 存储 | 约 500MB 空间 |

---

## 🎁 能做什么？

| 场景 | 示例 |
|------|------|
| 📱 即时聊天 | 微信/Telegram 问 AI 问题 |
| 💻 编程助手 | 丢个代码让 AI 帮你 debug |
| 📅 日程管理 | 让 AI 帮你查日历、设提醒 |
| 🔍 信息检索 | 让 AI 帮你搜资料、总结文章 |
| 🖼️ 图像分析 | 发图片让 AI 看看是啥 |
| 🎤 语音交互 | 手机语音跟 AI 对话 |

---

## 📦 配套资源

- 📋 [快速导航卡](/docs/快速导航卡.md) - 命令速查
- ❓ [FAQ 汇总](/docs/FAQ.md) - 常见问题
- 💻 [示例配置](/examples) - 开箱即用的配置

---

## 🤝 贡献指南

欢迎提交 Issue 和 PR！

- 🐛 发现 bug → 提 [Issue](https://github.com/mengxiangyu-meng/OpenClaw-Guide-Zh/issues)
- 💡 有建议 → 提 [PR](https://github.com/mengxiangyu-meng/OpenClaw-Guide-Zh/pulls)
- 💬 讨论交流 → [Discussions](https://github.com/mengxiangyu-meng/OpenClaw-Guide-Zh/discussions)

---

## 📄 License

MIT License

---

⭐ **有帮助的话，欢迎 Star！**

📢 **觉得有用就分享给朋友吧~**
