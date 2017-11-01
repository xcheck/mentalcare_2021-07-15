# sddm display manager configuration

* man sddm
* https://github.com/sddm/sddm


/etc/sddm/ ???  
/etc/sddm.conf ¼ (¬Debian9)  
/etc/init/sddm.conf - sddm display manager configuration
```
53	Numlock=on
13	#EnableAvatars=true   # ~/.face.icon rather than ~/.face
53	User=uwe
13	#Session=
…
23	post-start script
52	    sleep 2
```

/etc/init.d/sddm
```
26	DEFAULT_DISPLAY_MANAGER_FILE=/etc/X11/default-display-manager
```

/etc/X11/default-display-manager
```
26	/usr/bin/sddm
```
