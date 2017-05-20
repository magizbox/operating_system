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

## Related Reading

* Learn Basic Linux Commands with This Downloadable Cheat Sheet, [lifehacker.com](http://lifehacker.com/learn-basic-linux-commands-with-this-downloadable-cheat-1552019180)