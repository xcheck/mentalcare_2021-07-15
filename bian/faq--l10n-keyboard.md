# keyboard map
### key config settings
```
/etc/default/keyboard
```
```
/etc/default/locale
```

### X11 rather than Wayland

$ grep U2026 /usr/share/X11/xkb/symbols/de   # (Debian9)

_**[AltGr]+[.] ^ShortCut … ^aka hellip**_

```
[44]:     key <AB09>	{ [    period,      colon,                U2026,     division 	] };
```

|"key" |\<key\> |[Shift]+\<key\> |[AltGr]+\<key\> |[Shift]+[AltGr]+\<key\> |
|--- |-- |-- |-- |-- |
|AB09 |. |: |… |÷ |


### numlock special

_**but desktop**_

/etc/kbd/config   # 'kbd' package for Text Konsole - ex (Debian9)

	# Turn on numlock by default
	LEDS=+num


_**gsettings**_   # owned by GNOME

    gsettings list-recursively | fgrep lock


_**: Cinnamon**_   # settings app Keyboard

    /org/cinnamon/settings-daemon/peripherals/keyboard/numlock-state		'on'  
    /org/cinnamon/settings-daemon/peripherals/keyboard/remember-numlock-state	wahr  


_**: otha**_   # apt install numlockx

[¹] /etc/X11/Xsession.d/55numlockx

- Initial settings


[²] /etc/default/numlockx

	NUMLOCK=auto   # (Debian9) as is
	NUMLOCK=on   # (Mint18)


[³] crontab -e   # /var/spool/cron/crontabs/pi

- numlockx on @ reboot