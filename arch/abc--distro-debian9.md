# Linux ^®oller — Annoyances-by-Design ^Debian9 ^Stretch

CROW ^scroll


[ LiNK ∷ Debian9 Stretch — vivo ](#debian9-stretch-vivo)  
[ LiNK ∷ Open List ](#open-list)  


[ LⁱNK ∷ l10n fonts login-pic ](./faq--l10n-fontyin.md)  
[ LⁱNK ∷ l10n keyboard numlock ](./faq--l10n-keyboard.md)  


### Iso image validation
#### …run the sha1sum program to check against the value in the checksum file

```
sha1sum -c 2017-09-07-raspbian-stretch.zip.sha1
```

#### Write a zipped image to the SD card w/ `dd` err ^ound ~~`…conv=fsync`~~

```
unzip -p 2017-09-07-raspbian-stretch.zip | sudo dd of=/dev/sdX bs=4M oflag=direct status=progress
```

#### Error scan the image on the SD card w/ `rsync`
> ```
sudo dd if=/dev/sdX of=from-sd-card.img bs=1M count=5200 oflag=direct status=progress
sudo truncate from-sd-card.img --reference ubuntu-17.10-desktop-amd64.iso
diff -s from-sd-card.img ubuntu-17.10-desktop-amd64.iso
sync
```

```
sudo rsync -av --progress ubuntu-17.10-desktop-amd64.iso /dev/sdX
```


#### ~/.config/user_dir.dirs vs. /etc/xdg

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


## Debian9 Stretch vivo

```
ui install
° ¬LVM either or Network ¡w/o firmware! ↲ ↵
° firmware just cope /pool/f/firmaware-free/firmware-linux-free.deb ~/.

vivobook
vgvivobook-system … 8MB … "Vivo System"
vgvivobook-home … 22452MB … "Vivo Home"
```


#### .deb Pakage Install from USB as CDROM
plug USB device an execute
```
sudo mount --bind /media/<user>/<USB Debian Image Number> /media/cdrom
```



# Open List

```
chroot

calibre
kde-l10n-de digikam
```