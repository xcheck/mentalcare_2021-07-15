### numlock *but desktop*

1)	/etc/kbd/config   # 'kbd' package for Text Konsole - ex (Debian9)

	# Turn on numlock by default
	LEDS=+num


---
### numlockx *desktop* // app Keyboard alternative

_**Cinnamon**_

    /org/cinnamon/settings-daemon/peripherals/keyboard/numlock-state		'on'  
    /org/cinnamon/settings-daemon/peripherals/keyboard/remember-numlock-state	wahr  


1)	/etc/X11/Xsession.d/55numlockx   # apt install numlockx

- Initial settings


2)	/etc/default/numlockx

	NUMLOCK=auto   # (Debian9)
	NUMLOCK=on   # (Mint18)


3)  crontab -e   # /var/spool/cron/crontabs/pi

- numlockx on @ reboot
