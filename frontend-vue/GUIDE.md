# Vue + AI 前端学习指南 (GUIDE.md)

> **👤 学习者**: 罗智鍹
> **🤖 AI 导师**: 2026 前端架构师
> **核心原则**: 拒绝走马观花。每一个章节必须包含：概念理解、代码识谱、Vibe 练习。

---

## 🗺️ 深度学习路线图

### 🟢 第一章：HTML 网页骨架 (The Skeleton)
*深度目标：不仅是标签，更是结构思维。*
- **1.1 语义化基石**: 为什么要用 `<main>` 而不是 `<div>`？对 AI 和 SEO 的影响。
- **1.2 表单与交互**: `<input>`, `<button>`, `<select>`, `<form>` —— 网页收集数据的唯一入口。
- **1.3 多媒体与链接**: `<img>`, `<a>`, `<iframe>` 以及路径引用的陷阱。
- **1.4 Meta 与 Head**: 网页的幕后功臣（标题、字符集、视口配置）。

### 🔵 第二章：CSS 视觉艺术 (The Skin)
*深度目标：掌握布局的物理规律，告别乱试代码。*
- **2.1 盒子模型深度游**: Padding/Margin 对点击区域的影响，`box-sizing` 的秘密。
- **2.2 选择器与层叠**: 谁的样式会生效？优先级 (Specificity) 计算规则。
- **2.3 Flexbox 一维布局**: 主轴/交叉轴，`flex-grow` 与 `flex-shrink` 的动态挤压。
- **2.4 Grid 二维布局**: 网格区域划分，实现复杂的仪表盘布局。
- **2.5 响应式设计**: 媒体查询 (Media Queries) 与 Mobile-First 策略。
- **2.6 Tailwind CSS 进阶**: 常用原子类、状态前缀 (hover/active/focus)、暗黑模式切换。

### 🟣 第三章：JavaScript 逻辑灵魂 (The Soul)
*深度目标：理解浏览器的运行机制与异步数据流。*
- **3.1 数据仓库**: `const/let` 作用域，String/Number/Boolean/Object/Array/Null/Undefined 辨析。
- **3.2 逻辑指挥官**: 条件判断 (if/else/switch)、逻辑运算符 (&&, ||, !)、循环 (map/filter/forEach)。
- **3.3 动作包装盒**: 函数声明、箭头函数、回调函数 (Callback)、闭包 (Closure) 初探。
- **3.4 DOM 翻译官**: 事件监听 (addEventListener)、DOM 增删改查、属性操作。
- **3.5 时空管理 (异步)**: Promise 状态机、async/await 优雅处理、Fetch API 实战。

### 🟠 第四章：TypeScript 严谨契约 (The Contract)
*深度目标：在写代码前，先定义数据的“形状”。*
- **4.1 基础类型系统**: 显式声明 vs 自动推断，联合类型 (Union Types)。
- **4.2 Interface 与 Type**: 定义对象结构、可选属性、只读属性。
- **4.3 泛型初步**: 编写可复用的“类型模板”。

### 🔴 第五章：Vue 3 核心引擎 (The Framework)
*深度目标：掌握组件化思维与响应式原理。*
- **5.1 响应式核心**: `ref` 与 `reactive` 的选择，`computed` 计算属性的缓存威力。
- **5.2 模板指令**: `v-if/v-for` 的就地复用陷阱，`v-model` 双向绑定的原理。
- **5.3 组件通信**: Props 向下传递，Emits 向上喊话，插槽 (Slots) 灵活分发。
- **5.4 生命周期**: 挂载 (onMounted) 与 卸载 (onUnmounted) 的应用场景。

### ⚫ 第六章：Vue 实战工程 (Engineering)
- **6.1 Composables**: 逻辑抽离与复用，编写属于你的 `useXxx` 函数。
- **6.2 Pinia 状态管理**: 全局“单一真相来源”，Setup Store 模式。
- **6.3 Vue Router**: 单页应用 (SPA) 的导航逻辑，路由守卫。

### ⚪ 第七章：AI 结对编程 (Vibe Coding Meta)
- **7.1 高级 Prompt 技巧**: 上下文喂投、思维链 (CoT) 引导、错误复现模板。
- **7.2 代码嗅觉与重构**: 如何识别 AI 生成的冗余逻辑，进行性能优化。
