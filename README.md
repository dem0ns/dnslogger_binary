# DNSLogger


### Tutorial | 演示
- https://www.youtube.com/watch?v=JA8wn8sC844
- https://www.bilibili.com/video/av95178665/

### Source Code | 源码

`https://github.com/dem0ns/dnslogger`


### Get | 获取

`git clone --depth=1 https://github.com/dem0ns/dnslogger_binary.git`


### Run | 运行

`docker-compose up -d`


### Firewall | 防火墙

[CentOS] `firewall-cmd --add-port 53/udp --permanent && firewall-cmd --reload`


### Domain | 域名

DNS Records: 1. [NS] `log` -> `ns1.yourdomain.com`, 2. [A] `ns1` -> `server ip`.


### Tips | 提示

1. 使用Ubuntu系统，必须先停止`systemd-resolved` (`systemctl stop systemd-resolved.service`)，并建议禁用此服务(`systemctl disable systemd-resolved.service`)，最后在`/etc/resolve.conf`中将`nameserver`指定到正常的DNS地址。
