```
---
### C:\Windows.old § "NT SERVICE\TrustedInstaller" ACL kopieren
Autostart: Aufgabenplanung > Aktion > Aufgabe erstellen... (Trigger)
Aufgabe: Datenträgerverwaltung > Aktion > Virtuelle Festplatte anfügen

Trigger: µSD-Card, .vhdx, sound signal
---
wav art:=musik
C:\Windows\Media


@1703 Lockscreen per .reg
heise.de/-3686999 | News > 2017 > KW17


@Task-Manager > Autostart per [WIN]+[R] shell:startup
\\live.sysinternals.com | autoruns.exe


###
# "Energiesparplan Festplatte" (lange Pause vor dem Speichern) | ct 2017, Heft 08, Seite 152 // hos@
...erweiterte Energieeinstellungen



###
# "Compact OS" statt NTFS-Kompression | ct 2017, Heft 09, Seite 146
https://ct.de/yk9n

compact /compactos
compact /compactos:always


###
# Hardware-Diagnose | ct 2016, Heft 20, Seite 109
https://www.heise.de/ct/ausgabe/2016-20-Tools-zur-Hardware-Diagnose-unter-Windows-3318789.html
https://ct.de/yqbx
taskmgr.exe		Task Manager -- Strg+Shift+ESC
resmon.exe		Ressourcenmonitor
perfmon.exe /sys	Leistungsüberwachung
devmgmt.msc		Geräte Manager
diskmgmt.msc		Datenträgerverwaltung
msinfo32.exe		Systeminformationen
mdsched.exe		Windows-Speicherdiagnose
eventvwr.msc		Ereignisanzeige
-
cleanmgr.exe		Datenträgerbereinigung
msconfig.exe		Systemkonfiguration
-
msdt.exe		Microsoft Support-Diagnosetool
-
sfc /verifyonly		System File Checker /scannow
netsh wlan show wirelesscap


###
# Bluescreen vs. "Automatisch Neustart durchführen" | ct 2016, Heft 20, Seite 92 ff.
System [> Systeminfo] > Erweiterte Systemeigenschaften > Starten und Wiederherstellen: ...


###
# ANSI-Escape-Sequenzen in der Windows-Eingabeaufforderung | c't Magazin 2016, Heft 19, Seite 150
https://www.heise.de/ct/ausgabe/2016-19-ANSI-Escape-Sequenzen-in-der-Windows-Eingabeaufforderung-3305785.html

C:\Users\All Users\tweakCommandPromptColor.bat
prompt $E[92m$P$G$E[37m


###
# Windows 7 bekommt einen großen Sammel-Patch | c't Magazin 2016, Heft 12, Seite 36
http://www.heise.de/ct/ausgabe/2016-12-Windows-7-bekommt-einen-grossen-Sammel-Patch-3214123.html
http://heise.de/-3214123
http://ct.de/yrns


###
# Hotline: SATA Link Power Management mit Windows-Standardtreiber | c't Magazin 2016, Heft 9, Seite 175
1609-175.zip
http://www.heise.de/ct/hotline/SATA-Link-Power-Management-mit-Windows-Standardtreiber-3166936.html
http://heise.de/-3166936
http://ct.de/ycu8


###
# Admin-Konsole per Rechtsklick im Windows Explorer | c't Magazin 2016, Heft 6, Seite 164
http://www.heise.de/ct/hotline/Admin-Konsole-per-Rechtsklick-im-Windows-Explorer-3119116.html
http://heise.de/-3119116

C:\Users\All Users\cmdRunas-byD*.reg


###
# PID.txt
https://www.deskmodder.de/wiki/index.php/Seriennummern_Key_generischer_Schl%C3%BCssel_Windows_10
Product Key:	VK7JG-NPHTM-C97JM-9MPGT-3V66T	Pro-Generic
```