# sddm — simple desktop display manager
[LiNK ∷ https://github.com/sddm/sddm](https://github.com/sddm/sddm) _« man sddm_


* /etc/sddm/… _« :interrobang:_
* /etc/sddm.conf _« (¬Debian9)_
```
 1  [Autologin]
 2  Relogin=false
 3  Session=plasma.desktop
 4  User=<login>
```

* /etc/init/sddm.conf _« sddm display manager configuration_
```
11> #Numlock=on
>   #EnableAvatars=true « ~/.face.icon
>   #User=
>   #Session=
```
```
46  post-start script
47      sleep 2
```

* /etc/init.d/sddm
```
25	DEFAULT_DISPLAY_MANAGER_FILE=/etc/X11/default-display-manager
```

* /etc/X11/default-display-manager
```
 1	/usr/bin/sddm
```
