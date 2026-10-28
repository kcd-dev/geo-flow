# geo-flow

本地检出来自 `git@github.com:kcd-dev/geo-flow.git`，`origin` 已移除。仓库许可证是 Apache-2.0，见 [LICENSE](LICENSE)。

这次提交只增加本说明。GEOInflow 的程序源码在另一个仓库：<https://github.com/yaojingang/GEOInflow>。

下面保留姚金刚（[@yaojingang](https://x.com/yaojingang)）2026-10-26 公开发布的开源说明，以及该线程里有信息量的评论。

## GEOInflow

一套面向 GEO 的网站与 AI 爬虫分析系统，同时支持完整的访客数据、转化数据统计与分析。MIT 协议，Docker 一键部署。

GEOInflow 将网站访客、AI 搜索引荐、服务器抓取日志和内容目录放在同一个网站上下文中，用来回答：

- 哪些 AI 蜘蛛访问了网站，访问了哪些内容
- 哪些关键页面长期缺少抓取记录
- 访问是否遇到错误
- AI 搜索实际带来了多少访客和转化

### 核心逻辑与能力

1. 哪些 AI 平台在抓站：OpenAI、Anthropic、Perplexity、Google、字节、百度、Kimi、腾讯混元等。区分训练、AI 搜索，以及用户触发的访问。包括抓了哪些页面，哪些关键页从没被抓过。
2. 追踪 AI 搜索引荐来的会话、落地页和转化，看清 GEO 的真实效果。
3. 完整的网站统计：PV/UV、事件漏斗、热力图、留存、团队权限与分享。
4. 核心统计无需模型 API Key，默认无 Cookie 采集，数据留在自己的服务器上。
5. 已整理 61 种全球 AI 爬虫身份及分类，并在此基础上构建数据分析看板。

做 GEO，每一次内容调整都值得有数据可以复盘。欢迎体验和提 PR。

- 代码：<https://github.com/yaojingang/GEOInflow>
- 介绍视频：<https://github.com/user-attachments/assets/81e57cc4-3441-4e5f-b2fb-cd929c6c27bd>

介绍视频地址来自 GEOInflow 仓库 README 里已经公开的附件。原帖写明这条视频由 Claude 制作，用来了解项目。

### 作者补充

- GEOInflow 基于 Umami 开发，同样采用 MIT 开源，感谢 Umami 项目的开源贡献者。
- 联合发布：猎看科技、北京日报社智源GEO。
- 项目发起人：姚金刚、向阳乔木、任强。
- 欢迎提交 PR，一起持续完善。

## 保留的评论

### 同一家爬虫的训练访问和搜索访问

ReignSwords（[@ReignSwords](https://x.com/ReignSwords)，10月26日）问：61 种爬虫的整理很实用。之前只知道 GPTBot 和 ClaudeBot，分不清哪些是来训练、哪些是来检索的。它能区分同一家爬虫的训练访问和搜索访问吗？

姚金刚回复：能。目前按各大 AI 平台官网文档整理和区分。有些爬虫官网没有公布，需要自己做过滤机制，这需要时间。

### 数据是否来自 Web 服务器日志

Tony Woo（[@tonywoo](https://x.com/tonywoo)，10月26日）问：数据是来自 web server log 吗？

姚金刚回复：是的。

开源说明里同时写了访客数据、转化数据和服务器抓取日志。这条回复按原话保留。

### 新加坡方向的伪装爬虫如何屏蔽

伯恩控熵（[@rfboen](https://x.com/rfboen)）问：网站有大量来自新加坡的伪装爬虫吗？如何屏蔽？

姚金刚回复：接下来打算给这个系统增加一键屏蔽垃圾蜘蛛的功能。

这条回复记录的是后续计划。

### GEOFlow 与 GEOInflow 名称太接近

Jason Yin - Campus VC（[@jasonyin](https://x.com/jasonyin)，10月27日）说：GEOFlow 和 GEOInflow 这两个名字太相似，外行分不清，建议至少把其中一个改名，加大区分度。

姚金刚回复：好的，是有点。

本目录名是 `geo-flow`，帖子里的产品名是 GEOInflow。这条改名建议记在这里，目录名和产品名保持原文。
