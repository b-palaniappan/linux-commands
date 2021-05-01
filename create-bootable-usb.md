## Create Bootable USB drive using dd command

#### Format USB drive
* Get list of all drives - `sudo fdisk -l`
* Unmount - `sudo unmount /dev/sdb`
* Format USB - `sudo  mkfs.ext4  /dev/sdb`
* Create bootable USB from iso image - `dd bs=4M if=debian-64-bit.iso of=/dev/sdb status=progress oflag=sync`
