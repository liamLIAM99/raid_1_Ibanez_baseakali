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
