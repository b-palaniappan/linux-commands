# Mount disk
- Run `lsblk` command to get list of disk on the computer.
- Get block id for the disk.
```bash
$ sudo blkid /dev/sdb
/dev/sdb: UUID="3853c036-b6bc-4b33-a211-3605c66df6bb" BLOCK_SIZE="4096" TYPE="ext4"
```
- Get Unique ID to add to `/etc/fstab` file.
```bash
# External drives
UUID=5617389a-7cb3-4db7-9d22-c8c6aa08ad5f /mnt/disk1 ext4 errors=remount-ro 0 3
UUID=8c6c87bb-4bb6-49f9-80b9-e450f5bafd94 /mnt/disk2 ext4 errors=remount-ro 0 4
```
**Note** : the last(sixth) param will be last number +1.
**PS** Steps [here](https://www.debiantutorials.com/how-to-add-a-new-hard-disk-or-partition-using-uuid-and-ext4-filesystem/)
