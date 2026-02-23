Linux for DevOps may you thing why linux? and why not windows? 
Then the answer is:

    1. Linux provides high stability:
          > Linux uses a monolithic kernel (where the kernel handles all OS functions).
          > Separation of User and Kernel Space.
          > File Permissions and Security(user, group, permissions).
          > Long-Term Support (LTS) supports for 5-10 years.
    2. Virtualization & Hypervisors
    3. Cloud Provider Adoption

There are famous to quotes or the statments about linux:
    > "Everything in the linux is either a file or a directory(folder)".
    > "Everything starts with a process".

At the end you will understand the meaning of these two statments:

There are two forms of linux based operating system:
     > Linux server Distribution (Choose for hosting websites, database management, file storage).
     > Linux Dekstop Distribution (Choose for personal computing, web browsing).

       1. Linux server Distributions: 
            - Removes GUI prioritize security, stability, and efficiency.
            - Uses command line interface(CLI).
            - Focuses on baground processes
            - Ex. Ubuntu server, RHEL.

       2. Linux Dekstop Distribution:
            - uses Graphical User Interface(GUI)
            - Focus on responsiveness for interactive user tasks.
            - Ex. Ubuntu Dekstop, Fedora.

For each distribution they have installers in both forms server as well as dekstop.
        ubuntu server and Dekstop: "https://ubuntu.com/download/alternative-downloads"
        (you can find other installers for fedora workstation, REDHAT)
        

To install ubuntu follow the guid: 
         "https://ubuntu.com/tutorials/install-ubuntu-server#1-overview"

What does installer do:
 - The BIOS or UEFI firmware initializes hardware and loads the installer from bootable media, and the installer then partitions 
   the disk, copies OS files, and installs a bootloader to make the system bootable.

Now let's Understand linux boot process:

1. When power On button pressed hardware wakes up.
2. BIOS(Basic Input Output System)/ UEFI(Unified Extensible Firmware Interface) firmware starts:
    > It performs POST(POWER ON SELT TEST): 
        - To verify all hardware components are working or not (CPU, RAM, storage, and video card).
        - If components are not working or problems arises in components it will emit a series of beep code.
        - If all okay it will processed for further
    > Bootloader(GRUB): BIOS reads MASTER BOOT LOADER(MBR)/ UEFI uses GPT and laods GRUB.
3. GRUB(Grand Unified Bootloader):
    > It has interface for multiple operating system to load.
    > After clicking on OS it will load the kernel form the hard disk.
4. init process/systemd starts which is the first process having process ID:1.





#Systemd:
     - It is both init system and service manager for most of the linux based systems
     - An init system (short for initialization) is the first program that runs when you turn on your computer. It has the special 
       process ID of 1 and is responsible for starting everything else on your computer.
     - A service manager, on the other hand, handles starting, stopping, and monitoring the programs (called services) that run in 
       the background on your system.
     - It manages everything from hardware devices to network connections, controls when programs run, and even handles system 
       logs
     - systemd bring system into intended state, which is defined by a target like multe-user.target for server
       graphical.target for desktops.

The key components of systemd:
    1. systemctl: 
        - It is command line interface which use to interact with systemd
        - It used to start, stop, enable, disable, and check the status of services and other units.

    2. Journalnd:
        - It is systems memory which is one of systemd’s daemon that serves as the built-in logging system which collects and 
          stores messages from the kernel, services, and applications in a structured format.
        - Journald centralizes everything into a single, searchable database unlike your traditional text-based log files that are 
          scattered throughout your system.
        - systmd has some demones which handles specific aspects of system.
                > timedated: manages your system’s time and date settings
                > logind: handles user logins and sessions.
                > Networkd: provided network configuration capabilities
                                
    3. Journalctl:
        - The logs that were collected and stored in journald can be accessed using the journalctl 
          command.  
        - 

    4. Unites file:
        - At its core, systemd organizes everything as “units” which are represented by simple text files with a specific 
          extension.   
        - Unit files are configuration files that tell systemd how to manage different resources like services, sockets, mounts, 
          and timers.  
        - Types of Unit files:
            1. Service Units (.service)  
            2. Target Units (.target)
            3. Socket Units (.socket)
            4. Mount Units (.mount)
            5. Timer Units (.timer)                   
   
