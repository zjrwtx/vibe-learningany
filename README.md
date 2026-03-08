# （新的完全重构版本将会开源）
<img width="2382" height="1962" alt="Clipboard_Screenshot_1767272956" src="https://github.com/user-attachments/assets/04393c0b-7240-454d-8ded-ff7601c33b2e" />


---

## 🆕 更新日志

### 2026-01-01: 新增 PPT 生成与数学视频生成

新增两项创作工具：

- 🧩 **PPT 生成** - 输入主题或大纲，AI 自动生成课件结构与页面内容
- 🎥 **数学视频生成** - 基于 **Manim (Mathematical Animation Engine)** 生成 3Blue1Brown 风格数学动画

数学视频生成支持：

- 🎥 **自然语言生成** - 用中文描述想要的动画，AI 自动生成 Manim 代码
- 📝 **代码实时预览** - 流式显示生成的 Python 代码
- ⚡ **视频渲染** - 后端自动渲染生成 MP4 视频
- 📥 **下载分享** - 支持视频下载和在线播放

**使用方法：**

1. 安装 Manim：
   ```bash
   # 安装 Manim
   pip install manim
   
   # macOS 安装 LaTeX (可选，用于数学公式)
   brew install --cask mactex
   ```

2. 访问首页，点击「数学动画生成器」

3. 输入描述，如「解释勾股定理」

---

### 2026-01-01: 新增 FlashNote 闪卡笔记功能

集成 **FlashNote 闪卡笔记** 系统，支持：

- 📝 **Markdown 笔记管理** - 导入/导出/创建/编辑 Markdown 文件
- 🎴 **闪卡学习模式** - 将 Markdown 转换为学习卡片，支持键盘导航
- 🔍 **全文搜索** - 实时搜索所有笔记内容
- 🔖 **书签收藏** - 保存/整理网页链接，支持标签分类，通过 Jina AI 提取内容
- 🎨 **主题系统** - 多种颜色主题，支持持久化
- ☁️ **WebDAV 云同步** - 同步笔记到 WebDAV 服务器
- 📐 **数学公式支持** - KaTeX 渲染数学公式

**使用方法：** 访问首页，点击「FlashNote 闪卡笔记」工具卡片

---

### 2025-12-22: 新增视频转PDF功能

新增 **视频转PDF笔记** 功能，支持：

- 🎬 **视频上传** - 支持 mp4, webm, mov, avi, mkv 格式
- 🎤 **Whisper 语音识别** - 自动提取视频中的语音内容
- 🖼️ **关键帧提取** - 基于场景变化智能提取关键画面
- 👁️ **AI 视觉分析** - 使用 Kimi Vision API 分析画面内容
- 📄 **PDF 生成** - 自动生成结构化笔记文档

**使用方法：**

1. 安装系统依赖：
   ```bash
   # macOS
   brew install ffmpeg
   
   # Ubuntu
   apt install ffmpeg
   ```

2. 安装 Python 依赖：
   ```bash
   cd backend && uv sync
   ```

3. 访问 `/video-to-pdf` 页面上传视频

---

### 🎯 为什么是教育？

我们认为，**教育一定是 AI Agent 最大的落地场景之一**。  
而选择 **开源**，是希望能够：

- 🌱 帮助更多 **学校**
- 👩‍🎓 赋能更多 **同学**
- 👨‍🏫 支持更多 **教育工作者**

让 **AI 教育能力** 不只停留在少数平台，而是被更多人真正用起来。

---

### 🚧 项目现状

- 当前版本仍然 **较为粗糙**
- 功能与体验都在 **持续打磨中**
- 后续会 **不断完善与迭代**

---

### 🤝 共建与参与

欢迎你：

- 使用它  
- 提出建议  
- 贡献代码  

让我们一起打造更好的教育 AI 👏

---

> **一起 enjoy education agent time 🚀**


## 功能特点

- **对话式学习** - 输入想学习的知识点，AI 以引导式教学方式回应
- **概念地图导航** - 可视化知识结构，点击节点探索相关概念
- **实时可视化生成** - AI 自动生成交互式 HTML 可视化内容
- **云端部署** - 通过 EdgeOne Pages MCP 自动部署到云端
- **进度追踪** - 实时显示 AI 处理阶段（思考 → 编写 → 调用工具 → 部署）
- **视频转PDF** - 上传教学视频，AI 自动提取关键帧、识别语音，生成结构化笔记
- **FlashNote 闪卡笔记** - Markdown 笔记管理、闪卡学习、全文搜索、书签收藏、WebDAV 云同步
- **PPT 生成** - 输入主题或大纲，自动生成课件
- **数学视频生成** - 用自然语言生成 3Blue1Brown 风格数学动画视频 (Manim)


## 例子
<img width="1280" height="662" alt="317846db0c0788b24c10613b7d0775c0_720" src="https://github.com/user-attachments/assets/266c96a9-d2e6-4c35-9ff8-85899686e1ac" />
<img width="1280" height="929" alt="5cce227b43f6e958c8162b2c917ffc16_720" src="https://github.com/user-attachments/assets/baabeff4-374b-4d67-bc97-b76543462b66" />

![a747c77f0da7204666b4857ea771958e_720](https://github.com/user-attachments/assets/b213f4a6-62a9-43ac-adaa-721e37a09ea4)


## 快速开始

### 环境要求

- Node.js >= 18
- Python >= 3.13
- pnpm
- FFmpeg (用于视频转PDF功能)

### 安装

```bash
# 克隆仓库
git clone --recursive https://github.com/your-username/edu-ai-platform.git
cd edu-ai-platform

# 前端依赖
cd frontend && pnpm install

# 后端依赖
cd ../backend && uv sync
```

### 配置

复制环境变量模板并填入 API Key：

```bash
cp backend/.env.example backend/.env
```

编辑 `backend/.env`：

```bash
# 使用 Kimi（默认）
KIMI_API_KEY=sk-your-api-key
KIMI_MODEL_NAME=kimi-k2-turbo-preview

# 或使用 DeepSeek / OpenAI 兼容 API
LLM_PROVIDER_TYPE=openai_legacy
OPENAI_API_KEY=sk-your-api-key
OPENAI_BASE_URL=https://api.deepseek.com
OPENAI_MODEL_NAME=deepseek-chat
OPENAI_REASONING_KEY=reasoning_content
```

### 启动

```bash
# 终端 1 - 后端
cd backend && python main.py

# 终端 2 - 前端
cd frontend && pnpm dev
```

访问 http://localhost:3000

## 项目结构

```
edu-ai-platform/
├── frontend/           # Next.js 前端
│   └── src/
│       ├── app/        # 页面 (含 /flashnote 路由)
│       ├── components/ # 组件 (含 flashnote/ 模块)
│       ├── hooks/      # WebSocket、FlashNote 状态管理
│       ├── types/      # TypeScript 类型定义
│       └── utils/      # 工具函数 (markdown, themes, webdav)
├── backend/            # FastAPI 后端
│   ├── main.py         # 主应用
│   ├── kimi_runner.py  # Kimi CLI 封装
│   ├── mcp.json        # MCP 配置
│   ├── agent/          # Agent 配置和提示词
│   └── video_processor/ # 视频转PDF处理模块
├── kimi-cli/           # AI Agent 核心 (submodule)
└── kosong/             # LLM 抽象层 (submodule)
```

## 技术栈

| 层 | 技术 |
|---|------|
| 前端 | Next.js 16, React 19, TypeScript, Tailwind CSS 4 |
| 后端 | FastAPI, Python 3.13, WebSocket |
| AI | Kimi CLI, MCP (Model Context Protocol) |
| 笔记 | KaTeX, WebDAV, Markdown (remark/rehype) |
| 部署 | EdgeOne Pages |

## API

| 方法 | 路径 | 说明 |
|------|------|------|
| GET | `/` | 服务状态 |
| GET | `/health` | 健康检查 |
| GET | `/api/history` | 获取历史 |
| DELETE | `/api/history/{task_id}` | 删除历史 |
| WebSocket | `/ws/chat` | 实时聊天 |
| POST | `/api/video/upload` | 上传视频 |
| GET | `/api/video/status/{task_id}` | 视频处理状态 |
| GET | `/api/video/download/{task_id}` | 下载PDF |
| WebSocket | `/ws/video-to-pdf/{task_id}` | 视频处理进度 |


## 致谢

本项目基于以下优秀项目构建：

- **[Kimi CLI](https://github.com/MoonshotAI/kimi-cli)** - Moonshot AI 开源的 coding Agent 框架，提供工具调用、MCP 集成等核心能力
- **[Kosong](https://github.com/MoonshotAI/kosong)** - Moonshot AI 开源的 LLM 抽象层，统一消息结构与多 Provider 支持，让 Agent 开发更简洁灵活
- **[EdgeOne Pages MCP](https://github.com/TencentEdgeOne/edgeone-pages-mcp)** - EdgeOne Pages 的 MCP 服务，提供一键云端部署能力

感谢 Moonshot AI 团队和 EdgeOne Pages！

## 联系方式

如有问题或建议，请联系：3038880699@qq.com

## License

apache-2.0
https://www.apache.org/licenses/LICENSE-2.0
