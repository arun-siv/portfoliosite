## how to partition device

### Attach the device 
az command

### see if it reflects
sudo cat /proc/partitions
sudo fdisk /dev/sdc

p (print)
n (new partition)
1 ( new partition number )
first sector ( default)
last sector : +500M ## give the size 

#### Check again before writing
p (print)
Write the partition
w (write)

#### Create the filesystem
sudo mkfs.ext4 /dev/sdc1

#### Mount data
sudo mkdir newdata
sudo mount /dev/sdc1 /newdata
