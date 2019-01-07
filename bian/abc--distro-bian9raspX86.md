[ :arrow_up_small: Linux Mint 17 MATE → ASUS Eee PC 1000HE ](https://www.rollator-parcours.com/de/HOWTO/ASUS-Eee-PC-1000HE/Linux-Mint-17-MATE/) _« content knowledge presumed_

[ :leftwards_arrow_with_hook: To-Do Liste ](#to-do-liste)


<br>

# Understatement-of-Performance — Linux <sup>&reg;oller</sup>
### Gettin started

+ **pi \/ raspberry** _« default login_  
  [ :arrow_up_small: Raspbian x86 Images ](https://downloads.raspberrypi.org/rpd_x86/images/)


+ **best of keyboard shortcuts**  
  [ :arrow_up_small: Best Linux Keyboard Shortcuts ](https://www.linux.com/learn/best-linux-keyboard-shortcuts)
  
  | hotkeys | function |
  | :--- | :--- |
  | \[super\] | dektop menu |
  | \[alt\]+\[space\] | app menu |
  | \[ctrl\]+\[alt\]+\[T\] | start app terminal |
  
  …
+ **l10n keyboard map-file numlock**  
  [ :arrow_right_hook: faq--l10n-keyboard ](./faq--l10n-keyboard.md) _« full story_


:call_me_hand_tone1:

### user customization and localisation "l10n"

+ **user management and login-pic**  
  [ :arrow_right_hook: faq--l10n-user-directories ](./faq--l10n-user-directories.md) _« full story_


+ **~/.bash_aliases** _« bash aliases for the list command et al._  
  [ :arrow_right_hook: raw--config-bash ](./raw--config-bash.md) _« full story_


+ **l10n fonts spellcheck**  
  [ :arrow_right_hook: faq--l10n-fonts-n-spell ](./faq--l10n-fonts-n-spell.md) _« full story_


:call_me_hand_tone2:

### calDAV-Workaround for Kalender

+ **enter your calDAV calendar in Evolution to augment it for** `gnome-calendar`


### Druckeinstellungen

+ **install pakets** `cups` `system-config-printer`
  
  ```
  usermod -gG lpadmin pi
  ```


:call_me_hand_tone3:

### trim flash drive

+ **\/etc\/fstab** _« missing_ \/etc\/cron.weekly\/\* _supposes a discard_


:call_me_hand_tone4:

### Rapberry Pi 3

+ **audio video words to**  
  [ :arrow_right_hook: vic--raspberrypi-audiovideo ](./vic--raspberrypi-audiovideo.md) _« full story_


:chains:

# Asus VivoBook E12 E203N
### LVM Debian9 Stretch

+ **ASUS VivoBook E12 E203N**
  
  ```
  ui install « from debian dvd image #4 (never the less find #1)
  ° ¬LVM either or Network ¡w/o firmware! ↲ ↵
  ° firmware just cope /pool/f/firmaware-free/firmware-linux-free.deb ~/.
  
  vivobook
  vgvivobook-system … 8MB … "Vivo System"
  vgvivobook-home … 22452MB … "Vivo Home"
  ```


:chains:

# To-Do Liste

```
chroot

calibre
kde-l10n-de kde-icons-mono digikam kdenlive

panel-clock: %R'%S

```