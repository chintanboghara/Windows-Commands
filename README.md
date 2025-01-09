## File and Directory Management

| Command               | Description                                      |
|-----------------------|--------------------------------------------------|
| `dir`                 | List files and directories in the current folder |
| `cd <directory>`      | Change directory                                 |
| `cd ..`               | Move up one directory level                     |
| `mkdir <directory>`   | Create a new directory                          |
| `rmdir <directory>`   | Remove a directory (must be empty)              |
| `del <file>`          | Delete a file                                   |
| `copy <source> <dest>`| Copy a file to another location                 |
| `move <source> <dest>`| Move a file to another location                 |
| `ren <old> <new>`     | Rename a file or directory                      |
| `type <file>`         | Display the contents of a file                  |
| `attrib`              | Display or change file attributes               |
| `tree`                | Display directory structure as a tree           |
| `robocopy <source> <dest>` | Advanced file copying tool                  |
| `mklink <link> <target>` | Create symbolic links (symlinks)             |

## System Information and Management

| Command               | Description                                      |
|-----------------------|--------------------------------------------------|
| `systeminfo`          | Display detailed system information             |
| `hostname`            | Display the computer name                       |
| `ver`                 | Display the Windows version                     |
| `tasklist`            | List all running processes                      |
| `taskkill /PID <id>`  | Terminate a process by its PID                  |
| `taskkill /IM <name>` | Terminate a process by its name                 |
| `shutdown /s`         | Shut down the computer                          |
| `shutdown /r`         | Restart the computer                            |
| `shutdown /l`         | Log off the current user                        |
| `wmic`                | Windows Management Instrumentation Command-line |
| `msinfo32`            | Open System Information GUI                     |
| `sfc /scannow`        | Scan and repair system files                    |
| `chkdsk /f`           | Check and fix disk errors                       |
| `powercfg /energy`    | Generate a power efficiency report              |
| `winsat`              | Run Windows System Assessment Tool              |
| `logman`              | Manage performance monitoring logs              |

## Networking

| Command               | Description                                      |
|-----------------------|--------------------------------------------------|
| `ipconfig`            | Display IP configuration                        |
| `ipconfig /release`   | Release the IP address                          |
| `ipconfig /renew`     | Renew the IP address                            |
| `ping <host>`         | Ping a host to check connectivity               |
| `tracert <host>`      | Trace the route to a host                       |
| `netstat`             | Display network connections                     |
| `nslookup <domain>`   | Look up DNS information for a domain            |
| `arp -a`              | Display the ARP table                           |
| `netsh`               | Configure network settings                      |
| `netstat -ano`        | Display all active connections with PIDs        |
| `route print`         | Display the routing table                       |
| `telnet <host> <port>`| Test connectivity to a specific port            |
| `pathping <host>`     | Combines `ping` and `tracert` functionality     |
| `netsh wlan show profiles` | View saved Wi-Fi profiles                |
| `netsh wlan export profile` | Export Wi-Fi profiles to a file          |

## Disk and Storage Management

| Command               | Description                                      |
|-----------------------|--------------------------------------------------|
| `chkdsk`              | Check and repair disk errors                    |
| `format <drive>`      | Format a disk                                   |
| `diskpart`            | Open the disk partitioning tool                 |
| `defrag`              | Defragment a disk                               |
| `vssadmin list shadows` | List volume shadow copies                    |
| `fsutil`              | File system utility for advanced operations     |
| `bcdedit`             | Edit boot configuration data                    |
| `diskraid`            | Manage RAID configurations                      |
| `storage spaces`      | Manage Storage Spaces (virtual disks)           |

## User and Group Management

| Command               | Description                                      |
|-----------------------|--------------------------------------------------|
| `net user`            | List user accounts                              |
| `net user <username>` | Display information about a user                |
| `net user <username> *`| Change a user's password                       |
| `net localgroup`      | List local groups                               |
| `net localgroup <group> <user> /add` | Add a user to a group          |
| `net localgroup <group> <user> /del` | Remove a user from a group     |
| `whoami`              | Display the current username                    |
| `gpupdate /force`     | Force update Group Policy settings              |
| `lusrmgr.msc`         | Open Local Users and Groups GUI                 |
| `net accounts`        | View or modify password and logon policies      |

## Process and Service Management

| Command               | Description                                      |
|-----------------------|--------------------------------------------------|
| `sc query`            | List all installed services                     |
| `sc start <service>`  | Start a service                                 |
| `sc stop <service>`   | Stop a service                                  |
| `sc config <service>` | Configure a service                             |
| `wmic process`        | Manage processes using WMIC                     |
| `start <program>`     | Start a program                                 |
| `tasklist /svc`       | List services associated with processes         |
| `pslist`              | List processes (Sysinternals tool)              |
| `pssuspend`           | Suspend a process (Sysinternals tool)           |
| `psexec`              | Execute processes remotely (Sysinternals tool)  |

## Advanced Commands

| Command               | Description                                      |
|-----------------------|--------------------------------------------------|
| `regedit`             | Open the Windows Registry Editor                |
| `schtasks`            | Schedule tasks                                  |
| `bcdedit`             | Edit boot configuration data                    |
| `dism`                | Deployment Image Servicing and Management tool  |
| `powershell`          | Open PowerShell                                 |
| `clip`                | Copy command output to clipboard                |
| `for /f`              | Loop through command output                     |
| `findstr`             | Search for strings in files or output           |
| `wevtutil`            | Manage Windows Event Logs                       |
| `auditpol`            | Configure auditing policies                     |
| `certutil`            | Manage certificates and certificate stores      |
| `icacls`              | Modify file and folder permissions              |
| `takeown`             | Take ownership of files or folders              |
| `robocopy /mir`       | Mirror a directory (sync source and destination)|
| `wsl`                 | Launch Windows Subsystem for Linux              |
## Scripting and Automation

| Command               | Description                                      |
|-----------------------|--------------------------------------------------|
| `for`                 | Loop through files or commands                  |
| `if`                  | Conditional execution                           |
| `set`                 | Set or display environment variables            |
| `call`                | Call a batch script from another script         |
| `goto`                | Jump to a labeled section in a script           |
| `choice`              | Prompt user for input in a batch script         |
| `timeout`             | Pause execution for a specified time            |
| `start`               | Start a program or script in a new window       |
| `powershell -command` | Run a PowerShell command from CMD               |
| `wscript`             | Run a VBScript file                             |
## Miscellaneous

| Command               | Description                                      |
|-----------------------|--------------------------------------------------|
| `cls`                 | Clear the command prompt screen                 |
| `exit`                | Close the command prompt                        |
| `help`                | Display a list of available commands            |
| `<command> /?`        | Display help for a specific command             |
| `echo <text>`         | Display a message                               |
| `set`                 | Display or set environment variables            |
| `time`                | Display or set the system time                  |
| `date`                | Display or set the system date                  |
| `color`               | Change the command prompt text and background   |
| `title`               | Set the title of the command prompt window      |
