# Linux ^®oller — Annoyances-by-Design
CROW ^scroll

[ROPA ∷ Raspbian Stretch Respin](#raspbian-blank-on-16g-linux-install-respin)  
[ROPA ∷ vc4-rapberry-pi-3](#vc4-rapberry-pi-3)  
[ROPA ∷ Debian9 Stretch — vivo](#debian9-stretch-vivo)  
[ROPA ∷ Open List](#open-list)  


[LINK ∷ l10n fonts login-pic](./faq--l10n-fontyin.md)  
[LINK ∷ l10n keyboard numlock](./faq--l10n-keyboard.md)  


### keyboard shortcuts

| hotkeys | function |
| :--- | :--- |
| \[super\] | dektop menu |
| \[alt\]+\[space\] | app menu |
| \[ctrl\]+\[alt\]+\[T\] | start app terminal |


### Default login

[ pi / raspberry ](https://downloads.raspberrypi.org/raspbian/images/)


### user management

|[pimp](#bash_aliases) default \<user\> |hereby directory ^/etc/skel/ |  
| :--- | :--- |  
|`adduser` |/etc/adduser.conf |
| |/etc/passwd |
|`groupmod` |initScript |
| |/etc/group |

**initScript ^todo — …check pi placement then append ,`whoami`**
```
sed -e "s/:pi.*$/&,`whoami`/g" /etc/group-

DEST_USER=`whoami`
ETC_GROUP="/etc/group-"
if ! fgrep -q ${DEST_USER} ${ETC_GROUP}; then
    sed -e "s/:pi.*$/&,${DEST_USER}/g" ${ETC_GROUP}
fi
```

### directory names, match directory icons

> /etc/xdg/user-dirs.defaults … user-dirs.locale

~/.config/user_dir.dirs « supersedes above  
~/.config/user_dir.locale « language config

sudo update-locale fired via app raspi-config

|english |deutsch |
| :--: | :--: |
|~~Desktop~~ |Poster |
|Public |~~Öffentlich~~ |

#### ~/.bash_aliases
> **~/.bashrc**
> ```
…
# enable color support of ls and also add handy aliases
if [ -x /usr/bin/dircolors ]; then
    test -r ~/.dircolors && eval "$(dircolors -b ~/.dircolors)" || eval "$(dircolors -b)"
    alias ls='ls --color=auto'
    #alias dir='dir --color=auto'
    #alias vdir='vdir --color=auto'
…
    alias grep='grep --color=auto'
    alias fgrep='fgrep --color=auto'
    alias egrep='egrep --color=auto'
fi
…
# colored GCC warnings and errors
#export GCC_COLORS='error=01;31:warning=01;35:note=01;36:caret=01;32:locus=01:quote=01'
…
# some more ls aliases
#alias ll='ls -l'
#alias la='ls -A'
#alias l='ls -CF'
…
# Alias definitions.
# You may want to put all your additions into a separate file like
# ~/.bash_aliases, instead of adding them here directly.
# See /usr/share/doc/bash-doc/examples in the bash-doc package.
…
if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
fi
```

```
# Alias definitions.
# You may want to put all your additions into a separate file like
# ~/.bash_aliases, instead of adding them here directly.
# See /usr/share/doc/bash-doc/examples in the bash-doc package.

# colored GCC warnings and errors
#export GCC_COLORS='error=01;31:warning=01;35:note=01;36:caret=01;32:locus=01:quote=01'

# some more ls aliases
alias ll='ls -AlF'
alias la='ls -alF'
alias l='ls -lF'

alias py='/usr/bin/env python3'
```


### VC4 — Rapberry Pi 3 
```
sudo lsmod | grep - bmc2835
sudo modprobe [option] snd_bmc2835 [index=…]
```
```
vcgencmd get-config [str|int]
sudo vcdbg reloc
```


* tvservice -m (CEA|DMT)
* tvservice -n _« current device\_name_
* tvservice -s _« current state_

* EDID _« config.txt_
```
tvservice -d edit.dat; edidparser edid.dat > edid.txt
```


### ALSA — advanced linux audio system
* raspbian
```
/opt/vc/src/hello_pi/hello_video/text.h264
```

* alsactl alsamixer amixer
```
/etc/asound.conf
```
```
aplay -l
aplay -L | grep -i 'sysdefault'
```

## Debian9 Stretch vivo
```
ui install
° ¬LVM either or Network ¡w/o firmware! ↲ ↵
° firmware just cope /pool/f/firmaware-free/firmware-linux-free.deb ~/.

vivobook
vgvivobook-system … 8MB … "Vivo System"
vgvivobook-home … 22452MB … "Vivo Home"
```
### l10n – localisation (pakets)

```
kde-l10n-de kde-icons-mono libreoffice-l10n-de libreoffice-help-de ?geany-plugin-spellcheck? chromium-l10n
enchant hunspell-de-de hyphen-de mythes-de   # /usr/share/myspell/dicts
fonts-crosextra-caladea
fonts-crosextra-carlito
fonts-mathjax
fonts-wqy-microhei
ttf-mscorefonts-installer
```

# Open List
```
chroot

calibre
kde-l10n-de digikam

panel-clock: %R'%S

```
