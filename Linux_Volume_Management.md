What Volume management?

When we creat instance EC2 for an example on AWS, we get min 8Gb internel volume. 
We can add or extend volume of a instance using EBS.

EBS stands for Elastic Block Store.

Elastic: Give use elaticity we can decide size of volume as per our use.
Block: Block of storage.

There is alwayes one block of storage/volume with instance.
     -lsblk: List block use to list blocks 
            lsblk
        NAME            MAJ:MIN RM  SIZE RO TYPE MOUNTPOINTS
        loop0             7:0    0 27.8M  1 loop /snap/amazon-ssm-agent/12322
        loop1             7:1    0 50.9M  1 loop /snap/snapd/25577
        loop2             7:2    0 27.6M  1 loop /snap/amazon-ssm-agent/11797
        loop3             7:3    0   74M  1 loop /snap/core22/2163
        loop4             7:4    0 48.1M  1 loop /snap/snapd/25935
        nvme0n1         259:0    0   20G  0 disk
        ├─nvme0n1p1     259:4    0   19G  0 part /
        ├─nvme0n1p14    259:5    0    4M  0 part
        ├─nvme0n1p15    259:6    0  106M  0 part /boot/efi
        └─nvme0n1p16    259:7    0  913M  0 part /boot
        nvme2n1         259:1    0   12G  0 disk
        └─tws_vg-tws_lv 252:0    0   10G  0 lvm
        nvme3n1         259:2    0   14G  0 disk
        nvme1n1         259:3    0   10G  0 disk

    -df -h: Use to list free disk space and mount points

    root@ip-172-31-38-27:/# df -h
    Filesystem       Size  Used Avail Use% Mounted on
    /dev/root         19G  2.4G   16G  13% /
    tmpfs            456M     0  456M   0% /dev/shm
    tmpfs            183M  928K  182M   1% /run
    tmpfs            5.0M     0  5.0M   0% /run/lock
    efivarfs         128K  4.7K  119K   4% /sys/firmware/efi/efivars
    /dev/nvme0n1p16  881M  156M  663M  20% /boot
    /dev/nvme0n1p15  105M  6.2M   99M   6% /boot/efi
    tmpfs             92M   12K   92M   1% /run/user/1000
    root@ip-172-31-38-27:/#

- We have to create volume and then need to attach and then have to mount with instance

1. Create volume 
2. Attach it with instance.
3. Mount it in root directory.

-we can access that memory block only if it is mounted.

- There are three tecnical state volumes in linux
   1. Physical volume
   2. Volume Group
   3. Logical Volumes

Logical Volume Manager: a tool use to handle all the operations telated to the volume management.

1. Physical Volume: when we create EBS as follow in EC2 instance 
          
          Elastic Block Store(Section) -> Volumes -> Create Volume -> Attach it to instance 
    
    then the volume is called Physical volume.
    After attaching we can see list of volumes using:
    ~$ lsblk or
    ~$ df -h
    ~$ pv display

2. Volume Group: 
    - When we combine two or more physical volume togater then it is called as a volume group.
    - We can create group using following commands.
    - ~$ vgcreate gr_name path_to_pv1 path_to_pv2   (PV-Physical volume)
    - We can list volume groups using
       ~$ vg or
       ~$ vg display

3. Logical Volume:
    - Initializing small portion of volume group for a particular process is called logical volume.
    - We can initialize logical volume(LV) using following command.

    - "~$ lvcreate -L size_of_lv -n name_of_lv name_of_group"

    - To list the Logical Volume:
        ~$ lv display

- Heirarchi looks as fall
           
              Physical Volume(PV) 1-
                                    |                         -----> Logical Volume 1
              Physical Volume(PV) 2-                         |
                                    | -----> Volume Group --- 
              Physical Volume(PV) 3-                         |
                                    |                         ------> Logical Volume 2
              Physical Volume(PV) 4- 
              

