# Skype ^https://www.skype.com/go/getskype-linux-beta-dynamic

[J] libqt4 Paket installieren  
[J] libQtWebKit4 Paket installieren

```
    # tar -jxvf skype-4.2.0.13.tar.bz2

    # rm -f /usr/local/share/applications/skype.desktop
    # rm -f /usr/local/bin/skype
    # rm -f /usr/local/etc/dbus-1/system.d/skype.conf
    # rm -rf /usr/local/share/skype

    # mv skype-4.2.0.13 /usr/local/share/skype
    # cd /usr/local/share/skype
    # mv skype.conf /usr/local/etc/dbus-1/system.d/ # Verzeichnis ggf. vorher erstellen
    # mv skype /usr/local/bin/
    # mv skype.desktop /usr/local/share/applications/ # Verzeichnis ggf. vorher erstellen

    # vim /usr/local/share/applications/skype.desktop
```

    …folgende Zeile anpassen:

```
    Icon=/usr/local/share/skype/icons/SkypeBlue_96x96.png
```
