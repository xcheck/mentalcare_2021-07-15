# KVM kernel-based virtual machine

### kvm server

qemu-kvm   # `exec qemu-system-x86_64 -enable-kvm "$@"`

```
apt install qemu [qemu-kvm] virt-manager
```


_**spice # VM-Video: QXL (2D) new VirtIO (3D) rendering**_
_**spice   # guest video screen resizing ^ob¬ing**_
apt install spice-client-gtk
apt install spice-vdagent


_**kernel-based modul kvm   # requirements**_

$ lsmod | grep kvm   # (Debian9)

´´´
kvm_intel             192512  0
kvm                   589824  1 kvm_intel
irqbypass              16384  1 kvm
´´´


_**groupmod**_

/etc/group   # add user

```
pi:x:1000:libvirt-qemu
	libvirt:x:128:pi
	libvirt-qemu:x:64055:libvirt-qemu,pi
```



### audio w/ not-pa-but.spice

+	spice requirement: host input audio device (figure HDMI/DP dues input) pegel independent
	USB audio device or any LINE-IN plug -- spice quick and dirty ,vnc otherwise
	or ALSA virtual device .. "snd-aloop snd-dummy modprobe" ... /etc/modules
	or "pacmd load-module module-virtual-source source_name=loop_source uplink_sink=loop_sink"

