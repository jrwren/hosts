# hosts
My host files and bind config for DNS sink holes

pihole is great at blocking anything by name, not use ads.

## facebook

That Facebook f icon on nearly every media web page on the internet is how facebook is able to track every page you visit.
Even in private browsing mode that javascript will execute. 
Add https://raw.githubusercontent.com/jrwren/hosts/master/facebook as an adlist to your pihole to block it along with instagram.

## doh

DNS over HTTPS is a nice idea but it lets apps completely subvert your custom DNS configuration, your pihole.
Apps usually use a name to find a DoH and fallback to local DNS.
Add https://raw.githubusercontent.com/jrwren/hosts/master/doh to your pihole adlist so that apps cannot find a DoH server.

## ebay

ebay portscans you just for visiting their page. https://duckduckgo.com/?q=ebay+port+scanning&t=osx&ia=web
Never let anyone visit their page from your network.
Add https://raw.githubusercontent.com/jrwren/hosts/master/ebay to your pihole adlist.

## netflix

Netflix is great but if you don't subscribe, then they have no business knowing about you.
If you have a network connected television, it is likely telling Netflix when you watch and maybe what you watch even if you aren't a subscriber!
Add https://raw.githubusercontent.com/jrwren/hosts/master/netflix to your pihole adlist.

## ntp

I'm extra paranoid so I intercept ntp on my network.
I don't use the pihole adlist for this because I want the name to resolve to my home NTP server.
Add `time.apple.com` and `time.windows.com` to the `Local DNS`->`DNS Records` in pihole and use your local ntp server IP address.
If you don't have one, run `apt install ntp ntpstat` on your pihole system.
Sadly, these names also have CNAME records and AAAA records and so some traffic may still leak through. TODO: patch pihole to allow adding AAAA records.

## porn

Blocking all porn is very difficult.
The top porn sites https://toppornsites.com lists popular porn sites.
Sinkholing those domains blocks the most popular porn sites.
Add https://raw.githubusercontent.com/jrwren/hosts/master/topporn to your pihole adlist.
