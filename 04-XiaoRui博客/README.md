# xiaorui.cc爬虫说明

---

**第三方模块**：Scrapy<br>

**代码说明**:

- 目标：爬取技术博客网站帖子内容
- 功能：
	- 获取网站导航链接
	- 获取每页文章链接
	- 存储数据
- 已知反爬手段及应对策略
	- 导航栏会有无用的链接
		- 处理方法：针对性的在队列中进行删除
	- 每篇文章中都有一个本页跳转的链接
	    - 处理方法：获取每链接，需要特殊处理


**注意点**：

- 本爬虫不能保证所有博客都可以兼容，只是提供一个思想和思路，其他网站请自行分析。
- 如需保存到数据库，请使用pymongo进行保存。
