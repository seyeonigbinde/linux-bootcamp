# Lab 3: Manage Azure disks with the Azure CLI

1. Default Azure disks
2. Azure data disks
3. VM disk types
4. Launch Azure Cloud Shell
5. Create and attach disks
   {
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroupDisk",
   "location": "eastus",
   "managedBy": null,
   "name": "seyeResourceGroupDisk",
   "properties": {
   "provisioningState": "Succeeded"
   },
   "tags": null,
   "type": "Microsoft.Resources/resourceGroups"
   }
   {
   "fqdns": "",
   "id": "/subscriptions/d2653dbd-1995-4aba-8a53-fd1fd943c124/resourceGroups/seyeResourceGroupDisk/providers/Microsoft.Compute/virtualMachines/seyeVM",
   "location": "eastus",
   "macAddress": "00-0D-3A-9C-5B-8D",
   "powerState": "VM running",
   "privateIpAddress": "10.0.0.4",
   "publicIpAddress": "20.119.63.135",
   "resourceGroup": "seyeResourceGroupDisk",
   "zones": ""
   }
6. Prepare data disks
   Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 5.4.0-1063-azure x86_64)

- Documentation: https://help.ubuntu.com
- Management: https://landscape.canonical.com
- Support: https://ubuntu.com/advantage

System information as of Fri Nov 19 10:10:22 UTC 2021

System load: 0.08 Processes: 116
Usage of /: 4.6% of 28.90GB Users logged in: 0
Memory usage: 2% IP address for eth0: 10.0.0.4
Swap usage: 0%

0 updates can be applied immediately.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/\*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

meta-data=/dev/sdc1 isize=512 agcount=4, agsize=8388480 blks
= sectsz=4096 attr=2, projid32bit=1
= crc=1 finobt=1, sparse=0, rmapbt=0, reflink=0
data = bsize=4096 blocks=33553920, imaxpct=25
= sunit=0 swidth=0 blks
naming =version 2 bsize=4096 ascii-ci=0 ftype=1
log =internal log bsize=4096 blocks=16383, version=2
= sectsz=4096 sunit=1 blks, lazy-count=1
realtime =none extsz=4096 blocks=0, rtextents=0

/dev/sda1 29G 1.4G 28G 5% /
/dev/sda15 105M 4.4M 100M 5% /boot/efi
/dev/sdd1 14G 41M 13G 1% /mnt
/dev/sdc1 128G 163M 128G 1% /datadrive

/dev/sda1: LABEL="cloudimg-rootfs" UUID="5d344270-f90f-4c30-a4eb-0ae6d367ab12" TYPE="ext4" PARTUUID="21d9dbee-5c16-4250-b0e2-82c55f360e80"
/dev/sda15: LABEL="UEFI" UUID="89D4-973D" TYPE="vfat" PARTUUID="0d225417-b6c7-47a7-b994-f3ea880a16ef"
/dev/sdd1: UUID="7ef6dced-8054-40b0-8b49-a037dfb74356" TYPE="ext4" PARTUUID="197d37d9-01"
/dev/sda14: PARTUUID="14dc2e34-590e-4419-98aa-a65d5806b0bb"
/dev/sdc1: UUID="b1f59be9-dbe4-47be-9377-ca6dcd62965d" TYPE="xfs" PARTLABEL="xfspart" PARTUUID="a65c2cfe-b095-40bf-b5b4-1c2269792e58"

GNU nano 2.9.3 /etc/fstab

# CLOUD_IMG: This file was created/modified by the Cloud Image build process

UUID=5d344270-f90f-4c30-a4eb-0ae6d367ab12 / ext4 defaults,discard$
UUID=89D4-973D  /boot/efi       vfat    umask=0077      0 1
/dev/disk/cloud/azure_resource-part1    /mnt    auto    defaults,nofail,x-system$

                                  [ Cancelled ]

^G Get Help ^O Write Out ^W Where Is ^K Cut Text ^J Justify ^C Cur Pos
^X Exit ^R Read File ^\ Replace ^U Uncut Text^T To Spell ^\_ Go To Line

7. Take a disk snapshot

### Notes:

Quickstart: Manage Azure disks

- https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-disks

Quickstart for Bash in Azure Cloud Shell

- https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart
