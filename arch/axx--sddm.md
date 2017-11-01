# sddm — simple desktop display manager
[LiNK ∷ https://github.com/sddm/sddm](https://github.com/sddm/sddm) _« man sddm_


* /etc/sddm/… _« :interrobang:_
* /etc/sddm.conf _« (¬Debian9)_
* /etc/init/sddm.conf _« sddm display manager configuration_
```
53	Numlock=on
13	#EnableAvatars=true   # ~/.face.icon rather than ~/.face
53	User=<user_login>
13	#Session=
…
23	post-start script
52	    sleep 2
```

* /etc/init.d/sddm
```
26	DEFAULT_DISPLAY_MANAGER_FILE=/etc/X11/default-display-manager
```

* /etc/X11/default-display-manager
```
26	/usr/bin/sddm
```
