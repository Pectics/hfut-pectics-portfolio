# 个人网站（Vue）课程期末项目 — 项目计划与总结报告

## 1. 网站设计目的
基于 Vue 3 搭建一个简洁的个人展示型网站，集中呈现我的基本信息与项目实践，作为课程期末项目的成果展示。

## 2. 使用技术
- 前端框架：Vue 3
- 构建工具：Vite
- 路由：Vue Router
- 组件写法：`<script setup>`
- 样式：原子化的自定义 CSS（未引入 UI 库，保持轻量）

## 3. 页面结构与功能
- **Home**：欢迎语、关键词标签、引导按钮跳转 About。
- **About**：个人信息（姓名/网名、学校、专业、学号）与技术兴趣列表。
- **Projects**：使用 `v-for` 动态渲染的项目数组，包含名称、描述与可选链接。
- **Navbar/Footer**：全局导航与页脚，导航高亮当前路由。

目录结构遵循约定：`src/components` 放置 Navbar、Footer；`src/pages` 放置 Home/About/Projects；`src/router` 管理路由；`src/assets/main.css` 提供全局样式。

## 4. 动态性实现方式
1. **路由切换**：使用 Vue Router 配置 `/`、`/about`、`/projects` 三条路由，`<RouterView>` 负责页面动态加载。
2. **数据驱动列表**：`Projects.vue` 中的项目数组通过 `v-for` 渲染，实现动态内容展示。
3. **导航高亮**：在路由配置中自定义 `linkActiveClass`，配合样式让当前页面的导航项高亮。

## 5. 源码截图（文字化说明）
- `src/pages/Home.vue`：展示欢迎语、关键词标签、按钮跳转。
- `src/pages/About.vue`：两列布局呈现基本信息与技术兴趣。
- `src/pages/Projects.vue`：卡片列表使用 `v-for` 渲染项目数据。
- `src/components/Navbar.vue`：包含导航链接与高亮状态样式。

## 6. 调试过程与运行方式
- 本地安装依赖：`npm install`
- 开发调试：`npm run dev`
- 生产构建：`npm run build`

调试过程中确认：路由切换无报错，导航高亮正常，Projects 列表随数组变化自动更新。

## 7. 总结与心得（约 200 字）
本次项目聚焦于 Vue 3 基础能力的练习。从搭建 Vite 工程到拆分路由与组件，进一步理解了组合式 API 与 `<script setup>` 的简洁性。项目刻意保持轻量化，没有引入额外 UI 库，以便把精力放在路由切换、数据驱动渲染和样式统一性上。实现导航高亮与 `v-for` 列表让我体会到响应式数据流带来的效率；同时，通过模块化的目录结构，后续扩展页面（如 Contact/Gallery）也会更加顺畅。整体过程证明：清晰的结构、适度的样式和恰当的动态交互，足以支撑一个可维护的个人展示站点。
