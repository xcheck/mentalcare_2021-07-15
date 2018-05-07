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

### swap stereo audio channels

```
#
# ~/.asoundrc
# this supersedes /etc/asound.conf
#


# list available sound cards by executing aplay -Ll
# card 0: ALSA [bcm2835 ALSA], device 0: bcm2835 ALSA [bcm2835 ALSA]
# card 0: ALSA [bcm2835 ALSA], device 1: bcm2835 ALSA [bcm2835 IEC958/HDMI]


# PCM: Pulse-code modulation
# devices for recording or playing digitized sound samples

pcm_slave.raspi_composite.pcm "hw:ALSA,0"
pcm_slave.raspi_hdmi.pcm "hw:ALSA,1"

pcm.!default { # this swaps the audio channels
type route
slave raspi_hdmi
ttable.0.1 1
ttable.1.0 1
}


# CTL (left unchanged with original configuration)
# devices that allow manipulating the internal mixer and routing of the card

ctl.!default {
type hw
card 0
}
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
