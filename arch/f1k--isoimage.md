# Iso image validation

### …run the sha1sum program to check against the value in the checksum file
```
sha1sum -c 2017-09-07-raspbian-stretch.zip.sha1
```

### Write a zipped image to the SD card
```
unzip -p 2017-09-07-raspbian-stretch.zip | sudo dd of=/dev/sdX bs=4M status=progress conv=fsync
```

### Error scan the image on the SD card
```
sudo dd if=/dev/sdd of=from-sd-card.img bs=1M count=1500 conv=fsync status=progress
sudo truncate from-sd-card.img --reference ubuntu-17.10-desktop-amd64.iso
diff -s from-sd-card.img ubuntu-17.10-desktop-amd64.iso
sync
```