# Logical volume manager

## to see partition
/proc/partitions

## volume group
abstraction of all storage
put the different disk in volume group

## logical volume
multiple logical lv 

## snapshot

## thin provisioning
specially used for docker . Allowed to grow 

## commands for creating fresh
> Initialze pv
```
pvcreate /dev/sdc
```
> verify pv
```
pvs # physical volumes or pvdisplay
```
> create vg 
```
vgcreate vgdata /dev/sdz
```
> verify vg
```
vgs
```
> Create logical volume
```
lvcreate -n lvdata -L 1G vgdata
```
>verify lv
```
lvs
```
> Create file system
```
mkfs
```

## Snapshots
snapshot keep current state of logical volume. Used for backup the volume.

## when to run partprobe
when you have one partition in linux and another in lvm
partprobe /dev/sdc

## check we have sufficient disk space
fdisk -l /dev/sdc


## ext4 file system
mkfs.ext4
tune2fs
resize2fs
e2fsck .. and many more

## xfs file system
mkfs.xfs
xfs_admin
xfs_freeze
xfs_copy
xfs_growfs


