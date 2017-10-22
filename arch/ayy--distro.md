# Linux install respin

### Raspbian blank on 16G

**µSD Card l ^only partitioning**
 > ```
(parted) print                                                            
Model: Generic- USB3.0 CRW -SD (scsi)
Disk /dev/sde: 15931539456B
Sector size (logical/physical): 512B/512B
Partition Table: msdos
Disk Flags: 
⋮
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