# Linux ^®oller — Annoyances-by-Design
CROW ^scroll

[ROPA ∷ Raspbian Stretch Respin](#raspbian-blank-on-16g-linux-install-respin)  
[ROPA ∷ vc4-rapberry-pi-3](#vc4-rapberry-pi-3)  
[ROPA ∷ Debian9 Stretch — vivo](#debian9-stretch-vivo)  
[ROPA ∷ Open List](#open-list)  


[LINK ∷ l10n fonts login-pic](./faq--l10n-fontyin.md)  
[LINK ∷ l10n keyboard numlock](./faq--l10n-keyboard.md)  


### Default login

[ pi / raspberry ](https://downloads.raspberrypi.org/raspbian/images/)


### keyboard shortcuts

| hotkeys | function |
| :--- | :--- |
| \[super\] | dektop menu |
| \[alt\]+\[space\] | app menu |
| \[ctrl\]+\[alt\]+\[T\] | start app terminal |


:chains:

### user management

[ user initialisation on commandline ](./raw--config-userdirectory.md)


### ~/.bash_aliases

[ bash aliases for the list command ](./raw--config-bash.md)


:chains:

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
kde-l10n-de kde-icons-mono libreoffice-l10n-de libreoffice-help-de geany-plugin-spellcheck chromium-l10n
enchant \[aspell-de\] hunspell-de-de hyphen-de mythes-de   # /usr/share/myspell/dicts
```

# Open List
```
chroot

calibre
kde-l10n-de digikam

panel-clock: %R'%S

```
