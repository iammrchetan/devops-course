# Runlevels in Linux OS
A run level is a state of init and the whole system that defines what system services are operating. Run levels are identified by numbers. Some system administrators use run levels to define which subsystems are working, e.g., whether X is running, whether the network is operational, and so on.  
1. Whenever a LINUX system boots, firstly the init process is started which is actually responsible for running other start scripts which mainly involves initialization of you hardware, bringing up the network, starting the graphical interface.
2. Now, the init first finds the default runlevel of the system so that it could run the start scripts corresponding to the default run level.
3. A runlevel can simply be thought of as the state your system enters like if a system is in a single-user mode it will have a runlevel 1 while if the system is in a multi-user mode it will have a runlevel 5.
4. A runlevel in other words can be defined as a preset single digit integer for defining the operating state of your LINUX or UNIX-based operating system. Each runlevel designates a different system configuration and allows access to different combination of processes.

#### Linux system supports 7 different runlevels denoted by single digit 0 - 6
1. 0 – System halt i.e the system can be safely powered off with no activity.
2. 1 – Single user mode.
3. 2 – Multiple user mode with no NFS(network file system).
4. 3 – Multiple user mode under the command line interface and not under the graphical user interface.
5. 4 – User-definable.
6. 5 – Multiple user mode under GUI (graphical user interface) and this is the standard runlevel for most of the LINUX based systems.
7. 6 – Reboot which is used to restart the system.

## What are these files which OS uses to run program for specified runlevels.
On Ubuntu system, this is what you see under */etc/*. Go to under these directories and see the programs.
```
drwxr-xr-x   2 root root    4096 Dec 15 16:33 rc0.d/
drwxr-xr-x   2 root root    4096 Dec 15 16:33 rc1.d/
drwxr-xr-x   2 root root    4096 Dec 15 16:33 rc2.d/
drwxr-xr-x   2 root root    4096 Dec 15 16:33 rc3.d/
drwxr-xr-x   2 root root    4096 Dec 15 16:33 rc4.d/
drwxr-xr-x   2 root root    4096 Dec 15 16:33 rc5.d/
drwxr-xr-x   2 root root    4096 Dec 15 16:33 rc6.d/
drwxr-xr-x   2 root root    4096 Nov 24 13:05 rcS.d/
```

## How do I know which runlevel is currently my server in?
```chetan@99devops:/run$ runlevel 
N 5
```

## How can I change my system to go into a particular **runlevel**
```
[chetan.sharma@npl9dba08 ~]$ telinit --help
telinit [OPTIONS...] {COMMAND}

Send control commands to the init daemon.

     --help      Show this help
     --no-wall   Don't send wall message before halt/power-off/reboot

Commands:
  0              Power-off the machine
  6              Reboot the machine
  2, 3, 4, 5     Start runlevelX.target unit
  1, s, S        Enter rescue mode
  q, Q           Reload init daemon configuration
  u, U           Reexecute init daemon
```

Previous: [Know about Linux directory structure](directory-structure.md)
