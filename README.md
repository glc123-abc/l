[general]

excluded_routes=192.168.0.0/16, 10.0.0.0/8, 172.16.0.0/12, 100.64.0.0/10, 17.0.0.0/8

network_check_url=http://cp.cloudflare.com/generate_204

server_check_url=http://www.qualcomm.cn/generate_204

geo_location_checker=http://ip-api.com/json/?lang=zh-CN, https://github.com/KOP-XIAO/QuantumultX/raw/master/Scripts/IP_API.js

resource_parser_url=https://raw.githubusercontent.com/zwf234/Scriptable/master/resource-parser.js

profile_img_url= https://gitee.com/glc66/vess/raw/master/tp/An.JPEG

dns_exclusion_list = *.cmpassport.com, *.jegotrip.com.cn, *.icitymobile.mobi, id6.me, *.icitymobile.mobi, *.pingan.com.cn, *.cmbchina.com, *.localnetwork.uop, mfs.ykimg.com*.ttf

[dns]

no-ipv6

server=119.29.29.29

server=223.5.5.5

server=1.2.4.8

server=/*.taobao.com/223.5.5.5

server=/*.tmall.com/223.5.5.5

server=/*.alipay.com/223.5.5.5

server=/*.alicdn.com/223.5.5.5

server=/*.aliyun.com/223.5.5.5

server=/*.jd.com/119.28.28.28

server=/*.qq.com/119.28.28.28

server=/*.tencent.com/119.28.28.28

server=/*.weixin.com/119.28.28.28

server=/*.bilibili.com/119.29.29.29

server=/hdslb.com/119.29.29.29

server=/*.163.com/119.29.29.29

server=/*.126.com/119.29.29.29

server=/*.126.net/119.29.29.29

server=/*.127.net/119.29.29.29

server=/*.netease.com/119.29.29.29

server=/*.mi.com/119.29.29.29

server=/*.xiaomi.com/119.29.29.29

address=/mtalk.google.com/108.177.125.188

[http_backend] 

https://raw.githubusercontent.com/chavyleung/scripts/master/box/chavy.boxjs.js, tag=BoxJs, path=^/, img-url=https://qxnav.com/rules/QuantumultX/img/box.png, enabled=false

#BoxJs改为使用http backend方式，访问地址改为http://127.0.0.1:9999，更新配置后请长按风车-更新，然后重启代理

[policy]

static=海外服务, 优选节点1, 优选节点2, 优选节点3,负载均衡,自选节点, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Global.png

#优选节点默认每一小时进行一次延迟检测，想更换检测时间的请修改check-interval参数。

url-latency-benchmark=优选节点1, resource-tag-regex=^(LULIN), server-tag-regex=^(?!.*网易云), check-interval=3600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Urltest.png

url-latency-benchmark=优选节点2, resource-tag-regex=^(LINLIN), server-tag-regex=^(?!.*网易云), check-interval=3600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Urltest.png

url-latency-benchmark=优选节点3, resource-tag-regex=^(五毛钱), server-tag-regex=^(?!.*网易云), check-interval=3600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Urltest.png

round-robin=负载均衡, resource-tag-regex=^(五毛钱), server-tag-regex=^(?!.*网易云), img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Roundrobin.png

static=自选节点, proxy, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Static.png

static=大陆服务, direct, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/China.png

static=网易云音乐, server-tag-regex=^(music|𝐌𝐮𝐬𝐢𝐜|Unbolck|网易|解锁), img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Netease.png

static=屏蔽广告, reject, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Adblock.png

static=AdBlock, direct, reject, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Final.png

static=Mainland, direct, img-url=https://raw.githubusercontent.com/Orz-3/face/master/Bili.png

static=Outside, direct, 海外服务, img-url=https://raw.githubusercontent.com/Orz-3/face/master/YouTube.png

static=港台番剧, 优选节点3, 自选节点, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/StreamingSE.png

#url-latency-benchmark=香港, server-tag-regex=(?=.*(港|HK|(?i)Hong))^((?!(台|日|韩|新|美)).)*$, check-interval=600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/HK.png

#url-latency-benchmark=台湾, server-tag-regex=(?=.*(台|TW|(?i)Taiwan))^((?!(港|日|韩|新|美)).)*$, check-interval=600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/TW.png

#url-latency-benchmark=日本, server-tag-regex=(?=.*(日|JP|(?i)Japan))^((?!(港|台|韩|新|美)).)*$, check-interval=600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/JP.png

#url-latency-benchmark=新加坡, server-tag-regex=(?=.*(新|狮|獅|SG|(?i)Singapore))^((?!(港|台|日|韩|美)).)*$, check-interval=600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/SG.png

#url-latency-benchmark=美国, server-tag-regex=(?=.*(美|US|(?i)States|American))^((?!(港|台|日|韩|新)).)*$, check-interval=600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/US.png

[server_local]

shadowsocks=154.17.2.109:18335, method=chacha20-ietf-poly1305, password=B7wYOKgFl0YDIF3aOeCRl93eaSSa2pnzqZASDuxy4CN35CZpXAyjT6DEc8x38R, fast-open=false, udp-relay=false, tag=CYL-科

# 本地服务器部分，自行添加即可

shadowsocks=music.desperadoj.com:30003, method=aes-128-gcm, password=desperadoj.com_free_proxy_d39m, fast-open=false, udp-relay=false, tag=网易云解锁灰色

#请使用 Safari 浏览器访问网站。首先下载 证书 (https://qxnav.com/rules/QuantumultX/CA/wyy_ca.crt)，进入「设置」>「通用」>「描述文件」，安装「UnblockNeteaseMusic Root CA」，并在「设置」>「通用」>「关于本机」>「证书信任设置」开启对「UnblockNeteaseMusic Root CA」的信任。

#证书下载地址：https://qxnav.com/rules/QuantumultX/CA/wyy_ca.crt

[server_remote]

https://ssrr.xyz/api/v1/client/subscribe?token=b23de6c959073db6a611c31d13b1d765, tag=LULIN, img-url=https://gitee.com/glc66/vess/raw/master/tp/luc.png, update-interval=43200, opt-parser=true, enabled=true

https://anmuheipp.netlify.app/, tag=LINLIN, img-url=https://gitee.com/glc66/vess/raw/master/tp/lin.png, update-interval=43200, opt-parser=true, enabled=true

https://xsus.xyz/api/v1/client/subscribe?token=124146b1d16099e66e2c16bb3a669ef3, tag=五毛钱, img-url=https://gitee.com/glc66/vess/raw/master/tp/lin.png, update-interval=43200, opt-parser=true, enabled=true

#解锁网易云灰色音乐原订阅地址：https://git.io/JfNq3

https://qxnav.com/rules/QuantumultX/gz/wyy.list, tag=网易云解锁灰色, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Netease_Music.png, update-interval=86400, opt-parser=true, enabled=true

# 节点远程订阅，自行添加

[filter_remote]

#规则分流修复

https://raw.githubusercontent.com/zqzess/rule_for_quantumultX/master/QuantumultX/rules/ReFix.list, tag=ReFix规则修正, update-interval=86400, opt-parser=false, enabled=true

#自定义

https://raw.githubusercontent.com/zqzess/rule_for_quantumultX/master/QuantumultX/rules/AdBlock.list, force-policy=AdBlock,tag=AdBlock , enabled=true

https://gitee.com/glc66/Quantumult-X/raw/master/quantumult%20X/haiwai.md, tag=海外服务, enabled=true

https://raw.githubusercontent.com/zwf234/rules/master/QuantumultX/shunt/dalu.list, tag=大陆服务, enabled=true

https://raw.githubusercontent.com/zwf234/rules/master/QuantumultX/shunt/Netease.list, tag=网易云音乐, enabled=true

https://raw.githubusercontent.com/zwf234/rules/master/shunt/gangtaifanju.list, tag=港台番剧, update-interval=86400, opt-parser=false, enabled=true

https://gitee.com/glc66/Quantumult-X/raw/master/qgg.md, tag=去广告, update-interval=86400, opt-parser=false, enabled=false

https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/AdvertisingLite/AdvertisingLite.list, tag=屏蔽广告, force-policy=屏蔽广告, update-interval=86400, opt-parser=false, enabled=false

[filter_local]

# 本地分流规则(相同规则下，本地规则将覆盖远程规则，优先生效)

# 绕过企业证书过期

host, ocsp.apple.com, reject

#YouTube 去底部广告

host-suffix, ehg-youtube.hitbox.com, reject

# 屏蔽系统更新

host, ns.itunes.apple.com,屏蔽广告

host, appldnld.apple.com,屏蔽广告

host, mesu.apple.com,屏蔽广告

host, xp.apple.com,屏蔽广告

host, gdmf.apple.com,屏蔽广告

# 避免迅雷版权问题

host, hub5idx.v6.shub.sandai.net,reject

host, hub5emu.v6.shub.sandai.net,reject

host, hub5btmain.v6.shub.sandai.net,reject

# 其他

host-suffix, local, direct

host-keyword, merlinblog, proxy

ip-cidr, 10.0.0.0/8, direct

ip-cidr, 17.0.0.0/8, direct

ip-cidr, 100.64.0.0/10, direct

ip-cidr, 127.0.0.0/8, direct

ip-cidr, 172.16.0.0/12, direct

ip-cidr, 192.168.0.0/16, direct

geoip, cn, 大陆服务

final, 大陆服务

[rewrite_remote]

# rewrite 复写远程订阅

https://gitee.com/glc66/Quantumult-X/raw/master/quantumult%20X/fuxie.md, tag=路林规则合集, update-interval=86400, opt-parser=false, enabled=true

https://raw.githubusercontent.com/ddgksf2013/Cuttlefish/master/Rewrite/UnlockVip/ParseVideo.conf, tag=爱优腾, update-interval=172800, opt-parser=false, enabled=true

https://raw.githubusercontent.com/zwf234/rules/master/QuantumultX/price.conf, tag=京东淘宝比价, update-interval=86400, opt-parser=false, enabled=true

https://raw.githubusercontent.com/Semporia/TikTok-Unlock/master/Quantumult%20X/TikTok-JP.conf, tag=解锁TikTok（更改后缀换区）, update-interval=86400, opt-parser=false, enabled=true

https://gitee.com/glc66/Quantumult-X/raw/master/quantumult%20X/getCookie.md, tag=获取Cookie（获取完就禁用）, update-interval=86400, opt-parser=false, enabled=false

https://raw.githubusercontent.com/zwf234/rules/master/QuantumultX/tailadv.conf, tag=去开屏广告, update-interval=86400, opt-parser=false, enabled=true

https://gitee.com/chavyleung/scripts/raw/master/box/rewrite/boxjs.rewrite.quanx.tf.conf, tag=BoxJs tf版, update-interval=86400, opt-parser=false, enabled=false

https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.quanx.conf, tag=BoxJS 商店版, update-interval=86400, opt-parser=false, enabled=true

[rewrite_local]

#本地复写规则

#Task远程订阅  https://raw.githubusercontent.com/zwf234/rules/master/qixin.json

#添加方法：打开构造请求，最上方第一个按钮，右上角+号添加即可

[task_local]

10 12,18 * * * https://raw.githubusercontent.com/id77/QuantumultX/master/task/jdWuLiu.js, tag=京东物流派件提醒, img-url=https://qxnav.com/rules/QuantumultX/img/jd.png, enabled=true

2 9 * * * https://qxnav.com/rules/QuantumultX/js/jd_bean_change.js, tag=京豆变动通知, img-url=https://qxnav.com/rules/QuantumultX/img/jd.png, enabled=true

55 23 * * * https://qxnav.com/rules/QuantumultX/js/zwf234/jd_unsubscribe.js, tag=取关京东店铺商品, img-url=https://qxnav.com/rules/QuantumultX/img/jd.png, enabled=true

0 8-22/3 * * * https://raw.githubusercontent.com/Peng-YM/QuanX/master/Tasks/nCov.js, tag=疫情动态, img-url=https://qxnav.com/rules/QuantumultX/img/COVID-19.png, enabled=true

0 8 * * * https://raw.githubusercontent.com/NobyDa/Script/master/JD-DailyBonus/JD_DailyBonus.js, tag=京东签到, img-url=https://raw.githubusercontent.com/NobyDa/mini/master/Color/jd.png, enabled=true

0 2 * * * https://raw.githubusercontent.com
