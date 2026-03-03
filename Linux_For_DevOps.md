Linux for DevOps, may you think why Linux? And why not Windows? 
Then the answer is:

    1. Linux provides high stability:
          > Linux uses a monolithic kernel (where the kernel handles all OS functions).
          > Separation of User and Kernel Space.
          > File Permissions and Security(user, group, permissions).
          > Long-Term Support (LTS) supports for 5-10 years.
    2. Virtualization & Hypervisors
    3. Cloud Provider Adoption

There are famous quotes or the statments about Linux:
    > "Everything in the linux is either a file or a directory(folder)".
    > "Everything starts with a process".

At the end, you will understand the meaning of these two statements:

There are two forms of Linux-based operating systems:
     > Linux server Distribution (Choose for hosting websites, database management, file storage).
     > Linux Dekstop Distribution (Choose for personal computing, web browsing).

       1. Linux server Distributions: 
            - Removes GUI, prioritizes security, stability, and efficiency.
            - Uses command line interface(CLI).
            - Focuses on background processes
            - Ex. Ubuntu server, RHEL.

       2. Linux Dekstop Distribution:
            - uses Graphical User Interface(GUI)
            - Focus on responsiveness for interactive user tasks.
            - Ex. Ubuntu Dekstop, Fedora.

For each distribution, they have installers in both forms server as well as dekstop.
        Ubuntu Server and Desktop: "https://ubuntu.com/download/alternative-downloads"
        (You can find other installers for Fedora Workstation, Red Hat)
        

To install ubuntu follow the guide: 
         "https://ubuntu.com/tutorials/install-ubuntu-server#1-overview"

What does an installer do:
 - The BIOS or UEFI firmware initializes hardware and loads the installer from bootable media, and the installer then partitions 
   The disk copies OS files and installs a bootloader to make the system bootable.

Now let's Understand linux boot process:

1. When power On button is pressed hardware wakes up.
2. BIOS(Basic Input Output System)/ UEFI(Unified Extensible Firmware Interface) firmware starts:
    > It performs POST(POWER ON SELT TEST): 
        - To verify all hardware components are working or not (CPU, RAM, storage, and video card).
        - If components are not working or problems arise in components, it will emit a series of beep codes.
        - If all is okay, it will be processed for further
    > Bootloader(GRUB): BIOS reads MASTER BOOT LOADER(MBR)/ UEFI uses GPT and laods GRUB.
3. GRUB(Grand Unified Bootloader):
    > It has an interface for multiple operating systems to load.
    > After clicking on OS, it will load the kernel from the hard disk.
4. init process/systemd starts, which is the first process having process ID:1.





#Systemd:
     - It is both an init system and a service manager for most of the Linux-based systems
     - An init system (short for initialization) is the first program that runs when you turn on your computer. It has the special 
       process ID of 1 and is responsible for starting everything else on your computer.
     - A service manager, on the other hand, handles starting, stopping, and monitoring the programs (called services) that run in 
       the background on your system.
     - It manages everything from hardware devices to network connections, controls when programs run, and even handles system 
       logs
     - systemd bring system into the intended state, which is defined by a target like multi-user. target for server
       graphics. target for desktops.

The key components of systemd:
    1. systemctl: 
        - It is command line interface which use to interact with systemd
        - It used to start, stop, enable, disable, and check the status of services and other units.

    2. Journalnd:
        - It is systems memory, which is one of systemd’s daemons that serves as the built-in logging system, which collects and 
          stores messages from the kernel, services, and applications in a structured format.
        - Journald centralizes everything into a single, searchable database, unlike your traditional text-based log files that are 
          scattered throughout your system.
        - The system has some modules that handle specific aspects of the system.
                > timedated: manages your system’s time and date settings
                > logind: handles user logins and sessions.
                > Networkd: provided network configuration capabilities
                                
    3. Journalctl:
        - The logs that were collected and stored in journald can be accessed using the journalctl 
          command.  
        - 

    4. Unites file:
        - At its core, systemd organizes everything as “units,” which are represented by simple text files with a specific 
          extension.   
        - Unit files are configuration files that tell systemd how to manage different resources like services, sockets, mounts, 
          and timers.  
        - Types of Unit files:
            1. Service Units (.service): Defines how to mange a service or application, including how to start, stop, and automatically start it.  
            2. Target Units (.target): Targets ensure that the necessary services and resources are running to achieve a specific operational state.
            3. Socket Units (.socket): Information about sockets which port is used by which service.
            4. Mount Units (.mount): Defines a specific filesystem mount point. These units are named after their mount path
            5. Timer Units (.timer): Defines a service to run after perticular time    

- We will see how to list services               
   
   - systemctl list-units
   - systemctl list-timers
   - systemctl list-sockets
   - systemctl list-units --type=target

- We can create our own Service 


# Journald 

- It is like a Database which stores log of services system live 
- We can access these log using journalctl cmd

     - journalctl -u : It will print all the log 
     - journalctl -n 20: Prints 20 log live
     - sudo journalctl -u <service_name> : prints all the log related to service
    

