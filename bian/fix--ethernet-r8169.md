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