# user management and localization

### user initialisation

| default \<user\> [ ^pimp ](./raw--config-bash.md) | hereby directory ^/etc/skel/ |
| :--- | :--- |
| `adduser` | /etc/adduser.conf |
| | /etc/passwd |
| `groupmod` | initScript |
| | /etc/group |


### directory names, icons match

| english | deutsch | comment |
| :--: | :--: | :--- |
| ~~Desktop~~ | Poster | |
| ~~Public~~ | Öffentlich | |
| Templates | ~~Vorlagen~~ | raspbian9 issue w/ file recognition |

>>>
/etc/xdg/user-dirs.defaults  
/etc/xdg/user-dirs.locale
>>>

~/.config/user_dir.dirs « supersedes above  
~/.config/user_dir.locale « language config

sudo update-locale fired via app raspi-config


### user-login-pic
* /usr/share/pixmaps/faces/ _« Raspbian stretch_
* ~/.face _« Cinnamon_
* ~/.face.icon _« SDDM_
