# Debian 9 "Stretch" spin-off Raspbian

`libreoffice-l10n-de` `libreoffice-help-de` \(libreoffice-style-tango\) \(libreoffice-style-galaxy\) `[firefox-esr-l10n-de]` `[chromium-l10n]` `kde-l10n-de` ` kde-icons-mono`  
`enchant` \(aspell-de\) `hunspell-de-de-frami` `hyphen-de mythes-de` `geany-plugin-spellcheck`   # /usr/share/myspell/dicts  
`ttf-mscorefonts-installer` `fonts-crosextra-caladea` `fonts-crosextra-carlito` # ttf-liberation dropped for fonts-liberation  
`fonts-mathjax` `fonts-wqy-microhei`  
`gnome-keyring`   # requisite w/ evolution


### ttf-liberation dropped for fonts-liberation

>>>
For an example of well-hinted fonts I personally 
recommend the liberation fonts, but only v1, the 2.0 update broke the world 
class hinting the fonts had, which is why debian has both.
>>>


### character set

| cmd | conf | rel
| :--- | :--- | :---
| localectl [list-locales¦set-locale] | /etc/locale.conf | Systemd
| locale | /etc/default/locale |

> sudo fc-cache -f


:chains:

# Windows Fonts

| windows path | linux path
| :--- | :---
| %SYTEMROOT%\Fonts | /usr/local/share/fonts/
| | ~/.local/share/fonts/
