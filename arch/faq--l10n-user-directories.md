# user management and localisation l10n

### user initialisation

| default \<user\> [ ^pimp ](./raw--config-bash.md) | hereby directory ^/etc/skel/ |
| :--- | :--- |
| `adduser` | /etc/adduser.conf |
| | /etc/passwd |
| `groupmod` | initScript |
| | /etc/group |


:call\_me\_hand:

### directory names, icons match

| english | deutsch | comment |
| :--: | :--: | :--- |
| ~~Desktop~~ | Poster | |
| Public | ~~Öffentlich~~ | |
| Templates | ~~Vorlagen~~ | raspbian issue w/ file recognition |

>>>
/etc/xdg/user-dirs.defaults  
/etc/xdg/user-dirs.locale
>>>

~/.config/user_dir.dirs « supersedes above  
~/.config/user_dir.locale « language config

sudo update-locale fired via app raspi-config


:call\_me\_hand\_tone1:

### user-login-pic
* /usr/share/pixmaps/faces/ _« Raspbian stretch_
* ~/.face _« Cinnamon_
* ~/.face.icon _« SDDM_
