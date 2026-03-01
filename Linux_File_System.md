Linux File System Hierachy:

- In linux everything is represented as a file including a hardware program, the files are stored in a dirctoru, and every directory contains a file with a tree structure. That is called File System Hietatchy.

- Linux uses single rooted, inverted tree-like structure.

- Root Direvtory represents with '/' it is a top-level directory in Linux.

                                   '/'
                                    |
                                    |
    ---------------------------------------------------------------------
    |       |      |      |      |      |      |     |     |     |      |
    |       |      |      |      |      |      |     |     |     |      |
  /root    /mnt  /home  /media  /bin   /usr  /sbin  /etc  /dev  /opt   /var 


/ :
    
    - The base of the linux directory is the root. This is the starting point of FSH. Every directory arises from the root directory. It is represented by a forward slash(/).
    - If someone says to look into the slash directory, they refer to the root directory.


/root : 
    - It is the home directory for the root user(superuser).


/bin : User Binaries
    - Contains binary executable.
    - Common Linux commands you need to use in single user modes are located under this directory.
    - Commands used by all the users of the system are located here.


/sbin : SystemBinaries
    - Just like /bin, /sbin also contains binary executables.
    - But, the linux commands located under this directory are used typically by system administrator, for system maintenace purpose.
    - For example: iptables, reboot, fdisk, ifconfig, swapon


/dev : Device Files
    - It conatins hardware device files
    - Conatins device files.
    - These include terminal devices, usb, or any device attached to the system.
    - For example: /dev/ttyl, /dev/usbmon0



