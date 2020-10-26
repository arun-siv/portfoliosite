# Logical volume manager

## volume group
abstraction of all storage
put the different disk in volume group

## logical volume
multiple logical lv 


## snapshot

## thin provisioning
specially used for docker . Allowed to grow 

## commands
> Initialze pv
```
pvcreate /dev/sdc
```
> verify pv
```
pvs
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