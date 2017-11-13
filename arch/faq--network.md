# network devices interfaces — setup config
## AP – access point switch vs. bridge
iptraff[ic]  
tcpdump → wireshark


* interface — network device

```
iw dev [wlan0]
iw phy [phy0] info
```

## NTP — network t ^ime prot ^ocol
* /etc/ntp.conf

```txt
# You do need to talk to an NTP server or two (or three).
#server ntp.your-provider.example
server fritz.box iburst

# pool.ntp.org maps to about 1000 low-stratum NTP servers.  Your server will
# pick a different set every time it starts up.  Please consider joining the
# pool: <http://www.pool.ntp.org/join.html>
server 0.de.pool.ntp.org iburst
server 1.de.pool.ntp.org iburst
server 2.de.pool.ntp.org iburst
server 3.de.pool.ntp.org iburst
```


---
*   raspi-config

>>>
4 Wait for Network at Boot
>>>


---
*   konsole

```bash
#!/usr/bin/env bash

sudo systemctl stop ntp && sleep 2 && sudo systemctl start ntp && printf " \u2713 Fertig\t\u2026 start ntp\n"
ntpq -p

# wait $!;
```
