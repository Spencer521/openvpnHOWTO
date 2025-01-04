# openvpnHOWTO
openvpn搭建_http-proxy速通_参考手册

折腾一个月，分享几篇文档带你入门
看见这篇文有福啦^^-___-^^
有用记得~收藏
> 新年快乐！点赞的人好运连连！


起初看见这篇给我一个大体框架
[利openVPN自带的http-proxy突破**](https://www.yjlink.cc/?id=1175)
后来发现同名文：https://www.micoder.cc/blog/1175.html


## 然后赶紧双手奉上官方手册：

官方教程步骤：[2.x HOW TO](https://openvpn.net/community-resources/how-to/#installing-openvpn)
二（同上）：https://community.openvpn.net/openvpn/wiki/HOWTO
参数说明书：https://openvpn.net/community-resources/reference-manual-for-openvpn-2-6/

## server篇
Tejas写的详细步骤：
https://blog.tmthecoder.dev/posts/part-1-building-a-xor-patched-vpn-server/

openvpn-over-proxy-install.sh :
https://github.com/Null3rror/OpenVPN-over-Proxy/blob/main/openvpn-over-proxy-install.sh

openvpn有web界面，好像可能不支持http-proxy，感兴趣可以玩玩
https://cloud.tencent.com/developer/article/2207426

## client篇
**客户端配置分流**（鱼+熊掌）：
https://github.com/jonohill/docker-openvpn-proxy/tree/master?tab=readme-ov-file

客户端全局路由：![image](https://github.com/user-attachments/assets/f22615a4-1592-40df-aebd-ae8549c17aed)

![全局](https://i-blog.csdnimg.cn/direct/9317effd05bb42f8b100fc978534e970.png)

## 代理加速：
[DockerHub国内镜像源列表（2024年6月18日 亲测可用）](https://linux.do/t/topic/114516)

1、往链接前面加https://ghproxy.com/，例如：
> https://ghproxy.com/https://github.com/Nyr/openvpn-install/......
已失效。自行访问https://ghproxy.com/获取更新。

2、使用 docker hub proxy将原拉取镜像命令：
[DockerHub 镜像加速](https://docker.anyhub.us.kg/)
> docker pull ghcr.io/helloworld/helloworld
替换为下面的加速拉取镜像命令：
> docker pull ghcr.anyhub.us.kg/helloworld/helloworld

3、linux代理软件gg:
https://github.com/mzz2017/gg/blob/main/README_zh.md

代理软件
HTTP：squid、privoxy、polipo
socks ：srelay、ss5


未完待续*
