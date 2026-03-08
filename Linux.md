Hello everyone, my name is Soham. I am going to share my Linux with you.

Let's start

Firstly, there is lots of confusion about whether Linux is an operating system or a kernel, and the 
correct answer to that is Kernel. 

What is actually the kernel?
     A software program which is designed to communicate with the hardware of the computer. It helps the operating system to      send signals or data do to particular task.
    It includes subsystems that performs taks as assigned.

    > The core subsystems of the Linux Kernel are:
       1. Process Scheduler
       2. Memory Management Unit
       3. Virtual File System
       4. Networking Unit
       5. Inter-Process Communication Unit
This is all about the kernel. Let's move forward

Whenever we talk about linux two names arise with it: UNIX and GNU.

UNIX: It is an operating system designed in 1969, which introduced some fundamental concepts that are still useful now

    > file system hierarchy (/home, /etc)
    > multi-user system
    > multitasking
    > permissions
    > shell commands

Many systems are inspired by Unix:
   
    > Macos
    > Linux

GNU: Richard Stallman in 1983 comes with an agenda to build open source operating system.
They have built:

    > bash shell
    > gcc compiler
    > core utilities (ls, cat, rm, etc.)
    > libraries
    > system tools

Their kernel was not ready. They were facing issues while building the kernel names Hurd.

Then Linus Toravalds comes in picture in 1991 Linus published his kernel with an open source license, free for anyone.
Because of open source stallman collaborated with the Linux kernel and made GNU/Linux. Many Operating systems, like Ubuntu and debian family is based on GNU/Linux.

A question arises in your mind, what is actualy Ubuntu and debian are? 

Let's understand:

As you know, Linux is a kernel which is comunicator between hardaware and software(OS).
There are dozens of Operating System based on the Linux kernel. Linux based operating systems are called linux flavours or Distro or Families.

![Linux Distro](images/image.png)

Three popular Distros are:
    
    > Debian: It is maintained by Canonical
    > Read Hat Enterprices Linux(RHEL): Maintened by RedHat.
    > Suse Linux Enterprices: Maintened by SUSE. 

These distros are built on the 3 factors:
    1. Liux kernel
    2. Package Management System: 
       > Debian: The file extension in Debian is .deb, and the package manager is apt
       > Red Hat: Uses .rpm file extension and yum/dnf package manager.
       > SUSE: Uses .rpm file extension and zypper package manager.
    3. Init System:
       > Systemd
       > init
       > upstart(loader)

Each Linux distribution is built special Purpose:

        | ------ | ----------------------- | ---------------------- |
        | Debian | Stability + foundation  | Servers, base OS       |
        | Ubuntu | Ease + modern ecosystem | Cloud, DevOps, desktop |
        | RHEL   | Enterprise reliability  | Corporate production   |
        | SUSE   | Enterprise management   | SAP, enterprise infra  |

As you can see in the image, Operating Systems that have been derived from distros.
 
      > Ubuntu -> Debian
      > Fedora -> RHEL
      > SUSE   -> SUSE Linux Enterprises 

As of now, we have seen what Linux is and linux based operating system. 


