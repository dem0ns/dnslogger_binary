# DNSLogger

### Run

`sudo chmod +x dnslogger && sudo ./start`

Or Run With Docker

`docker-compose up` (for background use `docker-compose up -d`)


### Configuration

1. Import `init.sql` to database.

2. Edit `config.ini`.

### Allow UDP Port 53

[CentOS] firewall-cmd --add-port 53/udp --permanent && firewall-cmd --reload


### Domain

1. You must have a domain.
2. DNS Host: `ns1.example.com` -> `ip address`.
3. DNS resolve: [NS] `log` -> `ns1.example.com`; [A] `ns1` -> `ip address`.
4. Finally: DnsLog Domain `log.example.com`

### Tips

1. Aliyun ECS: Stop local DNS server `systemctl stop systemd-resolved.service`
