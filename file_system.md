<code>
chuck@atombomb:~$ cat /etc/fstab
</code>
<pre>
# /etc/fstab: static file system information.
#
# Use 'blkid -o value -s UUID' to print the universally unique identifier
# for a device; this may be used with UUID= as a more robust way to name
# devices that works even if disks are added and removed. See fstab(5).
#
# <file system> <mount point>   <type>  <options>       <dump>  <pass>
proc            /proc           proc    nodev,noexec,nosuid 0       0
/dev/sda1       /               ext4    errors=remount-ro 0       1
# swap was on /dev/sda5 during installation
UUID=06192c5d-6e46-48a1-b649-0bf8b8128fc3 none            swap    sw              0       0

#/dev/sdb1 /media/download ext4 defaults 0 3
#/dev/lvm-raid/lvm0 /media/media ext4 defaults 0 3
#/dev/sdd1 /media/backup ext4 noatime,data=writeback 0 3

/dev/sdb1 /media/media ext4 noatime,data=writeback 0 3
/dev/sdc1 /media/files ext4 noatime,data=writeback 0 3
/dev/sde1 /media/download ext4 noatime,data=writeback 0 3
</pre>

<code>
chuck@atombomb:~$ sudo lshw -C disk
</code>

<pre>
cription: ATA Disk
       product: WDC WD1600BEVE-0
       vendor: Western Digital
       physical id: 0.0.0
       bus info: scsi@0:0.0.0
       logical name: /dev/sda
       version: 01.0
       serial: WD-WXC908809687
       size: 149GiB (160GB)
       capabilities: partitioned partitioned:dos
       configuration: ansiversion=5 signature=000a30ef
  *-disk:0
       description: ATA Disk
       product: WDC WD30EZRX-00M
       vendor: Western Digital
       physical id: 0
       bus info: scsi@2:0.0.0
       logical name: /dev/sdb
       version: 80.0
       serial: WD-WCAWZ0727148
       size: 2794GiB (3TB)
       capabilities: gpt-1.00 partitioned partitioned:gpt
       configuration: ansiversion=5 guid=df748c5d-95b6-4bfe-9937-12f05766a78c
  *-disk:1
       description: ATA Disk
       product: WDC WD10EADS-00L
       vendor: Western Digital
       physical id: 1
       bus info: scsi@2:0.1.0
       logical name: /dev/sdc
       version: 01.0
       serial: WD-WCAU45941085
       size: 931GiB (1TB)
       capabilities: partitioned partitioned:dos
       configuration: ansiversion=5 signature=000b36db
  *-disk:2
       description: ATA Disk
       product: WDC WD30EFRX-68A
       vendor: Western Digital
       physical id: 2
       bus info: scsi@3:0.0.0
       logical name: /dev/sdd
       version: 80.0
       serial: WD-WCC1T1044811
       size: 2794GiB (3TB)
       configuration: ansiversion=5
  *-disk:3
       description: ATA Disk
       product: WDC WD20EARS-00S
       vendor: Western Digital
       physical id: 3
       bus info: scsi@3:0.1.0
       logical name: /dev/sde
       version: 80.0
       serial: WD-WCAVY2657430
       size: 1863GiB (2TB)
       capabilities: partitioned partitioned:dos
       configuration: ansiversion=5 signature=3bda2f9f
</pre>

<code>
sudo fdisk /dev/sdd
</code>

<code>
sudo mkfs.ext4 /dev/sdd1
</code>

<code>
sudo tune2fs -m 0 /dev/sdd1
</code>
