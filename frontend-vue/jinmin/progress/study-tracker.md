| 章节 | 主题 | 掌握 | 信心 | 首次学习 | 上次复习 |
|------|------|------|------|----------|----------|
| 01 | HTML 语义化 | [ ] | Medium | 2025-12-22 | 2025-12-23 |
| 02 | CSS 盒子与布局 | [ ] | - | - | - |
| 03 | JavaScript 逻辑 | [ ] | - | - | - |
| 04 | TypeScript 契约 | [ ] | - | - | - |
| 05 | Vue 核心概念 | [ ] | - | - | - |
| 06 | 组合式 API 精通 | [ ] | - | - | - |
| 07 | AI 结对编程 | [ ] | - | - | - |

- 2025-12-22：开始第 01 章（HTML 语义化），当前对“语义=结构含义”与“行为=脚本交互”的边界还不清晰。
  - 已能明确：评论区属于文章内容的一部分，通常放在 `article` 内的 `section`；整站级信息才放 `footer`。（Confidence: Medium）
  - 需要纠正的判断依据：语义化不看“是否来自后端”，而看“在页面里扮演的角色”（主内容/辅助内容/站点级结构）。（Confidence: Medium）
  - 已能判断：跨页面复用的导航属于站点级结构，常用 `header > nav` 表达。（Confidence: Medium）
  - 已能判断：与当前内容相关的辅助信息（如“相关文章推荐”）更适合放 `aside`，而不是 `nav`。（Confidence: High）
  - 关键区分：语义标签（结构/角色）≠ 交互控件；交互入口通常是 `button/a/input/form`，复杂行为由 `script` 驱动。（Confidence: Medium）
  - 交互控件语义补强：`button`（触发动作）vs `a`（跳转地址）；目录锚点导航使用 `nav`。（Confidence: Medium）
  - ARIA 最小集：`aria-haspopup/controls/expanded` 描述“按钮打开弹窗”，`role="dialog" aria-modal aria-labelledby` 描述模态对话框。（Confidence: Medium）
  - 已形成最小判定：`section = 可命名的主题/功能区`；`div = 纯布局/包裹/样式钩子`。（Confidence: Medium）
  - 以掘金文章页验证：互动区更像 `article` 的补充内容；入口用 `button`，容器按“可命名”选择 `section/div`。（Confidence: Medium）
  - 能写出基本语义结构树：`header>nav`、`main>(article>section[评论]) + aside[作者/推荐]`、`footer`。（Confidence: Medium）

- 2025-12-23：补强交互与表单（继续第 01 章）。
  - 已能区分：`button`（触发动作） vs `a`（跳转地址），并能解释目录为什么用 `nav`。（Confidence: Medium）
  - 已能补齐：表单 `label for=id`、字段 `name`、`textarea` 与 `input` 的正确选择；理解 `aria-invalid/aria-describedby` 的错误提示关联。（Confidence: Medium）
  - 待继续：补齐常用内容语义（`time/figure/code/blockquote`）与媒体标签 `img alt`。（Confidence: Low）
