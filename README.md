# QuantumultX 懒人配置DIY版 【作者】w37fhy 【电报频道】https://t.me/w37fhy【更新日期】2023/6/2
# 【YouTube视频教程】 QuantumultX 系列教程：https://fhyurl.tk/quantumultx
# 更新日志：
# 1. 增加OpenAI分流和策略组
# 2. 增加Netflix分流和策略组


[general]
dns_exclusion_list=*.cmpassport.com, *.jegotrip.com.cn, *.icitymobile.mobi, id6.me, *.pingan.com.cn
geo_location_checker=http://ip-api.com/json/?lang=zh-CN, https://raw.githubusercontent.com/Orz-3/Orz-3/master/QuantumultX/IP.js
resource_parser_url= https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/resource-parser.js
profile_img_url= https://raw.githubusercontent.com/Orz-3/mini/master/Color/Personal.png
server_check_url=http://www.gstatic.com/generate_204
#第一个filter为4g模式开启规则分流，第二个filter为其他wifi下开启规则分流，第三个wifi1修改成你路由器翻墙的wifi名开启直连模式，第四个wifi2为你公司或者其他有路由器翻墙的WiFi名走直连）
#默认关闭根据wifi切换模式，如需开启，删除下方的“#”即可！
#running_mode_trigger=filter, filter, wifi1:all_direct, wifi2: all_direct

[dns]
no-ipv6
server=119.29.29.29
server=114.114.114.114


[policy]
static=节点选择, 自动选择, 香港, 台湾, 日本, 韩国, 新加坡, 美国, 荷兰, proxy, direct, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Static.png
url-latency-benchmark=自动选择, server-tag-regex=.*, check-interval=600, tolerance=80, alive-checking=false, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Urltest.png
url-latency-benchmark=香港, server-tag-regex=(?=.*(港|HK|(?i)Hong))^((?!(台湾|日本|新加坡|美国|韩国|狮城|南朝鲜|US|SG|JP|KR|TW|台灣|美國|韓國|獅城)).)*$, check-interval=600, tolerance=80, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/HK.png
# 默认设置10分钟测速一次，当前使用节点延迟和最新测速延迟最低的节点相差80ms以上则切换为最新的最低延迟节点，否则继续延用节点
url-latency-benchmark=台湾, server-tag-regex=(?=.*(台|TW|(?i)Taiwan))^((?!(港|日|韩|新|美)).)*$, check-interval=600, tolerance=80, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/TW.png
url-latency-benchmark=日本, server-tag-regex=(?=.*(日本|JP|(?i)Japan))^((?!(香港|台湾|新加坡|美国|韩国|狮城|南朝鲜|US|SG|KR|HK|TW|台灣|美國|韓國|獅城)).)*$, check-interval=600, tolerance=100, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/JP.png
url-latency-benchmark=韩国, server-tag-regex=(?=.*(KR|Korea|KOR|首尔|韩|韓|(?i)Korea))^((?!(香港|台湾|新加坡|美国|狮城|南朝鲜|US|SG|HK|TW|台灣|美國|獅城)).)*$, check-interval=600, tolerance=100, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/KR.png
url-latency-benchmark=新加坡, server-tag-regex=(?=.*(新加坡|狮城|SG|(?i)Singapore))^((?!(香港|台湾|日本|美国|韩国|南朝鲜|US|JP|KR|HK|TW|台灣|美國|韓國)).)*$, check-interval=600, tolerance=100, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/SG.png
url-latency-benchmark=美国, server-tag-regex=(?=.*(美国|美國|US|洛杉矶|西雅图|(?i)States|American))^((?!(香港|台湾|日本|新加坡|韩国|狮城|南朝鲜|SG|JP|KR|HK|TW|台灣|韓國|獅城|直连)).)*$, check-interval=600, tolerance=100, alive-checking=false, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/US.png
url-latency-benchmark=荷兰, server-tag-regex=荷兰, check-interval=600, tolerance=0, alive-checking=false, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/XD.png
static=Apple, direct, 香港, 台湾, 日本, 韩国, 新加坡, 美国, 节点选择, img-url=https://raw.githubusercontent.com/erdongchanyo/icon/main/Policy-Filter/Apple.png
static=TikTok, DIRECT, 香港, 台湾, 日本, 韩国, 新加坡, 美国, 节点选择, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/TikTok.png
static=OpenAI, direct, 香港, 台湾, 日本, 韩国, 新加坡, 美国, 节点选择, 荷兰, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Bot.png
static=Netfilx, server-tag-regex=(日本B|新加坡A I|巴西|奈|Netflix), img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Netflix.png
static=漏网之鱼, 节点选择, 自动选择, 香港, 台湾, 日本, 韩国, 新加坡, 美国, PROXY, DIRECT, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Final.png

[server_remote]
https://byg.zzxuh.com/api/v1/client/subscribe?token=ccb86f6780c797df319d9f4160262040&flag=quantumult%20x, tag=byg, update-interval=172800, opt-parser=true, enabled=true
https://sub.api.ovodisk.com/api/v1/client/subscribe?token=9332d56e075ab1144602e1255faf7ef3, tag=Tag-1696587841, update-interval=172800, opt-parser=true, enabled=true

[filter_remote]
https://raw.githubusercontent.com/RuCu6/QuanX/main/Rules/MyBlockAds.list, tag=MyBlockAds, force-policy=reject, update-interval=172800, opt-parser=false, inserted-resource=true, enabled=true
# OpenAI分流
https://raw.githubusercontent.com/w37fhy/QuantumultX/master/Rules/Advertising.list, tag=🛑轻量广告拦截-拒绝, force-policy=reject, update-interval=172800, opt-parser=true, enabled=true
https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/AdRule.list, tag=🛑重度广告拦截-拒绝, force-policy=reject, update-interval=172800, opt-parser=true, enabled=true
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/OpenAI/OpenAI.list, tag=🤖OpenAI, force-policy=OpenAI, update-interval=172800, opt-parser=true, enabled=true
# TikTok分流
https://raw.githubusercontent.com/Semporia/TikTok-Unlock/master/Quantumult-X/TikTok.list, tag=🎯TikTok分流, force-policy=TikTok, update-interval=172800, opt-parser=false, enabled=true
# Apple规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Apple/Apple.list, tag=Apple 规则, force-policy=Apple, update-interval=86400, opt-parser=true, enabled=true
# Unbreak 后续规则修正
https://raw.githubusercontent.com/w37fhy/QuantumultX/master/Rules/Unbreak.list, tag=🎯规则修正-直连, force-policy=direct, update-interval=172800, opt-parser=true, enabled=true
# Advertising 广告
# NobyDa大佬去广告 -默认关闭，自行手动启用！
# Privacy 隐私
https://raw.githubusercontent.com/w37fhy/QuantumultX/master/Rules/Tracking.list, tag=🛑隐私保护-拒绝, force-policy=reject, update-interval=172800, opt-parser=true, enabled=true
# Hijacking 运营商劫持或恶意网站
https://raw.githubusercontent.com/w37fhy/QuantumultX/master/Rules/Hijacking.list, tag=🛑运营商劫持-拒绝, force-policy=reject, update-interval=172800, opt-parser=true, enabled=true
# Netfilx分流
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Netflix/Netflix.list, tag=🎬Netflix, force-policy=Netfilx, update-interval=172800, opt-parser=false , enabled=true
# Streaming 国际流媒体服务
https://raw.githubusercontent.com/w37fhy/QuantumultX/master/Rules/Streaming.list, tag=🎯国际流媒体, force-policy=节点选择, update-interval=172800, opt-parser=true , enabled=true
# Global 全球加速
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Global/Global.list, tag=🎯全球加速, force-policy=节点选择, update-interval=172800, opt-parser=false , enabled=true
# China 国内网站
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/China/China.list, tag=🎯国内网站-直连, force-policy=direct, update-interval=172800, opt-parser=false, enabled=true
# ChinaIP 中国直连
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/ChinaIPs/ChinaIPs.list, tag=🎯中国IP-直连, force-policy=direct, update-interval=172800, opt-parser=false , enabled=true

[rewrite_remote]
https://github.com/VirgilClyne/iRingo/raw/main/snippet/Location.snippet, tag= iRingo: Location & Map, update-interval=172800, opt-parser=true, enabled=true
https://github.com/VirgilClyne/iRingo/raw/main/snippet/Siri.snippet, tag= iRingo: Siri & Search, update-interval=172800, opt-parser=true, enabled=true
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/script/smzdm/smzdm_remove_ads.qxrewrite, tag=什么值得买去广告, update-interval=172800, opt-parser=true, enabled=true
https://raw.githubusercontent.com/ddgksf2013/Rewrite/master/AdBlock/Applet.conf, tag=wx小程序去广告, update-interval=172800, opt-parser=true, enabled=true
https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/Js.conf, tag=去广告野比, update-interval=172800, opt-parser=true, enabled=true
https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/Cube/xiaohongshu.snippet, tag=xiaohongshu, update-interval=172800, opt-parser=true, inserted-resource=true, enabled=true
https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/Cube/cloudmusic.snippet, tag=cloudmusic, update-interval=172800, opt-parser=true, inserted-resource=true, enabled=true
https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/Cube/bilibili.snippet, tag=bilibili, update-interval=172800, opt-parser=true, inserted-resource=true, enabled=true
https://raw.githubusercontent.com/Orz-3/QuantumultX/master/YouTube.conf, tag=YouTube去广告, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/Cube/youtube.snippet, tag=youtube, update-interval=172800, opt-parser=true, inserted-resource=true, enabled=true
https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/Cube/amap.snippet, tag=amap, update-interval=172800, opt-parser=true, inserted-resource=true, enabled=true
https://raw.githubusercontent.com/w37fhy/QuantumultX/master/QuantumultX_JS.conf, tag=比价等脚本, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/Semporia/TikTok-Unlock/master/Quantumult-X/TikTok-TW.conf, tag=解锁TikTok台湾区, update-interval=86400, opt-parser=false, enabled=false
https://raw.githubusercontent.com/Semporia/TikTok-Unlock/master/Quantumult-X/TikTok-JP.conf, tag=解锁TikTok日本区, update-interval=86400, opt-parser=false, enabled=false
https://raw.githubusercontent.com/Semporia/TikTok-Unlock/master/Quantumult-X/TikTok-KR.conf, tag=解锁TikTok韩国区, update-interval=86400, opt-parser=true, inserted-resource=true, enabled=true
https://raw.githubusercontent.com/Semporia/TikTok-Unlock/master/Quantumult-X/TikTok-US.conf, tag=解锁TikTok美国区, update-interval=86400, opt-parser=false, enabled=false
https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.quanx.tf.conf, tag=Boxjs, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/TestFlightDownload.conf, tag=TestFlight区域限制解除, update-interval=172800, opt-parser=true, enabled=true
https://raw.githubusercontent.com/w37fhy/QuantumultX/master/QuantumultX_Cookie.conf, tag=获取Cookie, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/qiangxinglin/Emby/main/QuantumultX/emby.conf, tag=Emby Premiere, update-interval=86400, opt-parser=true, enabled=true
[server_local]
vless=104.24.59.80:443, method=none, password=294da701-40df-4381-ba74-cfd8cd1a4bd3, obfs=wss, obfs-host=kk.qzinori.link, obfs-uri=/?ed=2048, tls-verification=false, fast-open=false, udp-relay=false, tag=kk.qzinori.link
[filter_local]
host-suffix, sentry.io, reject
host-keyword, exitgames.com, 节点选择
host-suffix, bnbstatic.com, 节点选择
host-suffix, local, direct
ip-cidr, 192.168.0.0/16, direct
ip-cidr, 10.0.0.0/8, direct
ip-cidr, 172.16.0.0/12, direct
ip-cidr, 127.0.0.0/8, direct
ip-cidr, 100.64.0.0/10, direct
ip-cidr, 224.0.0.0/4, direct
ip6-cidr, fe80::/10, direct
# GEOIP,CN,DIRECT
FINAL,漏网之鱼

[rewrite_local]
^https?:\/\/api\.m\.jd\.com\/client\.action\?functionId=(queryTemplates|serverConfig)$ - script-request-header https://raw.githubusercontent.com/chiupam/surge/main/scripts/javascripts/wskey.js

[task_local]
0 2 */12 * * * https://raw.githubusercontent.com/NobyDa/Script/master/JD-DailyBonus/JD_DailyBonus.js, tag=京东, img-url=https://raw.githubusercontent.com/Orz-3/task/master/jd.png, enabled=true
0 8 * * * https://raw.githubusercontent.com/Peng-YM/QuanX/master/Tasks/exchange.js, tag=汇率监控, img-url=https://raw.githubusercontent.com/Orz-3/task/master/exchangerate.png, enabled=true

[mitm]
hostname = 
passphrase = 
