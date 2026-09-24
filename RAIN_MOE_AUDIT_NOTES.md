# rain.moe 对比证据

参考站：

- https://rain.moe/
- https://rain.moe/211/
- https://rain.moe/timeline/
- https://rain.moe/fantasy/
- https://rain.moe/wife/
- https://rain.moe/friend/

## 已核验优势

rain.moe 的首页公开显示“内容数 88 篇”“评论数 87 条”，文章卡包含日期、热度、字数、阅读时间和摘要。一级导航有首页、云盘、追番、动漫、狂想、时光、友人、关于和搜索。视觉层有全屏动漫背景、头像、随机换背景、浅深色切换、DIY 背景和字体切换。

文章页抽样显示阅读量、字数、预计阅读时间、发布日期、最后更新时间、作者信息、许可协议、上一篇文章和带回复关系的评论。友人页提供友链申请信息、RSS/图标/描述等站外发现路径。时光页按年份、月份和分类组织内容。

## 当前博客的关键弱势

第一次浏览当前站首页时，发现 index.html 在 load() 之前执行 `$('#guestOpen').onclick`，但页面中没有 `guestOpen` 元素，导致初始化被空引用中断，页面永久停留在 Supabase 读取占位。本轮已改为可选事件绑定，随后浏览器验证显示 9 张文章卡、Supabase connected 和真实精选文章。

其他已核验差距：独立文章页此前没有评论区；文章没有上下篇、相关阅读、作者卡、许可和更新说明；站内 feed.xml 没有 item；sitemap 没有逐文章 URL；品牌署名在 reincarnation.log 与 reincarnation2 之间不统一；没有关于页和友链页；评论默认直接写入 approved。

## 本轮行动

已修复首页初始化空引用，统一首页和内页文章导航，新增 About / Friends 页面，给首页补 RSS alternate 和菜单 aria-expanded/aria-controls，给独立文章页接入评论计数、评论列表、回应表单、上下篇和继续读模块，并从 Supabase 生成包含 9 个文章条目的 feed.xml 和逐文章 sitemap.xml。

来源：2026-09-25 浏览器实际访问、当前仓库源代码检查和 Supabase 只读数据核验。
