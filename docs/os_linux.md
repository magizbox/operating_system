# Linux
 
## System

```
# display linux system information
uname -a

# isplay kernel release information
uname -r

# show how long the system has been running + load
uptime
 
# show system host name
hostname

# display the IPO address of the host
hostname -i

# show system roeboot history
last reboot

# show the current date and time
date

# show this month calendar
cal

# display who is online
w

# who are logged in as
whoami

# display information about user
finger user
```

## Hardware

```
# detected hardware and boot messages
dmesg

# CPU model
cat /proc/cpuinfo

# Hardware memory
cat /rpoc/meminfo

# List the number of interrupts per CPU per I/O device
cat /proc/interrupts

# Displays information on hardware configuration of the system
lshw

# Displays block device related information in Linux
lsblk

# Used and free memory (-m for MB)
free -m

# Show PCI devices
lspci -tv

# Show USB devices
lsusb -tv

# Show hardware info from the BIOS
dmidecode

# Show info about disk sda
hdparm -i /dev/sda

# Do a read speed test on disk sda
hdparm -iT /dev/sda

# Test for unreadable blocks on disk sda
badblocks -s /dev/sda
```

## Users

```
# Show the active uder id with login and group
id

# Show the last logins on the system
last

# Show who is logged on the system
who

# Add group "admin"
groupadd admin

# Create user "sam"
useradd -c "Sam Tomshi"

# Delete user sam
userdel sam

# Add user "sam"
adduser sam

# Modify user information
usermod
```

## File Commands

```
# display all infromation about files/directories
ls -al

# Show the path of current directory
pwd

# Create a directory
mkdir directory-name

# Delete file
rm file-name

# Delete directory recursively
rm -r directory-name

# Forcefully remove file
rm -f file-name

# Forcefully remove directory recursively
rm -rf directory-name

# Copy file1 to file2
cp file1 file2

# Copy dir1 to dir2, create dir2 if it doesn't exist
cp -r dir1 dir2

# Rename source to dest / move source to directory
mv file1 file2

# Create symbolic link to file-name
ln -s /path/tofile-name link-name

# Create or update file
touch file

# Place standard input into file
cat > file

# Outut contents of ile
more file

# Output first 10 lines of file
head file

# Output last 10 lines of file
tail file

# Output contents of file as it grows starting with the last 10 lines
tail -f file

# Encrypt file
gpg -c file

# Decrypt file
gpg file gpg

# print the number of bytes, words, and lines in files
wc

# Execute command lines from standard input
xargs
```

## Process Related

```
# display your currently active processes
ps

# find all process id related to telnet process
ps aux | grep 'telnet'

# memory map of process
pmap

# display all running processes
top

# kill process with mentioned pid id
killpid

# kill all processes named proc
killall proc

# send signal to process with its name
pkill process-name

# lists stopped or background jobs
bg

# brings the most recent job to foreground
fg

# brings job n to the foreground
fg n
```

## File Permission Related

```
# change the permissions of file to octal 
chmod octal file-name
# set rwx permission for owner, group, world
chmod 777 /data/test.c
# set rwx permission for owner, rw for group and world
chmod 755 /data/test.c

# change owner of the file
chown owner-user file

# change owner and group owner of the file
chown owner-user:owner-group file-name

# change owner and group owner of the directory
chown owner-user:owner-group directory
```

## Network

```
# display all network ports and ip address
ifconfig -a

# display specific ethernet port
ifconfig eth0

# linux tool to show ehternet status
ehthtool eth0

# linux tool to show ethernet status
mii-tool eth0

# send echo request to test connection
ping host

# get who is information for domain 
whois domain

# get DNS information for domain
dig domain

# reverse lookup host
dig -x host

# lookup DNS ip address for the name
host google.com

# lookup local ip address
hostname -i

# download file
wget file

# list active connections to/from system
netstat -tupl
```

## Compression / Archives

```
# create tar named home.tar contianing home
tar cf home.tar home

# extract the files from file.tar
tar xf file.tar

# create a tar with gzip compression
tar czf file.tar.gz files

# compress file and renames it to file.gz
gzip file
```

## Install package

```
# installl rpm based package
rpm -i pkgname.rpm

# remove package
rpm -e pkgname
```

## Install from source

```
./configure
make
make install
```

## Search

```
# search for pattern in files
grep pattern files

# search recursively for pattern in dir
grep -r pattern dir

# find all instances of file
locate file

# find files names that start with "index"
find /home/tom -name "index"

# find files large than 10000k in /home
find /home -size +10000k
```

## Login (SSH and Telnet)

```
# connect to host as user
ssh user@host

# connect to host using specific port
ssh -p port user@host

# connect to the system using telnet port
telnet host
```

## File Transfer

```
# secure copy file.txt to remote host /tmp folder
scp file.txt server2:/tmp

# synchonize source to destination
rsync -a /home/apps /backup/
```

## Disk Usage

```
# show free space on mounted filesystems
df -h

# show free inodes on mounted filesystems
df -i

# show disks partitions sizes and types
fdisk -l

# display disk usage in human readable form
du -ah

# display total disk usage on the current directory
du -sh
```

## Directory Traverse

```
# to go up on level of the diretory tree
cd .. 

# go to $HOME directory 
cd 

# change to /test directory
cd /test
```

## Related Reading

* Learn Basic Linux Commands with This Downloadable Cheat Sheet, [lifehacker.com](http://lifehacker.com/learn-basic-linux-commands-with-this-downloadable-cheat-1552019180)