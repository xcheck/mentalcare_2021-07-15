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

### watch monitor sizing detection

**config.txt**

```
# For more options and information see
# http://rpf.io/configtxt
# Some settings may impact device functionality. See link above for details
decode_MPG2=0x54e1704d   # 000000000818ada5

# Sets the memory split between the CPU and GPU; the CPU gets the remaining
# memory.
gpu_mem=64
gpu_mem_1024=128

# uncomment if you get no picture on HDMI for a default "safe" mode
#hdmi_safe=1

# uncomment this if your display has a black border of unused pixels visible
# and your display can output without overscan
#disable_overscan=1

# uncomment the following to adjust overscan. Use positive numbers if console
# goes off screen, and negative if there is too much border
#overscan_left=16
#overscan_right=16
#overscan_top=16
#overscan_bottom=16

# uncomment to force a console size. By default it will be display's size minus
# overscan.
#framebuffer_width=1280
#framebuffer_height=720

# uncomment if hdmi display is not detected and composite is being output
#hdmi_force_hotplug=1

# uncomment to force a HDMI mode rather than DVI. This can make audio work in
# DMT (computer monitor) modes
hdmi_drive=2

# uncomment to increase signal to HDMI, if you have interference, blanking, or
# no display
#config_hdmi_boost=4

# uncomment for composite PAL
#sdtv_mode=2

#uncomment to overclock the arm. 700 MHz is the default.
#arm_freq=800

# Uncomment some or all of these to enable the optional hardware interfaces
#dtparam=i2c_arm=on
#dtparam=i2s=on
#dtparam=spi=on

# Uncomment this to enable the lirc-rpi module
#dtoverlay=lirc-rpi

# Additional overlays and parameters are documented /boot/overlays/README

# Enable audio (loads snd_bcm2835)
dtparam=audio=on


# uncomment to force a specific HDMI mode (this will force VGA)
# list the EDID device_name by executing tvservice -n
[all]
#hdmi_group=0 # Auto-detect from EDID
#hdmi_group=1 # CEA (Consumer Electronic Assosiacion)
hdmi_group=2 # DMT (Display Monitor Timings)
hdmi_mode=36 # 1280x1024 @ 75Hz
hdmi_pixel_encoding=2 # RGB full (0-255) 3x8bit

[EDID=HWP-HP_Z24n] # HP Z24n
hdmi_group=2 # DMT (Display Monitor Timings)
hdmi_mode=69 # WUXGA 1920x1200 @ 60Hz
hdmi_pixel_encoding=2 # RGB full (0-255) 3x8bit
#[all]
[EDID=HWP-HP_Z24nf] # HP Z24nf
hdmi_group=2 # DMT (Display Monitor Timings)
hdmi_mode=82 # FHD 1920x1080 @ 60Hz
hdmi_pixel_encoding=2 # RGB full (0-255) 3x8bit
#[all]

# prerequesite w/ latency featured adapter vga>hdmi - edid file
[EDID=GSM-19MB15] # LG 19MB15 Touch
hdmi_group=2 # DMT (Display Monitor Timings)
hdmi_mode=36 # 1280x1024 @ 75Hz
hdmi_pixel_encoding=2 # RGB full (0-255) 3x8bit
#[all]
[EDID=PHL-Philips_190S] # Philips Brillance 190S9FB
hdmi_group=2 # DMT (Display Monitor Timings)
hdmi_mode=35 # SXGA 1280x1024 @ 60Hz
hdmi_pixel_encoding=2 # RGB full (0-255) 3x8bit
#[all]
```