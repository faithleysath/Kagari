![Kagari](https://socialify.git.ci/faithleysath/Kagari/image?custom_description=%E4%B8%BA%E4%B8%8B%E4%B8%80%E4%BB%A3+AI+%E5%8F%99%E4%BA%8B%E6%B8%B8%E6%88%8F%E8%80%8C%E7%94%9F%E3%80%82%E4%B8%80%E4%B8%AA%E4%BD%93%E9%AA%8C%E9%A9%B1%E5%8A%A8%E3%80%81%E5%B0%8F%E6%A8%A1%E5%9E%8B%E5%8F%8B%E5%A5%BD%E7%9A%84%E5%BC%80%E6%BA%90%E6%A1%86%E6%9E%B6%E3%80%82&custom_language=React&description=1&forks=1&issues=1&language=1&logo=https%3A%2F%2Fraw.githubusercontent.com%2Ffaithleysath%2FKagari%2Frefs%2Fheads%2Fmain%2Flogo%2Flogo.svg&name=1&owner=1&pattern=Plus&pulls=1&stargazers=1&theme=Auto)

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-5-646CFF?logo=vite)](https://vitejs.dev/)

**Kagari (篝火)** 是一个开源的、体验驱动的叙事游戏框架，旨在彻底改变 AI 驱动的 TRPG 体验。

我们的理念：**最好的故事值得被“玩”出来，而不仅仅是被“读”出来。**

Kagari 不再是一个纯文本的聊天窗口，它是一个真正的**游戏引擎**，旨在将 LLM 驱动的 TRPG 冒险转变为媲美视觉小说 (VN) 和推理游戏 (AVG) 的沉浸式体验。

## 📖 目录

* [核心特性](#-核心特性)
* [我们的理念](#-我们的理念)
* [路线图](#-路线图)
* [快速开始](#-快速开始)
* [贡献指南](#-贡献指南)
* [许可证](#-许可证)

## ✨ 核心特性

Kagari 将 LLM 的文本输出结构化为游戏指令，实现传统聊天无法比拟的丰富体验。

* **🎮 结构化游戏界面 (Structured UI)**
    * 告别满屏的文字选项。Kagari 将 LLM 的指令解析为真正的 UI 组件——选项按钮、角色面板、道具栏，提供游戏级的交互体验。

* **🎨 沉浸式氛围 (Immersive Atmosphere)**
    * 由 AIGC 实时驱动的场景插图和动态 BGM，让你的每一步冒险都“声”临其境。

* **🧠 双 Agent 辅助 (Dual-Agent Assistance)**
    * **玩家 Agent (书记官):** 自动“观看”剧情，以玩家的有限视角总结和归类所有已知信息（人物、地点、线索、物品），并呈现在 UI 上。
    * **作家 Agent (小说家):** 游戏结束后，自动将你的冒险历程（包括 GM 描述和玩家选择）创作为一部文笔优美、可供收藏的同人小说。

* **🗺️ 宏观游戏管理 (Macro Management)**
    * 支持“战争迷雾”世界地图，GM (LLM) 可以动态点亮玩家已探索的区域。
    * 支持剧情检查点 (Checkpoints)，允许玩家清晰地查阅进度、存档，并从任意节点“回档”以探索不同分支。

## 💡 我们的理念

### 🚀 体验驱动 (Experience-Driven)

Kagari 的 V1.0 专注于一件事：**体验**。我们优先实现那些能立刻将“纯文本跑团”与“真正游戏”区分开来的功能。我们利用最强大的 LLM（如 Gemini 2.5 Pro）作为“完美黑盒”，优先交付华丽的“样板房”。

### 💡 小模型友好 (Small-Model Friendly)

这是 Kagari 的 V2.0 愿景，也是项目的核心护城河。我们深知昂贵的 API 无法让开源项目走向普惠。我们的长期目标是通过构建**记忆核心 (RAG + 知识图谱)**，将“记忆”的负担从 LLM 的上下文窗口转移到数据库中。

这将使得使用更便宜、更小型、甚至本地部署的模型（如 Llama 3, Qwen 2）成为可能，让高性能的叙事游戏体验真正“小模型友好”。

## 🗺️ 路线图

-   **[V1.0 - 体验驱动] (进行中)**
    -   [ ] 基于 React 和 PWA 的基础框架
    -   [ ] 结构化 UI（按钮、面板）
    -   [ ] AIGC 插图集成
    -   [ ] 动态 BGM 控制
    -   [ ] 玩家 Agent (书记官)
    -   [ ] 作家 Agent (小说家)
    -   [ ] 地图与剧情检查点

-   **[V2.0 - 普惠友好] (规划中)**
    -   [ ] **记忆核心：** 集成向量数据库 (RAG)
    -   [ ] **记忆核心：** 集成知识图谱（用于状态管理）
    -   [ ] 适配并优化小型/本地 LLM

-   **[V3.0 - 终极形态] (实验性)**
    -   [ ] **动态 UI Agent：** 允许 LLM 不仅叙述故事，更能动态生成匹配玩法的独特 UI（如模拟终端、炼金台等）。

## 🚀 快速开始

*本项目仍在早期开发中。*

1.  克隆仓库：
    ```bash
    git clone [https://github.com/faithleysath/Kagari.git](https://github.com/faithleysath/Kagari.git)
    ```
2.  安装依赖：
    ```bash
    cd Kagari
    npm install
    ```
3.  运行开发服务器：
    ```bash
    npm run dev
    ```

## 🤝 贡献指南

我们热烈欢迎所有形式的贡献，无论是新功能、Bug 修复、文档改进还是剧本创作！

1.  Fork 本仓库
2.  创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3.  提交你的更改 (`git commit -m 'Add some AmazingFeature'`)
4.  推送到分支 (`git push origin feature/AmazingFeature`)
5.  提交一个 Pull Request

## ⚖️ 许可证 (License)

本项目采用 **GNU Affero General Public License v3.0 (AGPL-3.0)** 许可证。

这是一个强 copyleft 许可证。简而言之，这意味着：

1.  **开源义务：** 你可以自由地修改、分发和使用 Kagari 的代码。
2.  **网络条款：** 如果你修改了 Kagari 的代码，并通过网络（例如作为一个网站或 PWA）向公众**提供服务**，你**必须**以同样的 AGPL-3.0 许可证，向所有用户提供你修改后的**完整源代码**。

我们选择 AGPL-3.0 是为了确保 Kagari 及其衍生作品始终保持开源和自由，防止其被“闭源 SaaS 化”，从而保护整个社区的成果。