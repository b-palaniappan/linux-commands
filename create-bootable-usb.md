## Create Bootable USB using ISO image file
- list block devices `lsblk` to identify the `sd*` name
- Format USB using `sudo mkfs.vfat /dev/sdb -I`
- Use dd command to create bootable USB.
```
sudo dd bs=4M if=debian-10.10.0-amd64-netinst.iso of=/dev/sdb status=progress oflag=sync
```
Breakdown of `dd` command,
  - `bs=4M`: Specify that a 4 MB block size should be used
  - `if=debian-10.10.0-amd64-netinst.iso`: Input file we want to copy
  - `of=/dev/sdb`: Output file (device) that we want to write to
  - `status=progress`: Show the progress of the dd command
  - `oflag=sync`: Sync after each output block. This can slow down our write time to our device, but it ensures that all data gets effectively “synced” to our USB device as it’s being written.

### Using MacOS
- Format the USB drive as FAT using Disk Util UI.
- List removable devices `diskutil list` in macos terminal
- Unmount the USB using `diskutil unmountDisk disk4`
- Use `dd` command to create bootable USB,
```bash
sudo dd bs=4M if=Fedora-Workstation-Live-x86_64-39-1.5.iso of=/dev/disk4 status=progress oflag=sync
```
