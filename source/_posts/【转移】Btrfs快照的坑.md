---
title: 【转移】Btrfs快照的坑
date: 2022-12-09 14:16:36
---

**本文写于2022.9.7，转移自原博客**  

今天我安装了一个名叫Iriun Webcam的软件，结果把电脑的音频搞坏了。幸好我有之前的快照，于是我打开Timeshift，点几下就恢复了上次的快照。  

本以为重启就万事大吉了，结果重启后提示/boot无法挂载直接进emergency mode了，更难的是我的USB键盘无法在emergency mode下驱动，自然无法解决问题。  

于是我引导进之前EndeavourOS的安装盘（要的是图形界面），安装Timeshift，恢复了在恢复快照之前的系统。  

问题解决了，但为什么会这样呢？于是我查看了`/etc/fstab`  
```
# Static information about the filesystems.
# See fstab(5) for details.

# <file system> <dir> <type> <options> <dump> <pass>
# /dev/nvme0n1p2 LABEL=arch
UUID=d6e6ab1f-10e2-4819-91f5-34b9b2de88c5	/         	btrfs     	rw,relatime,compress=zstd:3,ssd,space_cache=v2,subvolid=256,subvol=/@	0 0

# /dev/nvme0n1p1
UUID=9B35-3A56      	/boot     	vfat      	rw,relatime,fmask=0022,dmask=0022,codepage=437,iocharset=ascii,shortname=mixed,utf8,errors=remount-ro	0 2

# /dev/nvme0n1p2 LABEL=arch
UUID=d6e6ab1f-10e2-4819-91f5-34b9b2de88c5	/home     	btrfs     	rw,relatime,compress=zstd:3,ssd,space_cache=v2,subvolid=257,subvol=/@home	0 0
```  

看看`# /dev/nvme0n1p1`那行，原来我把efi分区挂载在了`/boot`下，虽然系统正常运行没有问题，但会导致`/boot`目录不会被快照，也就是说，对内核的更改不会被快照！而我恢复那个快照前刚好更新过内核，快照一恢复，不就相当于单独更新内核吗？系统启动不起来是正常现象。  

最后，建议把efi分区挂载在`/efi`或`/boot/efi`下！