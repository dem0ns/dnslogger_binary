# dnslogger

### Run

chmod +x dnslogger && ./dnslogger

### Configuration

1. Import sql struct file to database. (record.sql)
2. Change config.ini. (`conn` database connect config information, `default ip` DNS result ip.)


### Allow UDP Port 53

[CentOS] firewall-cmd --add-port 53/udp --permanent && firewall-cmd --reload
