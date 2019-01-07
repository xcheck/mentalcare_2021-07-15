# KVM kernel-based virtual machine
### requirements

+ **cpu virt <sup>technology</sup> by intel…**
  
  ```
  cat /etc/os-release; dmesg | grep -i virt; egrep '^flags.*(vmx|svm)' /proc/cpuinfo
  ```


+ **kernel-based modul kvm**  
  $ lsmod | grep kvm _« (Debian9)_
  
  ```
  kvm_intel             192512  0
  kvm                   589824  1 kvm_intel
  irqbypass              16384  1 kvm
  ```


### kvm\/spice server, client, guest

+ **qemu-kvm <sup>exec qemu-system-x86_64 -enable-kvm "$@"</sup>** _« (Mint19.1)_
  
  ```
  apt install [qemu] qemu-kvm virt-manager   # … libvirt0 virtinst
  apt install libosinfo-l10n virt-daemon virt-daemon-system  # … virt-viewer
  apt install ebtables dnsmask
  ```


+ **spice client** _« embedding the SPICE display_  
  `spice-client-gtk` _« remote "local" client_


+ **spice qxl guest drivers** _« video device driver QXL \(2D\), newer VirtIO \(3D\) rendering <sup>ob¬ing</sup>_  
  `xserver-xorg-video-qxl` _« guest_


+ **spice agent** _« mouse hand-over, copy 'n' paste, video adaption and resizing_  
  `spice-vdagent` _« guest \(optional\)_


+ **groupmod   # /etc/group** _« add user_
  
  ```
  pi:x:1000:libvirt-qemu
  libvirt:x:128:pi
  libvirt-qemu:x:64055:libvirt-qemu,pi
  ```


### Windows guest

+ **VirtIO drivers**  
  https://www.linux-kvm.org/page/WindowsGuestDrivers/Download_Drivers  
  https://docs.fedoraproject.org/en-US/quick-docs/creating-windows-virtual-machines-using-virtio-drivers/


### audio (no pulseaudio but spice)

+ **spice requirement:**  
  host input audio device \(figure HDMI\/DP dues input\) pegel independent  
  USB audio device or any LINE-IN plug -- spice quick and dirty ,vnc otherwise  
  or ALSA virtual device .. "snd-aloop snd-dummy modprobe" ... \/etc\/modules  
  or "pacmd load-module module-virtual-source source_name=loop_source uplink_sink=loop_sink"