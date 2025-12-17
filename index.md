# AI Study System

> 多人多技术栈的AI驱动学习平台

---

## 简介

本项目基于 [CFP-Study](https://github.com/chenran818/CFP-Study) 的成功经验，将苏格拉底式AI学习方法扩展为支持**多用户、多技术栈**的学习系统。

### 核心理念

1. **概念优于语法** - 在AI时代，记忆语法已过时，聚焦深层理解
2. **混合知识库** - 本地资料 + 实时联网搜索官方文档
3. **苏格拉底式引导** - AI通过提问验证理解，而非直接给答案
4. **代码必须可运行** - 所有示例代码确保可执行

---

## 快速开始

### 1. 选择技术栈

| 技术栈 | 目录 | 状态 |
|--------|------|------|
| 前端 & Vue | `frontend-vue/` | ✅ 可用 |
| Python后端 | `python-backend/` | 🔜 规划中 |
| 自动化测试 | `autotest/` | 🔜 规划中 |

### 2. 进入学习

```bash
# 示例：开始Vue学习
cd frontend-vue

# 在IDE中打开，让AI读取 VUE_TUTOR.md
# 然后开始提问：
# "我想学习Vue 3的响应式原理，我是luozhixuan。"
```

### 3. 添加新用户

在对应技术栈目录下创建用户文件夹：

```bash
mkdir frontend-vue\your_name\sessions
# 复制 progress.md 模板到你的文件夹
```

---

## 目录结构

```text
ai_study/
├── index.md                  # 本文件
├── FINAL_DESIGN.md           # 设计文档
│
├── frontend-vue/             # 前端技术栈
│   ├── VUE_TUTOR.md          # AI导师指令
│   ├── index.md              # 技术栈说明
│   ├── resources/            # 学习资料
│   └── luozhixuan/           # 用户空间
│
└── [其他技术栈]/
```

---

## 参与者

| 用户 | 技术栈 | 状态 |
|------|--------|------|
| luozhixuan | frontend-vue | 🟢 学习中 |

---

## 参考资料

- [CFP-Study 原项目](https://github.com/chenran818/CFP-Study)
- [设计文档](./FINAL_DESIGN.md)
