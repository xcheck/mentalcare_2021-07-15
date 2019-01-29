# r8169 ethernet doesn't work after wake up from suspend
### re-insert module after wake up \(remove &amp; add again\)

+ **Bionic Bug** _« \(Ubuntu18.04<sup>Mint19.1</sup>\)_  
  [ :arrow_up_small: https://bugs.launchpad.net/linux/+bug/1752772 ](https://bugs.launchpad.net/linux/+bug/1752772)
  
  /etc/systemd/system/fix-r8169.service
  
  ```
  # /etc/systemd/system/fix-r8169.service
  # systemctl enable fix-r8169.service
  #
  # https://bugs.launchpad.net/linux/+bug/1752772
  
  [Unit]
  Description=Fix RTL-8169 Driver on resume from suspend
  After=suspend.target
  
  [Service]
  User=root
  Type=oneshot
  ExecStartPre=/sbin/modprobe -r r8169
  ExecStart=/sbin/modprobe r8169
  TimeoutSec=0
  StandardOutput=syslog
  
  [Install]
  WantedBy=suspend.target
  ```