# Raid 1

This guide explains how to install and configure RAID 1 using mdadm on Ubuntu Linux. RAID 1 mirrors data across two disks for redundancy and fault tolerance.

🧪 Test RAID 1 Functionality
Create Test File
```bash
echo "Raid 1 Working" | sudo tee /mnt/raid1/test.txt
```
Read Test File
```bash
cat /mnt/raid1/test.txt
```
Simulate Disk Failure
```bash
sudo mdadm --manage /dev/md1 --fail /dev/sdc
```
Check RAID After Failure
```bash
cat /proc/mdstat
```
Verify Data Still Exists
```bash
cat /mnt/raid1/test.txt
```
Remove Failed Disk
```bash
sudo mdadm --manage /dev/md1 --remove /dev/sdc
```
Re-add Disk to RAID
```bash
sudo mdadm --manage /dev/md1 --add /dev/sdc
```
Final RAID check
```bash
sudo mdadm --detail /dev/md1
```
