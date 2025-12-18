# Vue + AI 前端学习指南 (GUIDE.md)

> **👤 学习者导航**: 这是你的核心教材，从零基础 HTML 到 AI 结对编程的完整路径。
> **🤖 AI 导航**: 这是你的教学大纲。请按章节顺序引导学习，**不要跳跃**。

---

## 🌟 核心理念：Vibe Coding

在 2026 年，编程的方式正在发生根本性转变：
*   **你不需要手写每一行代码**：AI 工具（Cursor, Windsurf, Copilot）可以帮你生成。
*   **但你必须理解基础原理**：否则你无法精准描述需求，也无法验收 AI 的产出。
*   **你的核心技能是"Prompting"**：学会如何用清晰、精准的自然语言与 AI 沟通。

---

## 🗺️ 学习路线图 (Roadmap)

| 阶段 | 章节 | 模块名称 | 核心技能 | Vibe Coding 目标 |
| :--- | :--- | :--- | :--- | :--- |
| **基础** | 01 | **HTML 语义化** | 标签、结构、语义化 | 能用自然语言描述页面骨架，让 AI 生成 HTML。 |
| **基础** | 02 | **CSS 盒子与布局** | 盒模型、Flex、Grid | 能画 ASCII 草图，让 AI 生成精准布局。 |
| **基础** | 03 | **JavaScript 逻辑** | 变量、函数、DOM、异步 | 理解数据流动，能阅读 AI 生成的 JS 代码。 |
| **进阶** | 04 | **TypeScript 契约** | 类型、接口、泛型 | 学会"Type-First"开发，先写 Interface。 |
| **框架** | 05 | **Vue 核心概念** | Setup, Ref, 生命周期 | 能向 AI 描述组件的 Props/Events/State。 |
| **框架** | 06 | **组合式 API 精通** | Composables, Pinia | 能指挥 AI 抽离业务逻辑。 |
| **实战** | 07 | **AI 结对编程** | Prompt 技巧、调试、重构 | 成为"技术总监"，高效验收 AI 代码。 |

---

## 🟢 第一章：HTML 语义化 (The Skeleton)

### 核心概念
HTML 是网页的**骨架**，它定义了内容的**结构**。AI 生成的 HTML 质量直接取决于你描述结构的精准度。

### 必须掌握的知识点
| 知识点 | 你需要理解的 | 你不需要背的 |
| :--- | :--- | :--- |
| **标签 (Tags)** | `<div>`, `<span>`, `<p>`, `<a>`, `<img>`, `<button>`, `<input>` 的作用 | 每个标签的全部属性列表 |
| **语义化 (Semantics)** | `<header>`, `<main>`, `<aside>`, `<footer>`, `<nav>`, `<section>`, `<article>` 的区别 | 所有 HTML5 标签 |
| **属性 (Attributes)** | `class` (样式钩子), `id` (唯一标识), `src` (资源路径), `href` (链接) | 各种事件属性的拼写 |

### 与 AI 沟通的模板
> "请生成一个博客文章页面的 HTML 结构。要求：
> 1. 顶部是 `<header>`，包含站点 logo 和导航链接。
> 2. 主体是 `<main>`，左边是 `<article>` 文章内容，右边是 `<aside>` 侧边栏。
> 3. 底部是 `<footer>`，包含版权信息。
> 请使用**语义化标签**，不要滥用 `<div>`。"

---

## 🔵 第二章：CSS 盒子与布局 (The Skin)

### 核心概念
CSS 控制网页的**外观**。在 Vibe Coding 时代，你不需要背诵属性，但必须理解**盒子模型**和**布局原理**。

### 必须掌握的知识点
| 知识点 | 你需要理解的 | 你不需要背的 |
| :--- | :--- | :--- |
| **盒子模型 (Box Model)** | `content` -> `padding` -> `border` -> `margin` 的层级关系 | 每个属性的简写语法 |
| **Flexbox** | 一维布局，`justify-content` (主轴对齐), `align-items` (交叉轴对齐) | 所有 flex 属性值 |
| **Grid** | 二维布局，`grid-template-columns/rows` 定义网格 | 复杂的 grid 语法 |
| **定位 (Position)** | `relative` (相对自身), `absolute` (相对父级), `fixed` (相对视口) | z-index 的所有交互规则 |

### 与 AI 沟通的模板 (附 ASCII 草图)
> "请使用 CSS Grid 生成这个布局 (Tailwind CSS)：
> ```text
> +---------------------------------------+
> | Header (全宽, 高度 64px)                |
> +---------------------------------------+
> | Sidebar (宽 240px) | Content (自适应)   |
> | (高度撑满)          | (可滚动)           |
> +--------------------|-------------------+
> ```
> 要求：Header 固定在顶部，Sidebar 固定不滚动，Content 区域可以滚动。"

---

## 🟣 第三章：JavaScript 逻辑 (The Soul)

### 核心概念
JavaScript 让网页**动起来**。你不需要手写复杂算法，但必须理解**数据如何流动**。

### 必须掌握的知识点
| 知识点 | 你需要理解的 | 你不需要背的 |
| :--- | :--- | :--- |
| **变量** | `let` (可变), `const` (不可变) 的区别 | var 的历史包袱 |
| **数据类型** | `String`, `Number`, `Boolean`, `Object`, `Array` | 类型转换的所有规则 |
| **函数** | 输入 -> 处理 -> 输出 的概念 | 箭头函数 vs function 的细微差异 |
| **DOM 操作** | 什么是 DOM，如何通过 JS "抓取"和"修改"页面元素 | getElementById 等 API 的拼写 |
| **异步 (Async)** | `Promise`, `async/await` 解决了什么问题（等待网络请求） | .then().catch() 的链式写法 |
| **数组方法** | `map` (变换), `filter` (过滤), `find` (查找) 的用途 | reduce 的复杂用法 |

### 与 AI 沟通的模板
> "我有一个用户数组，每个用户对象包含 `{ id, name, status }`。
> 请用 JavaScript 写一个函数，过滤出 `status === 'active'` 的用户，并返回一个只包含 `name` 的新数组。
> 使用 ES6 箭头函数和数组方法，不要用 for 循环。"

---

## 🟠 第四章：TypeScript 契约 (The Contract)

### 核心概念
TypeScript 是 JavaScript 的超集，它的核心价值是**类型 (Types)**。
在 Vibe Coding 中，**Type-First (契约优先)** 是黄金法则：先定义数据形状，再让 AI 生成逻辑。

### 必须掌握的知识点
| 知识点 | 你需要理解的 | 你不需要背的 |
| :--- | :--- | :--- |
| **Interface** | 如何定义一个对象的"形状" `{ name: string; age: number }` | 复杂的泛型语法 |
| **Type Alias** | `type Status = 'active' \| 'inactive'` 定义联合类型 | type vs interface 的细节差异 |
| **Optional** | `?` 表示可选属性 `avatar?: string` | 严格空检查的配置 |

### 与 AI 沟通的模板
> "请先定义以下 TypeScript 接口，然后基于它生成一个 fetch 函数：
> ```typescript
> interface Product {
>   id: number;
>   name: string;
>   price: number;
>   inStock: boolean;
> }
> ```
> 函数要求：从 `/api/products` 获取数据，返回 `Promise<Product[]>`，处理 404 和 500 错误。"

---

## 🔴 第五章：Vue 核心概念 (The Framework)

### 核心概念
Vue 是一个渐进式框架，它帮你把 HTML/CSS/JS 组合成可复用的**组件**。

### 必须掌握的知识点
| 知识点 | 你需要理解的 | 你不需要背的 |
| :--- | :--- | :--- |
| **Script Setup** | `<script setup>` 是 Vue 3 的极简写法 | Options API (旧写法) |
| **Ref** | `ref(0)` 创建一个"响应式"的值，改变它，界面自动更新 | `ref` vs `reactive` 的内部实现 |
| **模板语法** | `{{ value }}` 插值, `v-if/v-for/v-bind/v-on` 指令 | 所有指令的完整修饰符 |
| **Props** | 父组件如何向子组件传递数据 | `defineProps` 的复杂验证语法 |
| **Emit** | 子组件如何向父组件"喊话" | `defineEmits` 的复杂声明 |

### 与 AI 沟通的模板
> "请生成一个 Vue 3 组件 `UserCard.vue`：
> - 使用 `<script setup>` 和 TypeScript。
> - Props: `name: string`, `avatar?: string`, `isOnline: boolean`。
> - 如果没有 avatar，显示 name 的首字母作为占位符。
> - 使用 Tailwind CSS，风格是现代极简风，带圆角和柔和阴影。"

---

## ⚫ 第六章：组合式 API 精通 (Composables)

### 核心概念
**Composable** 是 Vue 3 的逻辑复用方式。把可复用的逻辑（如计数器、搜索、分页）抽离成 `useXxx.ts` 函数。

### 必须掌握的知识点
| 知识点 | 你需要理解的 | 你不需要背的 |
| :--- | :--- | :--- |
| **Composable 模式** | 一个返回 `{ 状态, 方法 }` 的函数，供组件使用 | VueUse 库的所有 API |
| **Pinia** | Vue 官方状态管理库，用 `defineStore` 创建全局状态 | Vuex 的 mutations/actions |
| **Setup Stores** | Pinia 的组合式写法，比 Options Store 更灵活 | Store 的复杂选项 |

### 与 AI 沟通的模板
> "请创建一个 `useCounter.ts` Composable：
> - 包含 `count` (响应式状态), `increment()`, `decrement()`, `reset()` 方法。
> - 使用 TypeScript，确保类型安全。
> - 然后创建一个 `Counter.vue` 组件来使用它。"

---

## ⚪ 第七章：AI 结对编程 (The Meta-Skill)

### 核心概念
这是最重要的一章。Vibe Coding 的精髓不是"让 AI 帮你写代码"，而是**"成为 AI 的技术总监"**。

### 必须掌握的技能
| 技能 | 描述 |
| :--- | :--- |
| **Context Feeding (上下文喂投)** | 不要问空泛问题。把相关的 Interface、已有代码一起发给 AI。 |
| **Iterative Refinement (迭代精修)** | 分步走：先让 AI 生成丑陋但能跑的版本，再美化，再优化。 |
| **Code Smell Detection (代码嗅觉)** | 能识别 AI 代码中的隐患：未清理的监听器、过深的嵌套、重复逻辑。 |
| **Debugging (调试)** | 不要只贴报错。告诉 AI："报错是 X，我的预期是 Y，我怀疑是 Z。" |

### 高质量 Prompt 范例
> "我正在开发一个任务管理应用。
> **上下文**:
> 1. 任务接口: `interface Task { id: string; title: string; done: boolean }`
> 2. 我用的是 Vue 3 + Pinia + Tailwind。
> **任务**:
> 请帮我生成一个 `TaskItem.vue` 组件：
> - 显示任务标题，左侧有 checkbox。
> - 点击 checkbox 切换 `done` 状态，并 emit `update` 事件通知父组件。
> - 已完成的任务标题显示删除线。
> - 点击任务标题右侧有一个删除按钮，emit `delete` 事件。"

---

## 🛠️ 推荐工具链 (2026 Edition)

| 类别 | 工具 | 说明 |
| :--- | :--- | :--- |
| **IDE** | **Cursor** / Windsurf | AI-Native 编辑器，内置 Chat 和 Composer。 |
| **Framework** | **Vue 3（优先最新稳定版）** | 默认使用 `<script setup>`；涉及实验/预览特性时先以官方文档确认。 |
| **Build** | **Vite（优先最新稳定版）** | 以官方推荐配置为准；如回答基于特定版本会提前声明。 |
| **State** | **Pinia（优先最新稳定版）** | 推荐 Setup Store 风格；如项目未使用 Pinia 会给替代方案。 |
| **Styling** | **Tailwind CSS（可选）** | 优先遵循项目现有样式方案；必要时提供原生 CSS 版本。 |
| **Language** | **TypeScript（优先最新稳定版）** | Type-First；必要时说明 `tsconfig` 假设（如 `strict`）。 |

---

## 📚 推荐资源
*   Vue 官方文档: [vuejs.org](https://vuejs.org)
*   Vite 官方文档: [vite.dev](https://vite.dev)
*   Tailwind CSS 文档: [tailwindcss.com](https://tailwindcss.com)
*   MDN Web Docs: [developer.mozilla.org](https://developer.mozilla.org)
