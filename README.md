# [am-cf-auto-trojan](https://github.com/amclubs/am-cf-auto-trojan)
这是基于CF平台的脚本，部署Trojan配置信息转换为订阅内容。可以快速生成优先节点信息。

#
▶️ **新人[YouTube](https://youtube.com/@am_clubs?sub_confirmation=1)** 需要您的支持，请务必帮我**点赞**、**关注**、**打开小铃铛**，***十分感谢！！！*** ✅
</br>🎁请 **follow** 我的[GitHub](https://github.com/amclubs)、给我所有项目一个 **Star** 星星（拜托了）！你的支持是我不断前进的动力！ 💖
</br>✅**解锁更多技能** [加入TG群【am_clubs】](https://t.me/am_clubs)、[YouTube频道【@am_clubs】](https://youtube.com/@am_clubs?sub_confirmation=1)、[【博客(国内)】](https://amclubss.com)、[【博客(国际)】](https://amclubs.blogspot.com) 
</br>✅点击观看教程[CLoudflare免费节点](https://www.youtube.com/playlist?list=PLGVQi7TjHKXbrY0Pk8gm3T7m8MZ-InquF) | [VPS搭建节点](https://www.youtube.com/playlist?list=PLGVQi7TjHKXaVlrHP9Du61CaEThYCQaiY) | [获取免费域名](https://www.youtube.com/playlist?list=PLGVQi7TjHKXZGODTvB8DEervrmHANQ1AR) | [免费VPN](https://www.youtube.com/playlist?list=PLGVQi7TjHKXY7V2JF-ShRSVwGANlZULdk) | [IPTV源](https://www.youtube.com/playlist?list=PLGVQi7TjHKXbkozDYVsDRJhbnNaEOC76w) | [Mac和Win工具](https://www.youtube.com/playlist?list=PLGVQi7TjHKXYBWu65yP8E08HxAu9LbCWm) | [AI分享](https://www.youtube.com/playlist?list=PLGVQi7TjHKXaodkM-mS-2Nwggwc5wRjqY)

## Workers 部署方法 
1. 部署 Cloudflare Worker：
   - 在 Cloudflare Worker 控制台中创建一个新的 Worker。
   - 将 [_worker.js](https://github.com/amclubs/am-cf-auto-trojan/blob/main/_worker.js) 的内容粘贴到 Worker 编辑器中。
2. 访问订阅内容：
   - 访问 `https://[YOUR-WORKERS-URL]/[UUID]` 即可获取订阅内容。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` 就是你的通用自适应订阅地址(Quantumult X、Clash、singbox、小火箭、v2rayN、v2rayU、surge、PassWall、SSR+、Karing等)。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?base64` Base64订阅格式，适用PassWall,SSR+等。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash订阅格式，适用OpenClash等。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?singbox` singbox订阅格式，适用singbox等。

3. 给 workers绑定 自定义域： 
   - 在 workers控制台的 `触发器`选项卡，下方点击 `添加自定义域`。
   - 填入你已转入 CloudFlare 域名解析服务的次级域名，例如:`vless.google.com`后 点击`添加自定义域`，等待证书生效即可。

</details>

## Pages 上传 部署方法 **最佳推荐!!!** 
1. 部署 Cloudflare Pages：
   - 下载 [_worker.js.zip](https://raw.githubusercontent.com/amclubs/am-cf-auto-trojan/main/_worker.js.zip) 文件，并点上 Star !!!
   - 在 Cloudflare Pages 控制台中选择 `上传资产`后，为你的项目取名后点击 `创建项目`，然后上传你下载好的 [_worker.js.zip](https://raw.githubusercontent.com/amclubs/am-cf-auto-trojan/main/_worker.js.zip) 文件后点击 `部署站点`。
   - 部署完成后点击 `继续处理站点` 后，选择 `设置` > `环境变量` > **制作**为生产环境定义变量 > `添加变量`。
     变量名称填写**UUID**，值则为你的UUID，后点击 `保存`即可。
   - 返回 `部署` 选项卡，在右下角点击 `创建新部署` 后，重新上传 [_worker.js.zip](https://raw.githubusercontent.com/amclubs/am-cf-auto-trojan/main/_worker.js.zip) 文件后点击 `保存并部署` 即可。
2. 访问订阅内容：
   - 访问 `https://[YOUR-WORKERS-URL]/[UUID]` 即可获取订阅内容。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` 就是你的通用自适应订阅地址(Quantumult X、Clash、singbox、小火箭、v2rayN、v2rayU、surge、PassWall、SSR+、Karing等)。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?base64` Base64订阅格式，适用PassWall,SSR+等。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash订阅格式，适用OpenClash等。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?singbox` singbox订阅格式，适用singbox等。

3. 给 Pages绑定 CNAME自定义域：
   - 在 Pages控制台的 `自定义域`选项卡，下方点击 `设置自定义域`。
   - 填入你的自定义次级域名，注意不要使用你的根域名，例如：
     您分配到的域名是 `google.com`，则添加自定义域填入 `vless.google.com`即可；
   - 按照 Cloudflare 的要求将返回你的域名DNS服务商，添加 该自定义域 `vless`的 CNAME记录 `vless.google.pages.dev` 后，点击 `激活域`即可。

</details>

## Pages GitHub 部署方法 
1. 部署 Cloudflare Pages：
   - 在 Github 上先 Fork 本项目，并点上 Star !!!
   - 在 Cloudflare Pages 控制台中选择 `连接到 Git`后，选中 `am-cf-auto-trojan`项目后点击 `开始设置`。
   - 在 `设置构建和部署`页面下方，选择 `环境变量（高级）`后并 `添加变量`
     变量名称填写**UUID**，值则为你的UUID，后点击 `保存并部署`即可。

2. 访问订阅内容：
   - 访问 `https://[YOUR-WORKERS-URL]/[UUID]` 即可获取订阅内容。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` 就是你的通用自适应订阅地址(Quantumult X、Clash、singbox、小火箭、v2rayN、v2rayU、surge、PassWall、SSR+、Karing等)。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?base64` Base64订阅格式，适用PassWall,SSR+等。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash订阅格式，适用OpenClash等。
   - 例如 `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?singbox` singbox订阅格式，适用singbox等。

3. 给 Pages绑定 CNAME自定义域：
   - 在 Pages控制台的 `自定义域`选项卡，下方点击 `设置自定义域`。
   - 填入你的自定义次级域名，注意不要使用你的根域名，例如：
     您分配到的域名是 `google.com`，则添加自定义域填入 `vless.google.com`即可；
   - 按照 Cloudflare 的要求将返回你的域名DNS服务商，添加 该自定义域 `vless`的 CNAME记录 `vless.google.pages.dev` 后，点击 `激活域`即可。


</details>


## 变量说明
| 变量名 | 示例 | 必填 | 备注 | YT |
|-----|-----|-----|-----|-----|
| TOKEN             | auto                                 |✅| 快速订阅内置节点的订阅路径地址 /auto (支持多元素, 元素之间使用,作间隔)  |  |
| HOST              | page-us-17m.pages.dev                |❌| 快速订阅内置节点的伪装域名             |  |
| PASSWORD          | amclubs                              |❌| 快速订阅内置节点的密码           |  |
| DNS_RESOLVER_URL | https://cloudflare-dns.com/dns-query |❌| DNS解析获取作用，小白勿用                                                           |  |
| IP_LOCAL         | `icook.hk:2053#官方优选域名`           |❌| 本地优选域名/优选IP(支持多元素之间`,`或 换行 作间隔)                                 | |
| IP_URL_TXT       | [https://raw.github.../ipv4.txt](https://raw.githubusercontent.com/amclubs/am-cf-auto-trojan/main/ipv4.txt) |❌| 优选ipv4、ipv6、域名、API地址(支持多个之间`,`或 换行 作间隔) |[Video](https://youtu.be/dzxezRV1v-o) |
| IP_URL_CSV       | [https://raw.github.../ipv4.csv](https://raw.githubusercontent.com/amclubs/am-cf-auto-trojan/main/ipv4.csv) |❌| 优选ipv4/6的IP测速结果(支持多元素, 元素之间使用`,`作间隔) |[Video](https://youtu.be/vX3U3FuuTT8)|
| NO_TLS           | true/false                           |❌| 默认false,是否开启TLS系列端口，只有workers部署才可以使非用TLS系列端口             | |
| SL               | 5                                    |❌| `CSV`文件里的测速结果满足速度下限                                                     ||
| SUB_CONFIG       | [https://raw.github.../ACL4SSR_Online_Mini.ini](https://raw.githubusercontent.com/amclubs/ACL4SSR/main/Clash/config/ACL4SSR_Online_Full_MultiMode.ini) |❌| clash、singbox等 订阅转换配置文件  ||
| SUB_CONVERTER    | https://url.v1.mk                    |❌| clash、singbox等 订阅转换后端的api地址                               ||
| SUB_NAME         | @AM_CLUB                             |❌ | 订阅名称                                                     ||
| TG_TOKEN        | 68941456:XXXXXXX0qExVUDAXXXqWXgBA     |❌| 发送TG通知的机器人token                       ||
| TG_ID           | 6946912345                            |❌ | 接收TG通知的账户数字ID                                       ||


# 
<center>
<details><summary><strong> [点击展开] 赞赏支持 ~🧧</strong></summary>
*我非常感谢您的赞赏和支持，它们将极大地激励我继续创新，持续产生有价值的工作。*

- **USDT-TRC20:** `TWTxUyay6QJN3K4fs4kvJTT8Zfa2mWTwDD`
- **TRX-TRC20:** `TWTxUyay6QJN3K4fs4kvJTT8Zfa2mWTwDD`

<div align="center"> 
  <img src="https://github.com/user-attachments/assets/e6cdc42a-6374-4722-b833-601738f72196" width="200"></br> 
  TRC10/TRC20扫码支付 
</div> 
</details>
</center>

 #
 免责声明:
 - 1、该项目设计和开发仅供学习、研究和安全测试目的。请于下载后 24 小时内删除, 不得用作任何商业用途, 文字、数据及图片均有所属版权, 如转载须注明来源。
 - 2、使用本程序必循遵守部署服务器所在地区的法律、所在国家和用户所在国家的法律法规。对任何人或团体使用该项目时产生的任何后果由使用者承担。
 - 3、作者不对使用该项目可能引起的任何直接或间接损害负责。作者保留随时更新免责声明的权利，且不另行通知。
 
