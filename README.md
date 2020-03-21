# DNSLogger


### Tutorial | 演示
- https://www.youtube.com/watch?v=JA8wn8sC844
- https://www.bilibili.com/video/av95178665/


### Get | 获取

`git clone --depth=1 https://github.com/nic329/dnslogger.git`


### Run | 运行

`docker-compose up` (for background use `docker-compose up -d`)


### Port Policy | 端口策略

[CentOS] firewall-cmd --add-port 53/udp --permanent && firewall-cmd --reload


### Domain | 域名

DNS Record: 1. [NS] `log` -> `ns1.example.com`, 2. [A] `ns1` -> `server ip`.


### 提示

1. 阿里云服务器需要停止本地DNS服务： `systemctl stop systemd-resolved.service`
