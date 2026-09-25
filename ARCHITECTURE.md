# ARCHITECTURE 3.0

本项目继续保持 GitHub Pages 兼容的纯 HTML、CSS 和 Vanilla JavaScript，不引入构建系统或大型 UI 框架。Supabase 仍然是公开文章、评论、留言和媒体的云端数据源。

## 页面

`index.html` 负责首页和阅读模式；`post.html` 负责独立文章；`archive.html`、`topics.html`、`about.html`、`friends.html`、`guestbook.html` 和 `404.html` 负责不同档案入口。所有页面都使用普通相对链接，支持 GitHub Pages 子路径刷新。

## 共享层

`site.js` 保存 Supabase 客户端、数据查询、转义、日期格式、文章卡、全局导航、档案侧边栏和图片灯箱。`site.css` 保留旧页面样式，并在末尾以 progressive layer 方式加入 ARCHIVE 3.0 的视觉规则，从而避免一次性重写破坏现有功能。

`assets/css/variables.css` 集中保存品牌颜色、字体、阴影和暗色主题 token。`assets/js/navigation.js` 与 `assets/js/theme.js` 是后续逐步把首页内联初始化迁出的模块入口；当前首页保留兼容性初始化，避免破坏既有 Supabase、搜索和阅读模式。

## 数据

`data/settings.json`、`data/topics.json` 和 `data/projects.json` 保存不依赖 Supabase 的公开配置和编辑策划数据。文章仍以 Supabase 为唯一在线来源，避免云端和静态副本发生不透明冲突。

## 质量约束

每个页面有独立标题和 description；公开图片使用 alt 和 lazy loading；文章图片支持键盘打开灯箱；页面支持 `prefers-reduced-motion`；侧边栏在桌面固定、平板横向收缩、手机转为顶部索引条；暗色主题使用纸张档案色板而不是纯黑纯白。
