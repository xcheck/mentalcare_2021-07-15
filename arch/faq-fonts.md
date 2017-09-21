## Debian 9 "Stretch" spin-off Raspbian

```
kde-l10n-de libreoffice-style-galaxy libreoffice-l10n-de libreoffice-help-de firefox-esr-l10n-de geany-plugin-spellcheck   # /usr/share/myspell/dicts
enchant (aspell-de) hunspell-de-de hyphen-de mythes-de
fonts-crosextra-caladea
fonts-crosextra-carlito
fonts-mathjax
fonts-wqy-microhei
ttf-mscorefonts-installer   # phase shift internal: transition ttf-liberation to fonts-liberation [from extra to optional]
gnome-keyring   # requisite w/ evolution
```

---
*quote window*

>>>
For an example of well-hinted fonts I personally 
recommend the liberation fonts, but only v1, the 2.0 update broke the world 
class hinting the fonts had, which is why debian has both.
>>> 


```
~$ apt show ttf-liberation 
Package: ttf-liberation
Version: 1:1.07.4-2
Priority: extra
Section: oldlibs
Source: fonts-liberation
Maintainer: Debian Fonts Task Force <pkg-fonts-devel@lists.alioth.debian.org>
Installed-Size: 38,9 kB
Depends: fonts-liberation
Homepage: https://fedorahosted.org/liberation-fonts/
Tag: role::shared-lib
Download-Size: 9.878 B
APT-Sources: http://ftp.de.debian.org/debian stretch/main amd64 Packages
Description: Übergangspaket
 Dieses Übergangspaket kann gefahrlos entfernt werden.
```


```
~$ apt show fonts-liberation
Package: fonts-liberation
Version: 1:1.07.4-2
Priority: optional
Section: fonts
Maintainer: Debian Fonts Task Force <pkg-fonts-devel@lists.alioth.debian.org>
Installed-Size: 2.143 kB
Breaks: ttf-liberation (<< 1.07.0-2)
Replaces: ttf-liberation (<< 1.07.0-2)
Homepage: https://fedorahosted.org/liberation-fonts/
Tag: made-of::font, role::data, x11::font
Download-Size: 827 kB
APT-Manual-Installed: no
APT-Sources: http://ftp.de.debian.org/debian stretch/main amd64 Packages
Description: Schriften mit den gleichen Metriken wie Times, Arial und Courier
 Ein Satz von Schriften mit und ohne Serifen und fester Zeichenbreite von Red
 Hat mit genau den gleichen Metriken wie die (unfreien) Microsoft-Schriften
 Times, Arial und Courier. Durch die identischen Metriken können sie als
 direkter Ersatz der Microsoft-Versionen dienen. Der Name der Schriftfamilie
```


## Windows Fonts

Quelle: Linux-Umzug, c't 2014, Heft 19, Seite 138


%SYTEMROOT%\Fonts -->

a) ~/.local/share/fonts/

b) /usr/local/share/fonts/ (als root)


`sudo fc-cache -f`
