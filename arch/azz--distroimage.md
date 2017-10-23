# Linux ^®oller — Annoyances-by-Design

### Iso image validation

##### …run the sha1sum program to check against the value in the checksum file
```
sha1sum -c 2017-09-07-raspbian-stretch.zip.sha1
```

##### Write a zipped image to the SD card w/ `dd` w/o conv=fsync
```
unzip -p 2017-09-07-raspbian-stretch.zip | sudo dd of=/dev/sdX bs=4M oflag=direct status=progress
```

##### Error scan the image on the SD card w/ `rsync`
> ```
sudo dd if=/dev/sdX of=from-sd-card.img bs=1M count=5200 oflag=direct status=progress
sudo truncate from-sd-card.img --reference ubuntu-17.10-desktop-amd64.iso
diff -s from-sd-card.img ubuntu-17.10-desktop-amd64.iso
sync
```

```
sudo rsync -av --progress ubuntu-17.10-desktop-amd64.iso /dev/sdX
```

### Linux install respin

##### Raspbian blank on 16G

Default login: [pi / raspberry](https://downloads.raspberrypi.org/raspbian/images/)

**µSD Card l ^only partitioning**
 > ```
(parted) print                                                            
Model: Generic- USB3.0 CRW -SD (scsi)
Disk /dev/sde: 15931539456B
Sector size (logical/physical): 512B/512B
Partition Table: msdos
Disk Flags: 
…
Number  Start         End           Size          Type     File system  Flags
 1      4194304B      48033279B     43838976B     primary  fat32        lba
 2      48234496B     11811160063B  11762925568B  primary  ext4
 3      11811160064B  15931539455B  4120379392B   primary
```

```
parted help resizepart NUM END
```

```
e2fsck -fv /dev/sdX2
resize2fs -p /dev/sdX2
```

**/boot/cmdline.txt**
```
root=/dev/mmcblk0p2
```