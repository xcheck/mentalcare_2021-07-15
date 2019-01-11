# Windows tweaks
### Cheat sheet und andere Oster-Eier

+ **"Compact OS" statt NTFS-Kompression** [ <sup><sup>ct</sup> 2017-09-146</sup> ](https://ct.de/yk9n)  
  
  compact /compactos  
  compact /compactos:always


+ **"Energiesparplan Festplatte" \(lange Pause vor dem Speichern\)** <sup><sup>ct</sup> 2017-08-152</sup>  
  …erweiterte Energieeinstellungen


+ **Hardware-Diagnose** [ <sup><sup>ct</sup> 2016-20-109</sup> ](https://ct.de/yqbx)  

  ```
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
  sfc /verifyonly		System File Checker vgl. /scannow
  -
  netsh wlan show wirelesscap
  ```


+ **Bluescreen vs. "Automatisch Neustart durchführen"** <sup><sup>ct</sup> 2016-20-092 ff.</sup>  
  System \[\> Systeminfo\] \> Erweiterte Systemeigenschaften \> Starten und Wiederherstellen: …


+ **ANSI-Escape-Sequenzen in der Windows-Eingabeaufforderung** <sup><sup>ct</sup> 2016-19-150</sup>  
  https://heise.de/-3305785
  
  C:\Users\All Users\tweakCommandPromptColor.bat
  prompt $E[92m$P$G$E[37m


+ **Windows 7 bekommt einen großen Sammel-Patch** [ <sup><sup>ct</sup> 2016-12-036</sup> ](http://ct.de/yrns)


+ **Hotline: SATA Link Power Management mit Windows-Standardtreiber** [ <sup><sup>ct</sup> 2016-09-175</sup> ](http://ct.de/ycu8)
  
  1609-175.zip


+ **Admin-Konsole per Rechtsklick im Windows Explorer** <sup><sup>ct</sup> 2016-06-164</sup>  
  http://heise.de/-3119116
  
  C:\Users\All Users\cmdRunas-byD*.reg


+ **PID.txt**  
  https://www.deskmodder.de/wiki/index.php/Seriennummern_Key_generischer_Schlüssel_Windows_10
  
  ```
  Product Key:	VK7JG-NPHTM-C97JM-9MPGT-3V66T	Pro-Generic
  ```


:chains:

# To-Do Liste

```
---
C:\Windows.old § "NT SERVICE\TrustedInstaller" ACL kopieren
Autostart: Aufgabenplanung > Aktion > Aufgabe erstellen... (Trigger)
Aufgabe: Datenträgerverwaltung > Aktion > Virtuelle Festplatte anfügen

Trigger: µSD-Card, .vhdx, sound signal

---
wav art:=musik
C:\Windows\Media

---
@1703 Lockscreen per .reg
heise.de/-3686999 | News > 2017 > KW17


@Task-Manager > Autostart per [WIN]+[R] shell:startup
\\live.sysinternals.com | autoruns.exe
```