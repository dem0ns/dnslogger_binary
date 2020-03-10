# DNSLogger

### Get

`git clone --depth=1 https://github.com/nic329/dnslogger.git`

### Run

`sudo chmod +x dnslogger && sudo ./start`

Or Run With Docker

`docker-compose up` (for background use `docker-compose up -d`)


### Configuration

1. Import `init.sql` To Database.

2. Edit `config.ini`.

### Allow UDP Port 53

[CentOS] firewall-cmd --add-port 53/udp --permanent && firewall-cmd --reload


### Domain

1. You Must Have A Domain.
2. DNS Resolve: [NS] `log` -> `ns1.example.com`; [A] `ns1` -> `ip address`.
3. Finally: DnsLog Domain `log.example.com`

### Tips

1. Aliyun ECS: Stop local DNS server `systemctl stop systemd-resolved.service`


https://www.youtube.com/watch?v=JA8wn8sC844
