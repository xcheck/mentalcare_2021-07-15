### numlock *but desktop*

1)	/etc/kbd/config   # 'kbd' package for Text Konsole - ex (Debian9)
	# Turn on numlock by default
	LEDS=+num

### numlockx *desktop* // app Keyboard alternative

**Cinnamon**

>
/org/cinnamon/settings-daemon/peripherals/keyboard/numlock-state		'on'  
/org/cinnamon/settings-daemon/peripherals/keyboard/remember-numlock-state	wahr  
>


0)	sudo apt install numlockx   # un:...
1-A)	/etc/default/numlockx
	NUMLOCK=auto   # (Debian9)
	NUMLOCK=on   # (Mint18)
1-B)	/etc/X11/Xsession.d/55numlockx
	# Initial settings
2)	/var/spool/cron/crontabs/pi   # crontab -e
	@reboot numlockx on
