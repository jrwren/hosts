# dnsmasq blocking

You don't need full pihole to sinkhole. pihole is built on dnsmasq. You can use these pihole config files to sinkhole common services. Each should be a .conf file in /etc/dnsmasq.d

```sh
cd /etc/dnsmasq.d
curl -siLO https://raw.githubusercontent.com/jrwren/hosts/main/dnsmasq/facebook.conf
curl -siLO https://raw.githubusercontent.com/jrwren/hosts/main/dnsmasq/ebay.conf
curl -siLO https://raw.githubusercontent.com/jrwren/hosts/main/dnsmasq/netflix.conf
curl -siLO https://raw.githubusercontent.com/jrwren/hosts/main/dnsmasq/snapchatads.conf
curl -siLO https://raw.githubusercontent.com/jrwren/hosts/main/dnsmasq/tiktok.conf
curl -siLO https://raw.githubusercontent.com/jrwren/hosts/main/dnsmasq/topporn.conf
curl -siLO https://raw.githubusercontent.com/jrwren/hosts/main/dnsmasq/vizio.conf
```