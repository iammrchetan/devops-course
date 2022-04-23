# Linux

## Directory Structure

![Linux Directory Structure](../images/Linux-Directory-Structure.jpeg)

* **/bin** : All the executable binary programs (file) required during booting, repairing, files required to run into single-user-mode, and other important, basic commands viz., cat, du, df, tar, rpm, wc, history, etc.
* **/boot** : Holds important files during boot-up process, including Linux Kernel.
* **/dev** : Contains device files for all the hardware devices on the machine e.g., cdrom, cpu, etc
* **/etc** : Contains Application’s configuration files, startup, shutdown, start, stop script for every individual program.
* **/home** : Home directory of the users. Every time a new user is created, a directory in the name of user is created within home directory which contains other directories like Desktop, Downloads, Documents, etc.
* **/lib** : The Lib directory contains kernel modules and shared library images required to boot the system and run commands in root file system.
* **/lost+found** : This Directory is installed during installation of Linux, useful for recovering files which may be broken due to unexpected shut-down.
* **/media** : Temporary mount directory is created for removable devices viz., media/cdrom.
* **/mnt** : Temporary mount directory for mounting file system.
* **/opt** : Optional is abbreviated as opt. Contains third party application software. Viz., Java, etc.
* **/proc** : A virtual and pseudo file-system which contains information about running process with a particular Process-id aka pid.
* **/root** : This is the home directory of root user and should never be confused with ‘/‘
* **/run** : This directory is the only clean solution for early-runtime-dir problem. This keeps the data for the runtime environment such as information for the running process. This data is all volatile.
* **/sbin** : Contains binary executable programs, required by System Administrator, for Maintenance. Viz., iptables, fdisk, ifconfig, swapon, reboot, etc.
* **/srv** : Service is abbreviated as ‘srv‘. This directory contains server specific and service related files, such as data and scripts for web servers, data offered by FTP servers, and repositories for version control systems (appeared in FHS-2.3 in 2004).
* **/sys** : Modern Linux distributions include a /sys directory as a virtual filesystem, which stores and allows modification of the devices connected to the system.
* **/tmp** :System’s Temporary Directory, Accessible by users and root. Stores temporary files for user and system, till next boot.
* **/usr** : Contains executable binaries, documentation, source code, libraries for second level program.
* **/var** : Stands for variable. The contents of this file is expected to grow. This directory contains log, lock, spool, mail and temp files.

## Some important good to know files
* **Linux Kernel File:**
	* **/boot/vmlinux** – The Linux kernel file.
* **Device Files:**
	* **/dev/hda** – Device file for the first IDE HDD.
	* **/dev/hdc** – A pseudo-device that output garbage output is redirected to /dev/null.  

## System Configuration Files:
* **/etc/bashrc** – It is used by bash shell that contains system defaults and aliases.
* **/etc/crontab** – A shell script to run specified commands on a predefined time interval.
* **/etc/exports** – It contains information on the file system available on the network.
* **/etc/fstab** – Information of the Disk Drive and their mount point.
* **/etc/group** – It is a text file to define Information of Security Group.
* **/etc/grub.conf** – It is the grub bootloader configuration file.
* **/etc/init.d* – Service startup Script.
* **/etc/lilo.conf** – It contains lilo bootloader configuration file.
* **/etc/hosts** – Information of IP and corresponding hostnames.
* **/etc/hosts.allow** – It contains a list of hosts allowed accessing services on the local machine.
* **/etc/host.deny** – List of hosts denied to access services on the local machine.
* **/etc/inittab** – INIT process and their interaction at the various run level.
* **/etc/issue** – Allows editing the pre-login message.
* **/etc/modules.conf** – It contains the configuration files for the system modules.
* **/etc/motd** – It contains the message of the day.
* **/etc/mtab** – Currently mounted blocks information.
* **/etc/passwd** – It contains username, password of the system, users in a shadow file.
* **/etc/printcap** – It contains printer Information.
* **/etc/profile** – Bash shell defaults.
* **/etc/profile.d** –  It contains other scripts like application scripts, executed after login.
* **/etc/rc.d** – It avoids script duplication.
* **/etc/rc.d/init.d** – Run Level Initialisation Script.
* **/etc/resolv.conf** – DNS being used by System.
* **/etc/security** – It contains the name of terminals where root login is possible.
* **/etc/skel** – Script that initiates new user home directory.
* **/etc/termcap** – An ASCII file that defines the behavior of different types of the terminal.
* **/etc/X11** –  Directory tree contains all the conf files for the X-window System.

## Virtual and Pseudo Process Related Files:
* **/proc/cpuinfo** – CPU Information
* **/proc/filesystems** – It keeps the useful info about the processes that are running currently.
* **/proc/interrupts** – it keeps the information about the number of interrupts per IRQ.
* **/proc/ioports** – Contains all the Input and Output addresses used by devices on the server.
* **/proc/meminfo** –  It reports the memory usage information.
* **/proc/modules** – Currently using kernel module.
* **/proc/mount** – Mounted File-system Information.
* **/proc/stat** –  It displays the detailed statistics of the current system.
* **/proc/swaps** –  It contains swap file information.

## Version Information File:
* **/version** – It displays the Linux version information.

## Log Files:
* **/var/log/lastlog – It stores user last login info.
* **/var/log/messages** – It has all the global system messages.
* **/var/log/wtmp** – It keeps a history of login and logout information.  

Next: [Know about linux runlevels](runlevels.md)
