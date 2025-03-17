# Windows Commands

### Table of Contents

1. [File and Directory Management](#file-and-directory-management)
2. [System Information and Management](#system-information-and-management)
3. [Networking](#networking)
4. [Disk and Storage Management](#disk-and-storage-management)
5. [User and Group Management](#user-and-group-management)
6. [Process and Service Management](#process-and-service-management)
7. [Advanced Commands](#advanced-commands)
8. [Scripting and Automation](#scripting-and-automation)
9. [Miscellaneous](#miscellaneous)

## File and Directory Management

| **Command**             | **Description**                                  | **Example**                                      |
|-------------------------|--------------------------------------------------|--------------------------------------------------|
| `dir`                   | Lists files and directories in the current folder | `dir /s` lists all files and subdirectories      |
| `cd <directory>`        | Changes the current directory                    | `cd Documents` switches to the Documents folder  |
| `cd ..`                 | Moves up one directory level                     | `cd ..` navigates up one level                   |
| `mkdir <directory>`     | Creates a new directory                          | `mkdir NewFolder` creates a folder named NewFolder |
| `rmdir <directory>`     | Deletes an empty directory                       | `rmdir OldFolder` removes OldFolder if empty     |
| `del <file>`            | Deletes a specified file                         | `del unwanted.txt` deletes unwanted.txt          |
| `copy <source> <dest>`  | Copies a file to another location                | `copy file.txt D:\Backup` copies to D:\Backup    |
| `move <source> <dest>`  | Moves a file to another location                 | `move file.txt D:\Archive` moves to D:\Archive   |
| `ren <old> <new>`       | Renames a file or directory                      | `ren oldname.txt newname.txt` renames the file   |
| `type <file>`           | Displays the contents of a text file             | `type notes.txt` shows the content of notes.txt  |
| `attrib`                | Displays or modifies file attributes             | `attrib +r file.txt` sets file.txt to read-only  |
| `tree`                  | Shows directory structure in a tree format       | `tree /f` displays all files and folders         |
| `robocopy <source> <dest>` | Advanced tool for copying files and directories | `robocopy C:\Source D:\Dest /e` copies subdirectories |
| `mklink <link> <target>` | Creates a symbolic link                         | `mklink /d C:\Link D:\Original` creates a directory link |
| `xcopy <source> <dest>` | Copies files and directories with advanced options | `xcopy C:\Source D:\Dest /s /e` copies all, including empty folders |
| `fc <file1> <file2>`    | Compares two files and shows differences         | `fc file1.txt file2.txt` displays differences    |
| `comp <file1> <file2>`  | Compares two files byte by byte                  | `comp file1.txt file2.txt` compares the files    |
| `find <string> <file>`  | Searches for a string within a file              | `find "error" log.txt` finds "error" in log.txt  |

## System Information and Management

| **Command**             | **Description**                                  | **Example**                                      |
|-------------------------|--------------------------------------------------|--------------------------------------------------|
| `systeminfo`            | Displays detailed system configuration info      | `systeminfo | find "OS Name"` shows the OS name   |
| `hostname`              | Shows the computer's hostname                    | `hostname` displays the computer name            |
| `ver`                   | Displays the Windows version                     | `ver` shows the current Windows version          |
| `tasklist`              | Lists all running processes                      | `tasklist /fi "imagename eq chrome.exe"` filters for Chrome |
| `taskkill /PID <id>`    | Terminates a process by its process ID (PID)     | `taskkill /PID 1234` ends process with PID 1234  |
| `taskkill /IM <name>`   | Terminates a process by its image name           | `taskkill /IM notepad.exe` stops Notepad         |
| `shutdown /s`           | Shuts down the computer                          | `shutdown /s /t 60` shuts down in 60 seconds     |
| `shutdown /r`           | Restarts the computer                            | `shutdown /r /t 0` restarts immediately          |
| `shutdown /l`           | Logs off the current user                        | `shutdown /l` logs off the current session       |
| `wmic`                  | Accesses Windows Management Instrumentation      | `wmic cpu get name` retrieves the CPU name       |
| `msinfo32`              | Opens the System Information GUI                 | `msinfo32` launches the System Information window |
| `sfc /scannow`          | Scans and repairs protected system files         | `sfc /scannow` initiates the scan and repair     |
| `chkdsk /f`             | Checks and fixes disk errors                     | `chkdsk C: /f` repairs errors on the C: drive    |
| `powercfg /energy`      | Generates a power efficiency diagnostic report   | `powercfg /energy` creates an energy report      |
| `winsat`                | Runs the Windows System Assessment Tool          | `winsat formal` performs a full system assessment |
| `logman`                | Manages performance monitoring data collectors   | `logman query` lists all active data collectors  |
| `driverquery`           | Lists all installed device drivers               | `driverquery /v` shows detailed driver info      |

## Networking

| **Command**             | **Description**                                  | **Example**                                      |
|-------------------------|--------------------------------------------------|--------------------------------------------------|
| `ipconfig`              | Displays IP configuration details                | `ipconfig /all` shows full IP configuration      |
| `ipconfig /release`     | Releases the current IP address                  | `ipconfig /release` releases the IP address      |
| `ipconfig /renew`       | Renews the IP address                            | `ipconfig /renew` requests a new IP address      |
| `ping <host>`           | Tests connectivity to a host                     | `ping google.com` pings Google to check connectivity |
| `tracert <host>`        | Traces the route packets take to a host          | `tracert google.com` traces the path to Google   |
| `netstat`               | Displays active network connections              | `netstat -an` lists all connections and ports    |
| `nslookup <domain>`     | Queries DNS for domain information               | `nslookup google.com` retrieves Google's IPs     |
| `arp -a`                | Shows the Address Resolution Protocol table      | `arp -a` displays cached ARP entries             |
| `netsh`                 | Configures network settings                      | `netsh interface ip set address "Local Area Connection" static 192.168.1.100 255.255.255.0 192.168.1.1` sets a static IP |
| `netstat -ano`          | Shows connections with process IDs               | `netstat -ano | findstr :80` filters for port 80  |
| `route print`           | Displays the IP routing table                    | `route print` shows current routing info         |
| `telnet <host> <port>`  | Tests connectivity to a specific port            | `telnet google.com 80` tests port 80 on Google   |
| `pathping <host>`       | Combines ping and tracert for network analysis   | `pathping google.com` shows latency and loss     |
| `netsh wlan show profiles` | Lists saved Wi-Fi profiles                    | `netsh wlan show profiles` displays Wi-Fi networks |
| `netsh wlan export profile` | Exports Wi-Fi profiles to files              | `netsh wlan export profile name="MyWiFi" folder="C:\Backup"` exports MyWiFi profile |
| `getmac`                | Displays the system's MAC addresses              | `getmac /v` shows detailed MAC information       |
| `nbtstat -a <host>`     | Shows NetBIOS info for a specified host          | `nbtstat -a remotePC` displays NetBIOS details   |
| `net view`              | Lists computers in the network                   | `net view` shows all visible network computers   |

## Disk and Storage Management

| **Command**             | **Description**                                  | **Example**                                      |
|-------------------------|--------------------------------------------------|--------------------------------------------------|
| `chkdsk`                | Checks and repairs disk errors                   | `chkdsk C: /r` repairs and recovers data on C:   |
| `format <drive>`        | Formats a specified drive                        | `format D: /fs:NTFS` formats D: to NTFS          |
| `diskpart`              | Launches the disk partitioning utility           | `diskpart` then `list disk` to list disks        |
| `defrag`                | Defragments a disk to improve performance        | `defrag C: /U /V` defrags C: with verbose output |
| `vssadmin list shadows` | Lists all volume shadow copies                   | `vssadmin list shadows /for=C:` shows C: shadows |
| `fsutil`                | Performs advanced file system operations         | `fsutil fsinfo drives` lists all available drives |
| `bcdedit`               | Edits the Boot Configuration Data                | `bcdedit /enum` lists all boot entries           |
| `diskraid`              | Manages RAID configurations                      | `diskraid /s` displays RAID status               |
| `diskmgmt.msc`          | Opens the Disk Management GUI                    | `diskmgmt.msc` launches Disk Management          |
| `mountvol`              | Manages volume mount points                      | `mountvol D:\MountPoint /L` lists mount points   |
| `vol`                   | Displays volume label and serial number          | `vol C:` shows C: drive info                     |

## User and Group Management

| **Command**             | **Description**                                  | **Example**                                      |
|-------------------------|--------------------------------------------------|--------------------------------------------------|
| `net user`              | Lists all user accounts                          | `net user` displays all local users             |
| `net user <username>`   | Shows details about a specific user              | `net user John` displays John's account info     |
| `net user <username> *` | Changes a user’s password                        | `net user John *` prompts for a new password     |
| `net localgroup`        | Lists all local groups                           | `net localgroup` shows all local groups          |
| `net localgroup <group> <user> /add` | Adds a user to a group            | `net localgroup Administrators John /add` adds John to Admins |
| `net localgroup <group> <user> /del` | Removes a user from a group       | `net localgroup Administrators John /del` removes John |
| `whoami`                | Displays the current logged-in user              | `whoami` shows the current username              |
| `gpupdate /force`       | Forces an immediate Group Policy update          | `gpupdate /force` applies policies now           |
| `lusrmgr.msc`           | Opens the Local Users and Groups GUI             | `lusrmgr.msc` launches the management GUI        |
| `net accounts`          | Manages password and logon policies              | `net accounts /minpwlen:8` sets min password length |
| `net group`             | Manages domain groups (domain environments)      | `net group "Domain Admins" /domain` lists admins |

## Process and Service Management

| **Command**             | **Description**                                  | **Example**                                      |
|-------------------------|--------------------------------------------------|--------------------------------------------------|
| `sc query`              | Lists all installed services                     | `sc query` displays all services                 |
| `sc start <service>`    | Starts a specified service                       | `sc start wuauserv` starts Windows Update        |
| `sc stop <service>`     | Stops a specified service                        | `sc stop wuauserv` stops Windows Update          |
| `sc config <service>`   | Configures service startup settings              | `sc config wuauserv start= auto` sets to auto    |
| `wmic process`          | Manages processes via WMIC                       | `wmic process where name="notepad.exe" delete` ends Notepad |
| `start <program>`       | Launches a program                               | `start notepad` opens Notepad                    |
| `tasklist /svc`         | Lists services tied to processes                 | `tasklist /svc` shows process-service mappings   |
| `pslist`                | Lists processes (Sysinternals tool)              | `pslist` displays all running processes          |
| `pssuspend`             | Suspends a process (Sysinternals tool)           | `pssuspend notepad` pauses Notepad               |
| `psexec`                | Runs processes remotely (Sysinternals tool)      | `psexec \\remotePC cmd` opens a remote CMD       |
| `services.msc`          | Opens the Services GUI                           | `services.msc` launches the Services window      |
| `taskmgr`               | Opens the Task Manager                           | `taskmgr` launches Task Manager                  |

## Advanced Commands

| **Command**             | **Description**                                  | **Example**                                      |
|-------------------------|--------------------------------------------------|--------------------------------------------------|
| `regedit`               | Opens the Windows Registry Editor                | `regedit` launches the Registry Editor           |
| `schtasks`              | Schedules tasks to run at specified times        | `schtasks /create /tn "MyTask" /tr "C:\myprogram.exe" /sc daily /st 09:00` sets a daily task |
| `bcdedit`               | Modifies Boot Configuration Data                 | `bcdedit /set {default} bootmenupolicy legacy` sets legacy boot |
| `dism`                  | Manages and services Windows images              | `dism /online /cleanup-image /restorehealth` repairs the system |
| `powershell`            | Launches PowerShell                              | `powershell` opens a PowerShell session          |
| `clip`                  | Copies command output to the clipboard           | `dir | clip` copies directory listing to clipboard |
| `for /f`                | Loops through command output                     | `for /f "tokens=*" %i in ('dir /b') do echo %i` echoes each file |
| `findstr`               | Searches for strings in files or output          | `findstr /i "error" log.txt` finds "error" case-insensitively |
| `wevtutil`              | Manages Windows Event Logs                       | `wevtutil el` lists all event logs               |
| `auditpol`              | Configures system auditing policies              | `auditpol /get /category:*` shows audit settings |
| `certutil`              | Manages certificates and certificate stores      | `certutil -store My` lists personal certificates |
| `icacls`                | Modifies file and folder permissions             | `icacls C:\folder /grant Users:F` grants full control |
| `takeown`               | Takes ownership of a file or folder              | `takeown /f C:\folder` claims ownership          |
| `robocopy /mir`         | Mirrors directories (syncs source to destination)| `robocopy C:\Source D:\Dest /mir` syncs directories |
| `wsl`                   | Launches Windows Subsystem for Linux             | `wsl --list` lists installed Linux distributions |
| `eventvwr.msc`          | Opens the Event Viewer GUI                       | `eventvwr.msc` launches Event Viewer             |
| `msconfig`              | Opens System Configuration utility               | `msconfig` launches the configuration tool       |
| `secpol.msc`            | Opens Local Security Policy Editor               | `secpol.msc` launches the policy editor          |

## Scripting and Automation

| **Command**             | **Description**                                  | **Example**                                      |
|-------------------------|--------------------------------------------------|--------------------------------------------------|
| `for`                   | Loops through files or commands                  | `for %i in (*.txt) do echo %i` lists .txt files  |
| `if`                    | Executes commands conditionally                  | `if exist file.txt (echo exists) else (echo missing)` checks file |
| `set`                   | Sets or displays environment variables           | `set PATH=%PATH%;C:\newpath` appends to PATH     |
| `call`                  | Runs another batch script                        | `call otherscript.bat` executes otherscript.bat  |
| `goto`                  | Jumps to a labeled section in a script           | `goto :label` moves to the :label section        |
| `choice`                | Prompts user for input in a script               | `choice /c yn /m "Yes or No?"` asks for Y/N      |
| `timeout`               | Pauses execution for a set time                  | `timeout /t 10` waits 10 seconds                 |
| `start`                 | Opens a program or script in a new window        | `start "" "C:\program.exe"` runs in a new window |
| `powershell -command`   | Runs a PowerShell command from CMD               | `powershell -command "Get-Process"` lists processes |
| `wscript`               | Executes a VBScript file                         | `wscript script.vbs` runs script.vbs             |
| `echo`                  | Displays messages or controls echoing            | `echo Hello World` prints "Hello World"          |
| `assoc`                 | Manages file extension associations              | `assoc .txt` shows the .txt file association     |
| `ftype`                 | Manages file type associations                   | `ftype txtfile` shows the command for txtfile    |

## Miscellaneous

| **Command**             | **Description**                                  | **Example**                                      |
|-------------------------|--------------------------------------------------|--------------------------------------------------|
| `cls`                   | Clears the Command Prompt screen                 | `cls` clears the current display                 |
| `exit`                  | Closes the Command Prompt window                 | `exit` terminates the session                    |
| `help`                  | Lists available commands                         | `help` displays a command list                   |
| `<command> /?`          | Shows help for a specific command                | `dir /?` provides detailed dir command help      |
| `echo <text>`           | Displays a specified message                     | `echo Hello` prints "Hello"                      |
| `set`                   | Shows or sets environment variables              | `set` lists all environment variables            |
| `time`                  | Displays or sets the system time                 | `time /t` shows the current time                 |
| `date`                  | Displays or sets the system date                 | `date /t` shows the current date                 |
| `color`                 | Changes the text and background colors           | `color 0a` sets black background, green text     |
| `title`                 | Sets the Command Prompt window title             | `title My Prompt` sets the window title          |
| `prompt`                | Customizes the Command Prompt string             | `prompt $P$G` shows current directory >          |
| `mode`                  | Configures console settings (e.g., size)         | `mode con cols=80 lines=25` sets window size     |
| `more <file>`           | Displays file contents one page at a time        | `more log.txt` pages through log.txt             |
