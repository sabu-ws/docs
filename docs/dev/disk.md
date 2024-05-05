# Manage disk

```
1) Add disk
- Shutdown your VM
- Add disk on your VM
- Start the VM


2) Partition
fdisk /dev/sdb

key: n (new)
key: p (partition)
key: enter x3 (part number, first sector, last sector)

key: w (write)


3) Format
mkfs.ext4 /dev/sdb1


4) Mount
# SABU MOUNT DATA DISK
/dev/sdb1       /data   ext4    defaults        0       2
```