# Session Notes: 2025-12-22

## 1. 讨论内容 (Topics Discussed)

### Question 1: HTML 是什么？语义化在描述什么？
- **Student's Question**: 我对 HTML 的理解是描述网页展示的文件，也可以与其他服务沟通（例如 `<html>`、`<script>`）。
- **Initial Understanding**: 认为“语义化”更偏“功能行为”，且不太记得具体语义化标签。
- **Explanation Given**: 语义化 HTML 主要描述“结构含义”（页面区域与内容角色），而行为/交互属于 JavaScript（如 `<script>`）。常见拆分：`header`（站点抬头）、`main`+`article`（主要内容/文章）、`aside`（侧栏）、评论区可用 `article` 内的 `section`；整站页脚才用 `footer`。
- **Comprehension Checks**: 让学生将博客文章页拆分为区域并选择标签；学生选择评论区放在 `article` 内的 `section`，理由：`footer` 更像整站页脚标识，评论区属于文章内容的一部分。
- **Understanding Level**: Medium

### Question 2: 为什么 `aside` 通常放在 `main` 内？
- **Student's Question**: 我的理解是：`header/footer` 是网页固定的标识；其他信息来自数据库/后端获取，应当作为正文都放在 `main` 里面。
- **Initial Understanding**: 用“数据来源（静态/动态）”来判断结构归属。
- **Explanation Given**: 语义化的划分依据是“内容角色/主次关系/站点级结构”，而不是“数据是不是后端来的”。`main` 承载页面主内容；`aside` 是对主内容的补充信息，常与 `article` 并列放在 `main` 内。
- **Comprehension Checks**: 通过“导航菜单是否放在 `header nav` 还是 `main`”的反例澄清判断依据；学生最终认为全站通用导航更像站点级结构的一部分。
- **Understanding Level**: Medium

### Question 3: `nav` 是什么？导航放哪？
- **Student's Question**: 不清楚 `header` 里的 `nav` 是什么标签；导航菜单是否应放在 `main`？
- **Initial Understanding**: 认为导航不代表整页标识，所以更像内容，倾向放 `main`。
- **Explanation Given**: `nav` 表示“导航区域”，包住主要导航链接（主导航/目录/面包屑等）；若导航是跨页面复用的站点级结构，常放在 `header`（或侧栏）中。
- **Comprehension Checks**: 学生判断“全站每页都有的导航”更像站点级结构的一部分。
- **Understanding Level**: Medium

### Question 4: 相关文章推荐放哪？
- **Student's Question**: 相关文章推荐放在 `aside` 还是 `nav`？
- **Initial Understanding**: 已理解 `nav` 是站点级全局导航。
- **Explanation Given**: -
- **Comprehension Checks**: 学生选择放在 `aside`，理由：与当前文章（`article`）相关的辅助内容，不是全站导航。
- **Understanding Level**: High

### Question 5: “除了 `<script>` 都是结构吗？”以及点赞交互怎么放？
- **Student's Question**: 是否可以理解为除 `<script>` 外都是“结构含义/身份”；点赞评论等动作都在 `<script>` 里；能否给一个包含点赞功能的详细 HTML？
- **Initial Understanding**: 将“非 `<script>`”等同于“纯结构容器”。
- **Explanation Given**: “语义/结构标签”指 `header/nav/main/article/section/aside/footer` 等用来标识内容角色的容器；但 HTML 里也有大量“交互控件标签”（如 `button/a/input/form`）本身就代表可交互元素。复杂行为（例如点赞计数、发请求）通常由 JS（`<script>`）驱动，但交互入口是控件标签（`<button>`）。
- **Comprehension Checks**: 让学生判断点赞交互应由 `button` 作为入口，`script` 负责事件与状态更新。
- **Understanding Level**: Medium

### Question 6: `div` vs `section` 怎么选？
- **Student's Question**: `div` 不算结构标签，只是用于布局明确层级；但不清楚 `div` 和 `section` 的使用区别。
- **Initial Understanding**: 认为 `div` 仅是布局容器，缺少语义；对 `section` 的“主题分区”概念不牢。
- **Explanation Given**: `section` 表示“有明确主题/可命名”的内容分区（通常能自然配一个标题或 aria-label，如“评论区/相关文章”）；`div` 是无语义通用容器，多用于纯布局/包裹/样式钩子。交互按钮本身用 `button`，外层包裹是否用 `section` 取决于你是否把它当作一个“功能区块”（例如“文章互动”）。
- **Comprehension Checks**: 问“文章互动区（点赞/收藏/分享）”更适合 `section` 还是 `div`；学生倾向用 `div` 进行包裹。
- **Understanding Level**: Medium

### Question 7: 结构树与 `div` 分组的使用
- **Student's Question**: 给出文章页结构树，并说明哪里用 `div` 做分组布局容器。
- **Initial Understanding**: 能写出 `header > nav`、`main > (article > section[评论]) + aside[作者/推荐]`、`footer` 的层级；倾向用 `div` 对正文部分进行统一管理样式。
- **Explanation Given**: -
- **Comprehension Checks**: -
- **Understanding Level**: Medium

### Practice 1: 以掘金文章页做语义骨架
- **Task**: 以“掘金文章页”为例，拆分站点级结构与文章级结构，并补齐“互动区”与 `div vs section` 判定。
- **Student's Answer**:
  - 顶部整站栏：`header`；主导航：`header > nav`
  - 页面主体：`main`
  - 正文：`article`
  - 评论区：`article` 内的 `section`
  - 右侧栏：`main` 内的 `aside`
  - 底部整站信息：`footer`
  - 互动区：更像 `article` 的补充（针对这篇文章的操作），交互入口用 `button`
- **Clarifications**:
  - `nav` 只包导航链接区域；搜索/登录等入口不一定属于 `nav`
  - “互动区”容器可用 `section aria-label="文章互动"`（明确可命名的功能区）；如果只是为布局/包裹/样式钩子则用 `div`
  - `div vs section` 最小判定：`section = 可命名的主题/功能区`；`div = 纯布局/包裹/样式钩子`
- **Mini Quiz (Result)**:
  - 两列布局包裹（article + aside）：`div` ✅
  - “相关推荐”模块：`section` ✅
  - 仅为背景/间距包一层：`div` ✅

### Practice 2: 标题层级、目录与交互控件语义
- **Task**: 用“水果文章”练习 `h1/h2/h3`、文章目录（`nav`）与交互控件（`button/a`）的语义选择。
- **Key Takeaways**:
  - 目录（文章内锚点跳转）用 `nav`，不局限于 `header`；侧栏目录可用 `aside > nav`
  - `h1` 通常为文章标题；`h2` 为一级分区；`h3` 为某个 `h2` 的子分区
  - `nav` 提供跳转链接，正文用对应 `id` 的 `h2/h3` 作为目标点
  - `button` 用于触发动作（点赞/打开弹窗/复制），`a` 用于地址跳转（去分享页等）
- **ARIA Quick Notes**:
  - `aria-haspopup="dialog"`：按钮会弹出对话框
  - `aria-controls="id"`：按钮控制的目标元素
  - `aria-expanded="true/false"`：展开/打开状态（如弹窗是否打开）
  - `role="dialog" aria-modal="true"`：声明模态对话框
  - `aria-labelledby="id"`：用标题元素为弹窗命名（优于只用 `aria-label`）

## 2. 知识盲区 (Knowledge Gaps)
- [ ] 区分“语义（结构含义）” vs “行为（脚本/交互）”
- [ ] 能举例并正确使用常见语义化标签（`header/main/nav/article/section/aside/footer`）
- [ ] 不以“数据来源（后端/静态）”作为语义化依据，而以“内容角色/主次关系”来划分
- [ ] 能在真实页面中为 `section` 补齐“可命名依据”（标题或 `aria-label`），避免滥用 `section`
- [ ] 理解“文章级 `header`”与“站点级 `header`”的区别（同名标签但语义范围不同）
- [ ] 理解表单可访问性最小集：`label`、`type="submit"`、错误提示关联（`aria-describedby`）
- [ ] 掌握内容语义标签：`time`、`figure/figcaption`、`code/pre`、`blockquote`、`strong/em` 的使用场景
- [ ] 掌握列表/定义列表的选择：`ul/ol/li` vs `dl/dt/dd`
- [ ] 掌握图片与媒体：`img`（`alt`）、`video`（基础属性）与何时用它们

## 3. 今日掌握 (Topics Mastered)
- 区分语义（结构含义）与行为（脚本/交互）（Confidence: Medium）
- 能将博客文章页拆成 `header/main/article/aside`，并将评论区放在 `article` 内的 `section`（Confidence: Medium）
- 能区分站点级导航（`nav`）与文章相关辅助内容（`aside`）（Confidence: High）
- 能用掘金文章页给出语义骨架，并把互动区归为文章级内容：入口用 `button`，容器按“可命名”选择 `section/div`（Confidence: Medium）
- 已形成 `div vs section` 的最小判定规则：`section = 可命名主题/功能区`；`div = 纯布局/包裹/样式钩子`（Confidence: Medium）
- 理解 `button` vs `a` 的语义边界，并能用最小 ARIA 描述“按钮打开弹窗”的关系与状态（Confidence: Medium）
- 已覆盖标签清单（本章已学/已用）：`header/nav/main/article/section/aside/footer`、`h1/h2/h3`、`div`、`a`、`button`、`form`、`label`、`input`、`textarea`、`ul/li`、`p`（Confidence: Medium）

## 4. 下次预告 (Action Items)
- [ ] 完成第 01 章：独立写出“掘金文章页”骨架 HTML（含文章级 `header`、互动区、评论区、右侧栏）
- [ ] 练习：把 10 个常见模块分别判断 `div`/`section`，并为每个 `section` 写出标题或 `aria-label`
- [ ] 练习：为“评论表单”补齐最小可访问性（`label`、必填/错误提示、提交按钮语义）
