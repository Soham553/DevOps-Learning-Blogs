Linux File System Hierarchy:

- In linux everything is represented as a file, including a hardware program. The files are stored in a directory, and every directory contains a file with a tree structure. That is called the File System Hierarchy.

- Linux uses single rooted, inverted tree-like structure.

- Root Direvtory represents with '/'; it is a top-level directory in Linux.

                                   '/'
                                    |
                                    |
    ---------------------------------------------------------------------
    |       |      |      |      |      |      |     |     |     |      |
    |       |      |      |      |      |      |     |     |     |      |
  /root    /mnt  /home  /media  /bin   /usr  /sbin  /etc  /dev  /opt   /var 


/ :
    
    - The base of the Linux directory is the root. This is the starting point of FSH. Every directory arises from the root directory. It is represented by a forward slash(/).
    - If someone says to look into the slash directory, they refer to the root directory.


/root : 
    - It is the home directory for the root user(superuser).


/bin: User Binaries
    - Contains a binary executable.
    - Common Linux commands you need to use in single-user modes are located under this directory.
    - Commands used by all the users of the system are located here.


/sbin: SystemBinaries
    - Just like /bin, /sbin also contains binary executables.
    - But, the Linux commands located under this directory are typically used by system administrators, for system maintenace purpose.
    - For example: iptables, reboot, fdisk, ifconfig, swapon


/dev: Device Files
    - It contains hardware device files
    - Contains device files.
    - These include terminal devices, USB, or any device attached to the system.
    - For example: /dev/ttyl, /dev/usbmon0


/var: Variable Files
    - The variable data files, such as log files, are located in the /var directory.
    - File contents that tend to grow are located in this directory
    - /var/log :
    - /var/lib :
    - /var/tmp :

/mnt: Mount Directory
    - This directory is used to mount a file system temporarily.

/media: Removable Media Devices
    - The /media directory contains subdirectories where removable media devices inserted into the computer are mounted

/usr: User Binaries
    - The /usr directory contains applications and files used by users, as opposed to applications and files used by the system.

/etc: Configuration files
    - It contains all the configuration files of the server 
    - The core configuration files are stored in the /etc directory. It controls the behavior of an operating system or application.

/boot: Boot Loader Files
    - The /boot directory contains the files needed to boot the system 
    - For example: GRUB boot loader's files 

/opt: Optional Applications
    - The opt directory is used for installing the application software from third-party vendors that are not available in the Linux distribution.

/home: Home Directory
    - It contains the secondary user's home directory

/tmp ; Temporary Files
    - Contains temporary files created by the system and users.
