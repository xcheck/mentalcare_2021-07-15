# user management

### user initialisation

| [pimp](./raw--config-bash.md) default \<user\> | hereby directory ^/etc/skel/ |
| :--- | :--- |
| `adduser` | /etc/adduser.conf |
| | /etc/passwd |
| `groupmod` | initScript |
| | /etc/group |


:chains:

# localise the user directory

### directory names, match directory icons

> /etc/xdg/user-dirs.defaults … user-dirs.locale

~/.config/user_dir.dirs « supersedes above  
~/.config/user_dir.locale « language config

sudo update-locale fired via app raspi-config

| english | deutsch |
| :--: | :--: |
| ~~Desktop~~ | Poster |
| Public | ~~Öffentlich~~ |
| ~~Templates~~ | Vorlagen |
