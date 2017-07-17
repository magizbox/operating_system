### 1. File Operations

### 2. User Environments

### 3. Network Operations

#### 3.1 SSH

SSH Secure Shell Client (homepage, [download](https://it.wm.edu/software/public/ssh/sshsecureshellclient-3.2.9.exe))

#### 3.2 RTMP

rtmpdump ([download](http://rtmpdump.mplayerhq.hu/download/))

#### 3.3 Synchonize

FullSync ([homepage](http://fullsync.sourceforge.net/index.php))

![](http://fullsync.sourceforge.net/screenshots/0.10.0/Profile_Details_dst.png)

### 4. Process

```powershell
# list process
tasklist

# kill prcess
taskkill /im chrome.exe /F
```

### 5. System Information

```powershell
# get architecture
wmic os get osarchitecture
#: OSArchitecture
#: 64-bit
```

### Known Issues

**How to fix MBR**

Fix MBR with command prompt and installation DVD. Fix MBR with command prompt requires the original Windows 8 or 8.1 installation DVD. The instructions are

1.Boot from the original installation DVD.
2.At the Welcome screen, click "Repair your computer".
3.Choose" Troubleshoot > Advanced options > Command Prompt".
4.When the Command Prompt loads, type the following commands in order:

```
bootrec /FixMbr
bootrec /FixBoot
bootrec /ScanOs
bootrec /RebuildBcd
```

Remember to press "Enter" after each command and wait for each operation to finish.

5.Remove the DVD from the disk tray.
6.Type exit and Hit "Enter".
7.Restart your computer and check if Windows 8/8.1 can boot now.

Read More
* [Windows MBR fix](https://www.partitionwizard.com/partitionmagic/windows-8-mbr-fix.html)

