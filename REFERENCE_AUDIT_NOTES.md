# 参考站对比证据

参考 URL：

- https://blog.jitsu.top/
- https://blog.jitsu.top/index.php/archives/36/
- https://blog.jitsu.top/index.php/category/default/
- https://blog.jitsu.top/index.php/archives.html

## 关键观察

参考站首页有首页、分类、页面、友链、搜索入口；页面组包含友情链接、留言板、文章归档；有热门文章、最新评论、随机文章、标签云、博客统计、文章与评论 RSS。参考站文章 URL 是独立的 `/index.php/archives/36/`，文章页显示作者、日期、浏览量、评论数、字数、分类、分享、目录、评论回复等。

参考站首页实测可见约 22 篇文章和 178 条评论；抽样文章显示 171/172 次浏览、5 条评论、2791 字数。首页按页码 1–5 导航，归档按年月聚合。

视觉对比：当前博客的暖白纸感、砖红/墨绿、衬线大标题、富文本和现代阅读层更有辨识度；参考站的信息发现路径更多，但三栏布局更拥挤、字号更小、可访问性更弱。

媒体对比：参考站首页图片多但没有原生 lazy、图片尺寸属性和 alt；当前博客图片有 alt 和 lazy，已有灯箱下载，但此前封面比例与素材复用仍需优化。

无障碍对比：当前博客有 zh-CN、skip link、语义 header/nav/main/aside/footer、减少动画；仍需补 dialog role、焦点圈定、live region、aria-label 和 44px 触控目标。参考站存在大量无名链接/按钮并限制移动缩放。

性能/工程对比：参考站使用 Cloudflare、版本化资源和多页内容结构，但资源较多、完整 load 约 6.5 秒；当前博客轻量但此前为单 HTML、全量 select、无构建/CI/robots/sitemap/RSS。当前轮已补多 HTML、共享 CSS/JS、robots、sitemap 和 feed 占位。

来源：2026-09-24/25 浏览器实际访问与八维度对比工作流结果。
