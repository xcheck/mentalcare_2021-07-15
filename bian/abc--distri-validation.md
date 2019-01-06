# ISO image validation

### …run the sha1sum program to check against the value in the checksum file

```
sha1sum -c 2017-09-07-raspbian-stretch.zip.sha1
```

### Write a zipped image to the SD card w/ `dd` err ^ound ~~`…conv=fsync`~~

```
unzip -p 2017-09-07-raspbian-stretch.zip | sudo dd of=/dev/sdX bs=4M oflag=direct status=progress
```

### Error scan the image on the SD card w/ `rsync`

>>>
```
sudo dd if=/dev/sdX of=from-sd-card.img bs=1M count=5200 oflag=direct status=progress
sudo truncate from-sd-card.img --reference ubuntu-17.10-desktop-amd64.iso
diff -s from-sd-card.img ubuntu-17.10-desktop-amd64.iso
sync
```
>>>

```
sudo rsync -av --progress ubuntu-17.10-desktop-amd64.iso /dev/sdX
```