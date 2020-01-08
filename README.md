# DNSLogger

### Run

chmod +x dnslogger && ./dnslogger


### Configuration

1. Import sql struct file to database. (record.sql)
2. Change config.ini. (`conn` database connect config information, `default ip` DNS result ip.)


### Allow UDP Port 53

[CentOS] firewall-cmd --add-port 53/udp --permanent && firewall-cmd --reload


### Domain (For example: DNS log doamin is log.example.com)

1. You must have a domain.
2. Add a `DNS Host`: the `DNS server` column write with `ns1.example.com`, `ip address` is your server ip.
3. Add a DNS resolve: `Host` write with `log`, `Type` write with `NS`, `value` write with `ns1.example.com`.


### Tips

1. Aliyun ECS need to stop local DNS server `systemctl stop systemd-resolved.service`
