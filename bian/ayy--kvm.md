# KVM kernel-based virtual machine
### requirements

+ **cpu virt <sup>technology</sup> by intel…**
  
  ```
  cat /etc/os-release; dmesg | grep -i virt; egrep '^flags.*(vmx|svm)' /proc/cpuinfo
  ```


+ **kernel-based modul kvm** _« \(Ubuntu18.04<sup>Mint19.1</sup>\)_  
  $ lsmod | grep kvm
  
  ```
  kvm_intel             204800  0
  kvm                   593920  1 kvm_intel
  irqbypass              16384  1 kvm
  ```


### kvm\/spice server, client, guest

+ **qemu-kvm** _« \(Ubuntu18.04<sup>Mint19.1</sup>\)_
  
  ```
  sudo apt install bridge-utils ebtables dnsmasq libosinfo-l10n \
  qemu libvirt-daemon-system \
  qemu-kvm virt-manager   # … libvirt0 libspice-server1 virtinst virt-viewer
  ```


+ **spice client** _« embedding the SPICE display_  
  `gir1.2-spiceclientgtk-3.0` `spice-client-gtk` _« remote "local" client_


+ **spice qxl guest drivers** _« video device driver QXL \(2D\), newer VirtIO \(3D\) rendering <sup>ob¬ing</sup>_  
  `xserver-xorg-video-qxl` _« guest \(performance\)_


+ **spice agent** _« mouse hand-over, copy 'n' paste, video adaption and resizing_  
  `spice-vdagent` _« guest \(extensions\)_


+ **groupmod** _« user linux,hu_  
  /etc/group
  
  ```
  …
  kvm:x:129:
  rdma:x:130:
  libvirt:x:131:linux,hu
  libvirt-qemu:x:64055:libvirt-qemu
  libvirt-dnsmasq:x:132:
  ```


### audio (no pulseaudio but spice)

+ **spice requirement:**  
  host input audio device \(figure HDMI\/DP dues input\) pegel independent  
  USB audio device or **any LINE-IN plug** -- spice **quick and dirty** ,vnc otherwise  
  or ALSA virtual device .. "snd-aloop snd-dummy modprobe" ... \/etc\/modules  
  or "pacmd load-module module-virtual-source source_name=loop_source uplink_sink=loop_sink"


### Windows guest extensions

+ **VirtIO drivers**  
  [ :arrow_up_small: https://www.linux-kvm.org/page/WindowsGuestDrivers/Download_Drivers ][winguestdrv1]  
  [ :arrow_up_small: https://docs.fedoraproject.org/en-US/quick-docs/creating-windows-virtual-machines-using-virtio-drivers/ ][winguestdrv2]


[winguestdrv1]: https://www.linux-kvm.org/page/WindowsGuestDrivers/Download_Drivers
[winguestdrv2]: https://docs.fedoraproject.org/en-US/quick-docs/creating-windows-virtual-machines-using-virtio-drivers/

![winsetup](https://www.rollator-parcours.com/de/HOWTO/KVM/Windows10-für-iTunes/img/Bildschirmfoto_vom_2019-01-10_18-42-58.png)

![winready](https://www.rollator-parcours.com/de/HOWTO/KVM/Windows10-für-iTunes/img/Bildschirmfoto_vom_2019-01-10_19-30-28.jpg)


### Fernzugriff auf Windows 10

+ **Remote desktop connection**  
  remote access with **xrdp** or **FreeRDP** having Desktop-as-a-Service [ <sup><sup>ct</sup> 2019-02-144</sup> ](https://ct.de/yc3h)