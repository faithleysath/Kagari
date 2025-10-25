# Kagari (篝火) - 技术栈 (Technical Stack)

Kagari (篝火) 的技术栈是围绕**性能、现代开发体验 (DX) 和前瞻性**来构建的。我们选择的工具旨在实现快速的开发迭代、极高的运行时性能和无缝的跨平台 PWA 体验。

## 1. 核心基础 (Core Foundation)

| 类别 | 技术 | 角色 |
| :--- | :--- | :--- |
| **运行时 & 工具链** | **[Bun](https://bun.sh/)** | JavaScript 运行时、包管理器、打包器、测试运行器 |
| **开发 & 构建** | **[Vite](https://vitejs.dev/)** | 下一代前端工具，提供极速的 HMR (热模块替换) |
| **语言** | **[TypeScript](https://www.typescriptlang.org/)** | JavaScript 的超集，提供强类型支持 |
| **UI 库** | **[React](https://react.dev/)** | 用于构建用户界面的 JavaScript 库 |

### 为什么这样选?

  * **Bun (as All-in-One Toolkit):** 我们选择 Bun 作为首选的运行时和包管理器，因为它提供了无与伦比的性能。它极大地加快了依赖安装 (`bun install`) 和脚本运行 (`bun run`) 的速度。它内置的工具链（打包器、测试器）简化了我们的开发依赖，使项目保持轻量和高速。
  * **Vite (as Dev Server):** Vite 提供了近乎瞬时的服务器启动和闪电般的 HMR，这是实现卓越开发者体验的关键。它使我们能够即时看到 UI 和功能的更改。
  * **React & TypeScript:** React 的组件化模型是构建 Kagari 复杂 UI（如面板、对话框、仪表盘）的理想选择。TypeScript 为这个开源项目提供了必要的代码健壮性和可维护性，使协作变得更安全、更高效。

## 2. 核心架构与功能 (Architecture & Features)

| 类别 | 技术 | 角色 |
| :--- | :--- | :--- |
| **状态管理** | **[Jotai](https://jotai.org/)** | 原子化的 (Atomic) 状态管理库 |
| **CSS 样式** | **[TailwindCSS](https://tailwindcss.com/)** | Utility-First (功能优先) 的 CSS 框架 |
| **路由** | **[React Router](https://reactrouter.com/)** | 声明式的客户端路由库 |
| **应用形态** | **PWA** | 渐进式 Web 应用，实现原生般的安装和离线体验 |

### 为什么这样选?

  * **Jotai (for State Management):** Kagari 的 UI 状态是高度分散的（例如：`isMapOpen`, `currentBgmTrack`, `playerStats`）。Jotai 的原子化模型允许我们创建微小、独立的“状态原子”，并以一种高性能、自下而上的方式管理它们。这避免了大型、单一 store 带来的复杂性和不必要的重渲染。
  * **TailwindCSS (for Styling):** 为了实现《审美指南》中定义的独特、风格化的视觉效果，我们需要一个能够快速迭代的 CSS 解决方案。TailwindCSS 的 Utility-First 方法使我们能够直接在 JSX/TSX 中构建复杂、响应式的设计，而无需编写单独的 CSS 文件或担心命名冲突。
  * **React Router (for Routing):** 作为 React 生态的标准路由库，它为 Kagari 提供了管理不同视图（如主屏 "篝火" 界面、游戏界面、设置界面）所需的灵活性和强大功能。
  * **PWA (for Immersive Experience):** PWA 是实现 Kagari “沉浸式”目标的核心。它允许用户将 Kagari “安装”到他们的桌面或移动设备上，提供全屏、无地址栏的原生应用体验，并为未来的离线功能（如缓存剧本和资源）打下基础。

## 3. 前瞻性构建 (Bleeding-Edge Tooling)

这是 Kagari 技术栈中最具前瞻性的部分，旨在利用生态系统中的最新进展来最大化性能和简化代码。

| 类别 | 技术 | 角色 |
| :--- | :--- | :--- |
| **React 优化** | **[React Compiler](https://www.google.com/search?q=https://react.dev/blog/2024/02/15/react-labs-what-we-been-working-on-february-2024%23react-compiler)** | 一个**自动优化**的编译器，无需 `useMemo` / `useCallback` |
| **Vite 插件** | **`rolldown-vite`** | 一个实验性插件，用 [Rolldown](https://github.com/rolldown/rolldown) 替代 Vite 的生产构建器 |

### 为什么这样选?

  * **React Compiler (for Logic-First Code):** React Compiler (前身为 "Forget") 是 React 的未来。它会自动将 React 代码进行 memoization 优化，使我们不再需要手动包裹 `useMemo` 和 `useCallback` 来防止不必要的重渲染。这极大地简化了我们的代码库，让我们可以专注于**业务逻辑**，而不是 React 的性能调优。
  * **Rolldown (for Ultimate Build Speed):** 我们选择 `rolldown-vite` 是一个前瞻性的赌注。Vite 目前在开发时使用 `esbuild`，在生产构建时使用 `Rollup`。**Rolldown** 是一个用 Rust 编写的新一代 JavaScript 打包器，旨在**同时取代** `esbuild` 和 `Rollup`，提供统一的、闪电般的构建体验。通过早期采用，我们确保 Kagari 始终站在 Vite 生态系统性能的最前沿。