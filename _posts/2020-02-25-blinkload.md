---
title: "ShawdowsocksR & V2Ray 服务"
date: "2020-02-25"
---

昨天我购买了半年的Blinkload的BGP中转和IPLC专线服务。  
5人一起买8折优惠加上手续费和3天试用共花费300HKD

每个月有300G流量  
直连0.5x  
BGP中转1x  
IPLC专线3x

如果用于看新闻，每天最多会使用2G  
如果用于下载Youtube视频，使用直连节点，一次不会超过50G（实际使用100G流量）

[官网地址（可跳转）](https://blinkload.to/aff/sRRI)

* * *

节点分为：

直连 - **Standard** - 美国x5/台湾x4/日本x2/香港x8

BGP中转 - **Premium** - 美国x5/英国x2/新加坡x2/日本x6/香港x7

IPLC专线 - **Pro** - 香港x5

写着 **Media** 的线路可以看 **Netflix**

* * *

技术分为：

SS/**SSR** x45条线路

**V2Ray** x45条线路

不同的客户端支持的技术略有不同

V2Ray 更加稳定

* * *

- iOS

到 app Store 购买 **Quantumult** 4.99$ \*支持v2ray

其他软件暂时不推荐

- Andriod

到 Google Store 下载 **Surfboard** \*支持ssr 目前免费

- Windows

**Clash**

- MacOS

**V2RayX**

* * *

下面介绍 **Quantumult** 的使用方式

到官网复制订阅地址

Settings - Favorites - 加号 - Server - 填写Name 并 粘贴订阅地址到URL 勾选 Update Detection 自动更新订阅 - Save - Home

Quantumult界面的LOGO - 仪表盘测速 - 选择一个延迟较低的节点 - 右上角打开开关

#### 进阶

- Filter

可使用**过滤**功能 浏览本地网站时不使用代理流量 浏览境外网站时使用代理流量

你正在使用代理看 YouTube 上的视频
但是你突然想起了有个 B 站的视频还没看
可是现在还连着代理懒得关闭
那么就有了过滤功能 识别出B站可以不用代理浏览
这时候即使你正在使用代理 也不会用代理流量服务看 B 站视频
实际上 YouTube 走的是代理服务
B 站走的是你的本地网络运营商的服务

Settings - Favorites - 加号 - Filter

Settings - Favorites - 加号 - Rejection

- Policy

可使用**策略**功能 浏览特定的网站 让软件自动转换为特定的线路

你正在学习日语
看Netflix的电影时 想看到日本语字幕 
那么就需要在这个时候使用日本的线路 
用到了策略的功能

Settings - Policy - 加号

SSID 设置使用蜂窝网络数据和wifi时是否使用代理
Latency 先测试延迟再自动选择速度最快的节点
Static 在主界面手动选择自己相连接的节点
Balance 未知

* * *

下面介绍 **Surfboard** 的使用方式

到官网复制订阅地址

**Profile** - 加号 - Download from url - Download

**Config** - Proxy - Test Latency - 选择一个延迟较低的节点

**Switch** - 点击开关 - Connected!

* * *

以上就是我目前使用的方式和了解的操作方式
