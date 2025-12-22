| 章节 | 主题 | 掌握 | 信心 | 首次学习 | 上次复习 |
|------|------|------|------|----------|----------|
| 01 | HTML 语义化 | [ ] | - | - | - |
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
  - 待补强：`div`（无语义通用容器） vs `section`（主题分区语义）的选择标准。（Confidence: Low）
  - 已理解倾向：纯布局包裹可用 `div`；若明确是“可命名的功能区块”，可升级为 `section` + 标题/aria-label。（Confidence: Medium）
  - 能写出基本语义结构树：`header>nav`、`main>(article>section[评论]) + aside[作者/推荐]`、`footer`。（Confidence: Medium）
