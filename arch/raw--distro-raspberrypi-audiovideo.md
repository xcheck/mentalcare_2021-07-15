# Audio

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

:chains:

# Video

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
