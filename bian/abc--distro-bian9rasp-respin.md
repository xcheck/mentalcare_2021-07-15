# Annoyances-by-Design – Linux ^®oller – tweak Raspbian (respin draft in work)

### draft autoscript

**initScript ^todo — …check pi placement then append ,`whoami`**
```
sed -e "s/:pi.*$/&,`whoami`/g" /etc/group-

DEST_USER=`whoami`
ETC_GROUP="/etc/group-"
if ! fgrep -q ${DEST_USER} ${ETC_GROUP}; then
    sed -e "s/:pi.*$/&,${DEST_USER}/g" ${ETC_GROUP}
fi
```


:chains:

# wear levelling – keep trim space µSD side

**µSD Card l ^only partitioning on 16G**

>>>
```
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
>>>

```
parted help resizepart NUM END
```

```
e2fsck -fv /dev/sdX2
resize2fs -p /dev/sdX2
```


:chains:

# boot from usb mass storage device

**/boot/cmdline.txt**

```
root=/dev/mmcblk0p2
```

**/etc/fstab**

```
proc            /proc           proc    defaults          0       0
/dev/mmcblk0p1  /boot           vfat    defaults          0       2
#PARTUUID=bfed2868-01  /boot           vfat    defaults          0       2
/dev/mmcblk0p2  /               ext4    defaults,noatime  0       1
#PARTUUID=bfed2868-02  /               ext4    defaults,noatime  0       1
# a swapfile is not a swap partition, no line here
#   use  dphys-swapfile swap[on|off]  for that
```