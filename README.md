# <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/robot.svg" width="28" style="vertical-align:text-bottom;"> 林缪斯 (Linmius)

<p align="center">
  <img src="https://raw.githubusercontent.com/ring-operation/gemma-270m/main/CherryBlossom.svg" width="120" alt="林缪斯 Logo">
</p>

<p align="center">
  <b>在浏览器中本地运行 AI 模型的 TurboWarp/Scratch 扩展</b>
</p>

<p align="center">
  <a href="#-%E5%8A%9F%E8%83%BD%E7%89%B9%E7%82%B9"><img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/star.svg" width="14" style="vertical-align:middle;"> 功能特点</a> •
  <a href="#-%E5%BF%AB%E9%80%9F%E5%BC%80%E5%A7%8B"><img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/rocket.svg" width="14" style="vertical-align:middle;"> 快速开始</a> •
  <a href="#-%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B"><img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/book.svg" width="14" style="vertical-align:middle;"> 使用教程</a> •
  <a href="#-%E6%8A%80%E6%9C%AF%E6%9E%B6%E6%9E%84"><img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/sitemap.svg" width="14" style="vertical-align:middle;"> 技术架构</a>
</p>

---

## <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/wand-magic-sparkles.svg" width="20" style="vertical-align:middle;"> 功能特点

- **<img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/robot.svg" width="16" style="vertical-align:middle;"> 本地 AI 推理** - 基于 [wllama](https://github.com/ngxson/wllama) 在浏览器中直接运行 GGUF 格式模型，数据完全本地处理，无需联网
- **<img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/book.svg" width="16" style="vertical-align:middle;"> 知识库系统** - 支持自定义知识库，实现 RAG (检索增强生成) 功能
- **<img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/comments.svg" width="16" style="vertical-align:middle;"> AI 训练师** - 内置交互式训练界面，可实时教 AI 新知识
- **<img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/bolt.svg" width="16" style="vertical-align:middle;"> 后台线程支持** - Worker 模式运行模型，不阻塞 UI
- **<img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/database.svg" width="16" style="vertical-align:middle;"> 离线存储** - 模型和知识库数据持久化存储在浏览器 IndexedDB 中
- **<img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/gamepad.svg" width="16" style="vertical-align:middle;"> 积木块编程** - 完整的 Scratch 积木块支持，拖拽即可实现 AI 功能

## <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/rocket.svg" width="20" style="vertical-align:middle;"> 快速开始

### 安装方法

#### <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/globe.svg" width="14" style="vertical-align:middle;"> 方法一：直接加载（推荐）

1. 打开 [TurboWarp](https://turbowarp.org/) 或 [Scratch](https://scratch.mit.edu/)
2. 点击左下角「添加扩展」按钮
3. 选择「加载自定义扩展」
4. 下载 [林缪斯.js](https://github.com/ring-operation/LinMuSi-TurboWarp-Expand/releases/latest/download/林缪斯.js) 文件
5. 点击载入您下载的扩展文件
   ```
   林缪斯.js
   ```

#### <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/folder-open.svg" width="14" style="vertical-align:middle;"> 方法二：本地加载

1. 下载 `林缪斯.js` 文件（混淆保护版本）
2. 在 TurboWarp 中选择「从本地文件加载」
3. 选择下载的 JS 文件

### <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/play.svg" width="14" style="vertical-align:middle;"> 首次使用

1. **加载模型**：点击扩展的「打开模型管理器」按钮
2. **选择模型**：可以从 URL 加载或选择本地 GGUF 文件
3. **开始对话**：模型加载完成后即可使用 AI 功能

## <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/book.svg" width="20" style="vertical-align:middle;"> 使用教程

### <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/cube.svg" width="14" style="vertical-align:middle;"> 基础积木块

| 积木块 | 功能说明 |
|--------|----------|
| `问 AI: [问题]` | 向 AI 发送问题并获取回复 |
| `问 AI (带知识库): [问题]` | 使用知识库上下文回答 |
| `AI 的回复` | 获取最近一次 AI 的回复内容 |
| `当 AI 回复完成时` | 事件触发积木 |

### <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/book-open.svg" width="14" style="vertical-align:middle;"> 知识库操作

| 积木块 | 功能说明 |
|--------|----------|
| `添加知识: [内容]` | 向当前知识库添加内容 |
| `清空知识库` | 清空所有知识库数据 |
| `当前启用的知识库` | 返回当前知识库名称 |

### <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/font.svg" width="14" style="vertical-align:middle;"> 字符串处理

| 积木块 | 功能说明 |
|--------|----------|
| `将字符串按每 [N] 个字符分割` | 分割字符串为数组 |
| `将数组拼接为字符串` | 将字符串数组合并 |

### <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/user-graduate.svg" width="14" style="vertical-align:middle;"> AI 训练师界面

1. 点击扩展工具栏的「AI训练师」按钮
2. 创建或选择知识库
3. 输入 `学习: 你想教给 AI 的内容` 来训练
4. 或直接提问让 AI 基于知识库回答

## <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/sitemap.svg" width="20" style="vertical-align:middle;"> 技术架构

```
┌─────────────────────────────────────────┐
│           TurboWarp / Scratch           │
│              (前端界面)                  │
├─────────────────────────────────────────┤
│         林缪斯扩展 (Linmius)            │
│  ┌─────────────┐    ┌──────────────┐   │
│  │  积木块接口  │    │  UI 管理器    │   │
│  └─────────────┘    └──────────────┘   │
├─────────────────────────────────────────┤
│         Web Worker (可选)               │
│         AI 推理后台线程                  │
├─────────────────────────────────────────┤
│              wllama                     │
│      (WebAssembly GGUF 推理引擎)         │
├─────────────────────────────────────────┤
│         IndexedDB (本地存储)            │
│    模型缓存 | 知识库数据 | 配置信息       │
└─────────────────────────────────────────┘
```

## <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/puzzle-piece.svg" width="20" style="vertical-align:middle;"> 支持的模型

本扩展支持 GGUF 格式的模型，推荐以下轻量级模型：

| 模型 | 大小 | 特点 |
|------|------|------|
| Gemma 2B/4B | ~1.5-3GB | Google 开源，中文支持较好 |
| Llama 3.2 1B/3B | ~0.6-2GB | Meta 最新，效率高 |
| Qwen 2.5 0.5B/1.5B | ~0.3-1GB | 阿里云，中文优化 |
| Phi-3/4 Mini | ~2-4GB | Microsoft，推理能力强 |

> <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/lightbulb.svg" width="14" style="vertical-align:middle;"> 提示：模型越大效果越好，但需要更多内存和加载时间

## <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/code.svg" width="20" style="vertical-align:middle;"> 开发相关

### <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/shield-halved.svg" width="14" style="vertical-align:middle;"> 构建混淆版本

如需从源码重新构建混淆版本：

```bash
node build-protected.js 不成熟的强行嵌入模型版本.js
```

然后将生成的 `不成熟的强行嵌入模型版本-protected.js` 重命名为 `林缪斯.js` 即可。

### <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/folder-tree.svg" width="14" style="vertical-align:middle;"> 项目结构

```
.
├── 林缪斯.js                    # 混淆保护版本（推荐使用）
├── 不成熟的强行嵌入模型版本.js   # 源码版本（旧版，用于开发）
└── README.md                    # 本文件
```

## <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/users.svg" width="20" style="vertical-align:middle;"> 社区交流

- **<img src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/tencentqq.svg" width="14" style="vertical-align:middle;"> QQ 群**: [1103478438](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=...) 
- **<img src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/bilibili.svg" width="14" style="vertical-align:middle;"> Bilibili**: [林缪斯官方账号](https://space.bilibili.com/)
- **<img src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/github.svg" width="14" style="vertical-align:middle;"> GitHub**: [项目仓库](https://github.com/ring-operation/LinMuSi-TurboWarp-Expand)
- **<img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/code.svg" width="14" style="vertical-align:middle;"> 小码王**: [社区主页](https://world.xiaomawang.com/)

## <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/clock-rotate-left.svg" width="20" style="vertical-align:middle;"> 更新日志

### v1.0.0 (2024-XX-XX)
- <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/star.svg" width="12" style="vertical-align:middle;"> 首次发布
- <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/robot.svg" width="12" style="vertical-align:middle;"> 支持本地 GGUF 模型运行
- <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/book.svg" width="12" style="vertical-align:middle;"> 知识库与 RAG 功能
- <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/comments.svg" width="12" style="vertical-align:middle;"> AI 训练师交互界面
- <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/bolt.svg" width="12" style="vertical-align:middle;"> Worker 后台线程支持

## <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/scale-balanced.svg" width="20" style="vertical-align:middle;"> 许可证

本项目采用 [MIT License](LICENSE) 开源协议。

## <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/heart.svg" width="20" style="vertical-align:middle;"> 致谢

- [wllama](https://github.com/ngxson/wllama) - 浏览器端 GGUF 推理引擎
- [llama.cpp](https://github.com/ggerganov/llama.cpp) - 底层推理实现
- [TurboWarp](https://turbowarp.org/) - Scratch 改进版运行时
- [Font Awesome](https://fontawesome.com/) - 开源图标库 (CC BY 4.0 License)
- [Simple Icons](https://simpleicons.org/) - 品牌图标库 (CC0 1.0 Universal)

---

<p align="center">
  <img src="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/svgs/solid/heart.svg" width="14" style="vertical-align:middle;"> Made by ring-operation
</p>
