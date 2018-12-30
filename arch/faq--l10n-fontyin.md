#### user-login-pic
* /usr/share/pixmaps/faces/ _« Raspbian stretch_
* ~/.face _« Cinnamon_
* ~/.face.icon _« SDDM_


### Debian 9 "Stretch" spin-off Raspbian

```
kde-l10n-de libreoffice-l10n-de libreoffice-help-de (libreoffice-style-galaxy) geany-plugin-spellcheck [firefox-esr-l10n-de] [chromium-l10n]
enchant (aspell-de) hunspell-de-de-frami hyphen-de mythes-de   # /usr/share/myspell/dicts
ttf-mscorefonts-installer fonts-crosextra-caladea fonts-crosextra-carlito # ttf-liberation dropped by fonts-liberation
fonts-mathjax fonts-wqy-microhei
gnome-keyring   # requisite w/ evolution
```

#### quote window

>>>
For an example of well-hinted fonts I personally 
recommend the liberation fonts, but only v1, the 2.0 update broke the world 
class hinting the fonts had, which is why debian has both.
>>>


|cmd |conf |rel  
|---|--|--  
| localectl [list-locales¦set-locale] | /etc/locale.conf | Systemd  
| locale | /etc/default/locale |  


### Windows Fonts

|windows path|linux path  
|---|--  
|%SYTEMROOT%\Fonts|~/.local/share/fonts/  
||/usr/local/share/fonts/  


> sudo fc-cache -f
