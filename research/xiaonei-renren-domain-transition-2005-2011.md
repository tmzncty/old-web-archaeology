# 校内网 → 人人网：域名迁移证据（2005—2011）

> 状态：bounded research note；不是 M1 complete case。

本轮聚焦 `xiaonei.com` 到 `renren.com` 的品牌与域名迁移，不写“人人网兴衰史”。2011 年 Renren Inc. 向 SEC 提交的 F-1 记录：公司 SNS 前身为 `www.xiaonei.com`，并在 2009 年 8 月更名为 `www.renren.com`；同一文件的知识产权部分同时列出 `renren.com` 与 `xiaonei.com` 为公司注册域名。由此至少可以确认：品牌更名不等于旧域名立即从资产层消失。

2009-08-04 新浪科技报道，千橡宣布校内网更名人人网并启用 `renren.com`，同时称原 `xiaonei.com` 将继续作为跳转网址。2009-08-24《互联网周刊》又把“域名相应更换”具体写在 8 月 14 日凌晨。因此更稳妥的写法是把“更名公告”和“canonical domain cutover”分开，而不是压成一个瞬间。没有直接 HTTP/DNS capture 前，跳转状态码、path/query 是否保留仍然未知。

2007 年同期报道还显示，校内网扩展到高中和白领市场时采用过分区身份规则：例如公司用户需使用相应邮箱后缀注册，而且不同新区不能跨区登录。这说明“实名 SNS”与“所有用户都经过法律身份核验”不是一回事，平台账号存在也不等于拥有所有分区的访问资格。

## 证据等级

- A：Renren Inc. Form F-1（2011-04-15），用于 2011 公司资产状态及正式公司披露。
- B：2006—2009 同期媒体，用于收购、分区规则、更名与域名切换过程。
- C：后来把 2009 更名解释为“衰落转折点”的文章，只作为后见叙事，不作因果证据。
- D：本文提出的 brand / domain / redirect / account / content 分层模型。

## 不能声称已经证明

- 2009-08-04 当天两个域名的实际 DNS/HTTP 状态；
- 旧域名使用何种重定向；
- 深层 URL 是否逐一保留；
- 历史页面 charset、DOM、JS 与浏览器依赖；
- “无缝迁移”是否对所有内容对象成立。

## 下一步

直接核验 2009-08-01..20 的 `xiaonei.com`、`www.xiaonei.com`、`renren.com`、`www.renren.com` capture，记录时间、HTTP/replay 状态、Location、charset 与子资源。优先使用登录/帮助/about 等公开页面，避免普通个人资料页。

## Sources

- SEC F-1: https://www.sec.gov/Archives/edgar/data/1509223/000119312511099693/df1.htm
- 2009-08-04: https://tech.sina.com.cn/i/2009-08-04/14523321884.shtml
- 2009-08-24: https://tech.sina.com.cn/i/2009-08-24/15153378768.shtml
- 2007-11-21: https://tech.sina.com.cn/i/2007-11-21/08491864406.shtml
