## File and Directory Management

| Command               | Description                                      | Example                                         |
|-----------------------|--------------------------------------------------|-------------------------------------------------|
| `dir`                 | List files and directories in the current folder | `dir /s` lists all files and subdirectories     |
| `cd <directory>`      | Change directory                                 | `cd Documents` goes to the Documents folder     |
| `cd ..`               | Move up one directory level                     | `cd ..` moves up one level                      |
| `mkdir <directory>`   | Create a new directory                          | `mkdir NewFolder` creates NewFolder             |
| `rmdir <directory>`   | Remove a directory (must be empty)              | `rmdir OldFolder` deletes OldFolder if empty    |
| `del <file>`          | Delete a file                                   | `del unwanted.txt` deletes unwanted.txt         |
| `copy <source> <dest>`| Copy a file to another location                 | `copy file.txt D:\Backup` copies to D:\Backup   |
| `move <source> <dest>`| Move a file to another location                 | `move file.txt D:\Archive` moves to D:\Archive  |
| `ren <old> <new>`     | Rename a file or directory                      | `ren oldname.txt newname.txt` renames the file  |
| `type <file>`         | Display the contents of a file                  | `type notes.txt` shows content of notes.txt     |
| `attrib`              | Display or change file attributes               | `attrib +r file.txt` makes file.txt read-only   |
| `tree`                | Display directory structure as a tree           | `tree /f` shows all files and folders           |
| `robocopy <source> <dest>` | Advanced file copying tool                  | `robocopy C:\Source D:\Dest /e` copies subdirs  |
| `mklink <link> <target>` | Create symbolic links (symlinks)             | `mklink /d C:\Link D:\Original` creates a link  |
| `xcopy <source> <dest>`| Copy files and directories with more options   | `xcopy C:\Source D:\Dest /s /e` copies all      |

## System Information and Management

| Command               | Description                                      | Example                                         |
|-----------------------|--------------------------------------------------|-------------------------------------------------|
| `systeminfo`          | Display detailed system information             | `systeminfo | find "OS Name"` finds the OS name  |
| `hostname`            | Display the computer name                       | `hostname` shows the computer name              |
| `ver`                 | Display the Windows version                     | `ver` shows the Windows version                 |
| `tasklist`            | List all running processes                      | `tasklist /fi "imagename eq chrome.exe"` lists Chrome processes |
| `taskkill /PID <id>`  | Terminate a process by its PID                  | `taskkill /PID 1234` kills process with PID 1234|
| `taskkill /IM <name>` | Terminate a process by its name                 | `taskkill /IM notepad.exe` kills Notepad        |
| `shutdown /s`         | Shut down the computer                          | `shutdown /s /t 60` shuts down in 60 seconds    |
| `shutdown /r`         | Restart the computer                            | `shutdown /r /t 0` restarts immediately         |
| `shutdown /l`         | Log off the current user                        | `shutdown /l` logs off the current user         |
| `wmic`                | Windows Management Instrumentation Command-line | `wmic cpu get name` gets the CPU name           |
| `msinfo32`            | Open System Information GUI                     | `msinfo32` opens the System Information window  |
| `sfc /scannow`        | Scan and repair system files                    | `sfc /scannow` starts the scan                  |
| `chkdsk /f`           | Check and fix disk errors                       | `chkdsk C: /f` checks and fixes the C: drive    |
| `powercfg /energy`    | Generate a power efficiency report              | `powercfg /energy` creates a report             |
| `winsat`              | Run Windows System Assessment Tool              | `winsat formal` runs a full assessment          |
| `logman`              | Manage performance monitoring logs              | `logman query` lists all data collectors        |
| `driverquery`         | List all installed drivers                      | `driverquery /v` shows detailed driver info     |

## Networking

| Command               | Description                                      | Example                                         |
|-----------------------|--------------------------------------------------|-------------------------------------------------|
| `ipconfig`            | Display IP configuration                        | `ipconfig /all` shows detailed IP info          |
| `ipconfig /release`   | Release the IP address                          | `ipconfig /release` releases the current IP     |
| `ipconfig /renew`     | Renew the IP address                            | `ipconfig /renew` gets a new IP                 |
| `ping <host>`         | Ping a host to check connectivity               | `ping google.com` checks connectivity to Google |
| `tracert <host>`      | Trace the route to a host                       | `tracert google.com` shows the path to Google   |
| `netstat`             | Display network connections                     | `netstat -an` shows all connections and ports   |
| `nslookup <domain>`   | Look up DNS information for a domain            | `nslookup google.com` shows Google's IPs        |
| `arp -a`              | Display the ARP table                           | `arp -a` lists all cached ARP entries           |
| `netsh`               | Configure network settings                      | `netsh interface ip set address "Local Area Connection" static 192.168.1.100 255.255.255.0 192.168.1.1` sets static IP |
| `netstat -ano`        | Display all active connections with PIDs        | `netstat -ano | findstr :80` finds port 80 connections |
| `route print`         | Display the routing table                       | `route print` shows the current routes          |
| `telnet <host> <port>`| Test connectivity to a specific port            | `telnet google.com 80` checks if port 80 is open|
| `pathping <host>`     | Combines `ping` and `tracert` functionality     | `pathping google.com` shows packet loss and latency |
| `netsh wlan show profiles` | View saved Wi-Fi profiles                | `netsh wlan show profiles` lists saved Wi-Fi networks |
| `netsh wlan export profile` | Export Wi-Fi profiles to a file          | `netsh wlan export profile name="MyWiFi" folder="C:\Backup"` exports profile |
| `getmac`              | Display MAC addresses                           | `getmac /v` shows detailed MAC info             |

## Disk and Storage Management

| Command               | Description                                      | Example                                         |
|-----------------------|--------------------------------------------------|-------------------------------------------------|
| `chkdsk`              | Check and repair disk errors                    | `chkdsk C: /r` locates bad sectors and recovers info |
| `format <drive>`      | Format a disk                                   | `format D: /fs:NTFS` formats D: to NTFS         |
| `diskpart`            | Open the disk partitioning tool                 | `diskpart` then `list disk` to list all disks   |
| `defrag`              | Defragment a disk                               | `defrag C: /U /V` defrags C: with progress      |
| `vssadmin list shadows` | List volume shadow copies                    | `vssadmin list shadows /for=C:` lists shadows for C: |
| `fsutil`              | File system utility for advanced operations     | `fsutil fsinfo drives` lists all drives         |
| `bcdedit`             | Edit boot configuration data                    | `bcdedit /enum` lists all boot entries          |
| `diskraid`            | Manage RAID configurations                      | `diskraid /s` shows RAID status                 |
| `storage spaces`      | Manage Storage Spaces (virtual disks)           | `Get-StoragePool` in PowerShell lists pools     |
| `diskmgmt.msc`        | Open Disk Management GUI                        | `diskmgmt.msc` opens Disk Management            |

## User and Group Management

| Command               | Description                                      | Example                                         |
|-----------------------|--------------------------------------------------|-------------------------------------------------|
| `net user`            | List user accounts                              | `net user` shows all users                      |
| `net user <username>` | Display information about a user                | `net user John` shows John's details            |
| `net user <username> *`| Change a user's password                       | `net user John *` prompts for a new password    |
| `net localgroup`      | List local groups                               | `net localgroup` shows all local groups         |
| `net localgroup <group> <user> /add` | Add a user to a group          | `net localgroup Administrators John /add` adds John to Admins |
| `net localgroup <group> <user> /del` | Remove a user from a group     | `net localgroup Administrators John /del` removes John from Admins |
| `whoami`              | Display the current username                    | `whoami` shows the logged-in user               |
| `gpupdate /force`     | Force update Group Policy settings              | `gpupdate /force` applies policies immediately  |
| `lusrmgr.msc`         | Open Local Users and Groups GUI                 | `lusrmgr.msc` opens the GUI                     |
| `net accounts`        | View or modify password and logon policies      | `net accounts /minpwlen:8` sets min password length to 8 |
| `net group`           | Manage domain groups (in domain environments)   | `net group "Domain Admins" /domain` lists domain admins |

## Process and Service Management

| Command               | Description                                      | Example                                         |
|-----------------------|--------------------------------------------------|-------------------------------------------------|
| `sc query`            | List all installed services                     | `sc query` shows all services                   |
| `sc start <service>`  | Start a service                                 | `sc start wuauserv` starts Windows Update service |
| `sc stop <service>`   | Stop a service                                  | `sc stop wuauserv` stops Windows Update service |
| `sc config <service>` | Configure a service                             | `sc config wuauserv start= auto` sets to auto start |
| `wmic process`        | Manage processes using WMIC                     | `wmic process where name="notepad.exe" delete` terminates Notepad |
| `start <program>`     | Start a program                                 | `start notepad` opens Notepad                   |
| `tasklist /svc`       | List services associated with processes         | `tasklist /svc` shows services for each process |
| `pslist`              | List processes (Sysinternals tool)              | `pslist` lists all processes                    |
| `pssuspend`           | Suspend a process (Sysinternals tool)           | `pssuspend notepad` suspends Notepad            |
| `psexec`              | Execute processes remotely (Sysinternals tool)  | `psexec \\remotePC cmd` opens remote command prompt |
| `services.msc`        | Open Services GUI                               | `services.msc` opens the Services window        |

## Advanced Commands

| Command               | Description                                      | Example                                         |
|-----------------------|--------------------------------------------------|-------------------------------------------------|
| `regedit`             | Open the Windows Registry Editor                | `regedit` opens the Registry Editor             |
| `schtasks`            | Schedule tasks                                  | `schtasks /create /tn "MyTask" /tr "C:\myprogram.exe" /sc daily /st 09:00` creates a daily task |
| `bcdedit`             | Edit boot configuration data                    | `bcdedit /set {default} bootmenupolicy legacy` sets legacy boot menu |
| `dism`                | Deployment Image Servicing and Management tool  | `dism /online /cleanup-image /restorehealth` repairs system image |
| `powershell`          | Open PowerShell                                 | `powershell` opens PowerShell                   |
| `clip`                | Copy command output to clipboard                | `dir | clip` copies directory listing to clipboard |
| `for /f`              | Loop through command output                     | `for /f "tokens=*" %i in ('dir /b') do echo %i` lists each file |
| `findstr`             | Search for strings in files or output           | `findstr /i "error" log.txt` finds "error" in log.txt |
| `wevtutil`            | Manage Windows Event Logs                       | `wevtutil el` lists all event logs              |
| `auditpol`            | Configure auditing policies                     | `auditpol /get /category:*` shows audit policies|
| `certutil`            | Manage certificates and certificate stores      | `certutil -store My` lists personal certificates|
| `icacls`              | Modify file and folder permissions              | `icacls C:\folder /grant Users:F` grants full control to Users |
| `takeown`             | Take ownership of files or folders              | `takeown /f C:\folder` takes ownership of folder|
| `robocopy /mir`       | Mirror a directory (sync source and destination)| `robocopy C:\Source D:\Dest /mir` syncs Source to Dest |
| `wsl`                 | Launch Windows Subsystem for Linux              | `wsl --list` lists installed distributions      |
| `eventvwr.msc`        | Open Event Viewer GUI                           | `eventvwr.msc` opens Event Viewer               |

## Scripting and Automation

| Command               | Description                                      | Example                                         |
|-----------------------|--------------------------------------------------|-------------------------------------------------|
| `for`                 | Loop through files or commands                  | `for %i in (*.txt) do echo %i` lists all .txt files |
| `if`                  | Conditional execution                           | `if exist file.txt (echo exists) else (echo does not exist)` checks file existence |
| `set`                 | Set or display environment variables            | `set PATH=%PATH%;C:\newpath` adds to PATH       |
| `call`                | Call a batch script from another script         | `call otherscript.bat` runs otherscript.bat     |
| `goto`                | Jump to a labeled section in a script           | `goto :label` jumps to :label                   |
| `choice`              | Prompt user for input in a batch script         | `choice /c yn /m "Yes or No?"` asks for Y or N  |
| `timeout`             | Pause execution for a specified time            | `timeout /t 10` waits for 10 seconds            |
| `start`               | Start a program or script in a new window       | `start "" "C:\program.exe"` runs in new window  |
| `powershell -command` | Run a PowerShell command from CMD               | `powershell -command "Get-Process"` lists processes |
| `wscript`             | Run a VBScript file                             | `wscript script.vbs` executes script.vbs        |
| `echo`                | Display messages or turn command echoing on/off | `echo Hello World` prints "Hello World"         |

## Miscellaneous

| Command               | Description                                      | Example                                         |
|-----------------------|--------------------------------------------------|-------------------------------------------------|
| `cls`                 | Clear the command prompt screen                 | `cls` clears the screen                         |
| `exit`                | Close the command prompt                        | `exit` closes the command prompt                |
| `help`                | Display a list of available commands            | `help` lists available commands                 |
| `<command> /?`        | Display help for a specific command             | `dir /?` shows help for `dir`                   |
| `echo <text>`         | Display a message                               | `echo Hello` prints "Hello"                     |
| `set`                 | Display or set environment variables            | `set` lists all environment variables           |
| `time`                | Display or set the system time                  | `time /t` shows the current time                |
| `date`                | Display or set the system date                  | `date /t` shows the current date                |
| `color`               | Change the command prompt text and background   | `color 0a` sets black background, green text    |
| `title`               | Set the title of the command prompt window      | `title My Prompt` sets the title                |
| `prompt`              | Change the command prompt string                | `prompt $P$G` sets prompt to directory >        |
