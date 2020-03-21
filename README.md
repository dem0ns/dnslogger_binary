# DNSLogger


### Tutorial | 演示
- https://www.youtube.com/watch?v=JA8wn8sC844
- https://www.bilibili.com/video/av95178665/


### Get | 获取

`git clone --depth=1 https://github.com/nic329/dnslogger.git`


### Run | 运行

`docker-compose up` (for background use `docker-compose up -d`)


### Port Policy | 端口策略

[CentOS] `firewall-cmd --add-port 53/udp --permanent && firewall-cmd --reload`


### Domain | 域名

DNS Record: 1. [NS] `log` -> `ns1.example.com`, 2. [A] `ns1` -> `server ip`.


### Tips | 提示

1. If you are using Alibaba Cloud, you must stop systemd-resolved first(`systemctl stop systemd-resolved.service`), and you can disable it (`systemctl disable systemd-resolved.service`), last setup change the nameserver to `8.8.8.8` `8.8.4.4` in /etc/resolve.  如果你使用的是阿里云，你必须先停止域名解析服务(`systemctl stop systemd-resolved.service`)，你还可禁止此服务(`systemctl disable systemd-resolved.service`)，最后你需要在/etc/resolve中将nameserver指定到`8.8.8.8` `223.5.5.5`。
