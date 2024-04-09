# Linux-server-monitoring
Goal :  being able to gather information about the state of a linux machine.

## The Mission

One of the most important responsibilities a system administrator or SOC analyst have is monitoring the systems he manages. Indeed it's one thing to set them up and install software on them, but then what!? Well the next step is ensuring that the machines you provisioned as well as the services you deployed on them remain **available**, **reliable** and **secure**!
This challenge is divided in two tasks, the first one having you **research how to monitor** a Linux system as well as **what to look for** when doing so. You will have to **take note** of all your findings in a text file (EX: _markdown_) while being as **exhaustive** as possible (_what to monitor_, _how to monitor it_, _commands used_, _..._). Try to answer, but **don't limit yourself to**, the questions below to guide you through 
the research process:

- What are the main area of concern when monitoring a system? (EX: _CPU load_, _disk usage_, ...)
- How can you check what are the most memory intensive [running processes](https://www.computerhope.com/jargon/p/process.htm) ?
- What are log files? Where can you fin them on a typical Linux system ?
- How can you check who where the last connected users, what they did, when they left ?
- What are the different metrics of health and performance of a system ?
- How can you check the uptime of a machine ?
- How can you assess the network traffic ?

The second task is meant to serve as practice and will have you, in a different file, **write a report** with as many relevant information (_what would make sense in a report_) as you can muster on a system you manage. It most preferably would be a remote machine, but it can also be your local machine as this is just practice.


> **IMPORTANT**: Take your time when researching, it's the most important part of this challenge as you'll need to be able to find out what is happening on any given system at any given time. Whether it's the percentage of system's resources currently used, what commands are being run, who is logged in, and so on...

## Write-up
# Main area of concern when monitoring a system 
  > https://www.datadoghq.com/blog/linux-security-threat-detection-datadog/ <br>
  > https://www.linode.com/docs/guides/linux-system-monitoring-fundamentals/ <br>
## CPU
- CPU usage is one of the first places to look when a Linux server shows signs of slowing down. Monitoring CPU usage regularly will help analyze the CPU load over a stipulated            period and overcome performance regression.
- We can use "vmstat" that provides information about CPU activity in addition to memory. <br>
- "mpstat" displays the statistics of CPU usage in the system by initializing the first processor with CPU 0, the second with CPU 1, and so on.

## System load
- System load averages, also called Linux load averages, show the running thread demand on the system as the average number of running plus waiting threads. <br>
- Average system load is calculated over a given period of one, five, and 15 minutes. 

## Memory utilization and processes
-  Monitoring memory helps you identify over- and underused servers and redistribute loads effectively.
-  Memory usage is calculated using the “free” command. The free command provides insight into swap space and the amount of used and unused memory.
-  Monitoring every process running on your Linux server will help you evaluate system performance, debug issues, and optimize server processes.
-  Watch process tree

##  Inode usage
- In linux, files systems contain two parts: metadata and actual data. Each file has an inode that contains metadata about the file. An inode stores all the information regarding the file, including file size, file location, device ID, user ID, group ID, file access privileges, and time stamps.
-  Since every file has an inode, the potential issue is that all the inodes of a disk might be completely used even before the disk is full.
  
## Cron jobs
-  Tracking how long your cron jobs usually run with the help of an efficient Linux server monitoring tool will help you receive customized alerts in case they run too slowly.

## Network statistics 
- Track all the mouvement on your network with a varieted pool of tools 

## Tools to do monitoring 
- Applications Manager is a part of ManageEngine ITOM suite of solutions. Apart from Applications monitoring, ITOM also has solutions to streamline network monitoring, server monitoring, bandwidth monitoring, configuration management, firewall security and compliance, IP address management and switch port management.
- Datadog Cloud Workload Security analyzes the full process tree across all your Linux hosts and containers in real time to automatically detect the kind of threats we’ve looked at.
- Tripwire is a file integrity monitoring tool that watches for changes to critical files on your system.

## Intersting thing to do to increase security on linux server.
- Remove unnecessary services
- Check for security on key files
- Set strong password policy
- Limit root access using SUDO
- Only allow root to access CRON
- Remote access and SSH basic settings
- Disable Xwindow
- Selinux (Security Enhanced Linux)
- Minimize Package Instllation
- Checking accounts for empty passwords
- Monitor user activities
- Install and configure fail2ban
- Rootkit detection
- Monitor system logs
- Enable 2-factor authentication

# Check most memory intensive running processes 

```bash
top
```
# What are log files? Where can you fin them on a typical Linux system ? 
- Usually they are stored in /var/log directory.
# How can you check who where the last connected users, what they did, when they left ?
- See last connected user with : 
```bash
last
```
```bash
grep 'session opened' /var/log/auth.log
```
- To know what users did : 
```bash
cat ~/.bash_history
```
- To know when users left : 
```bash
grep 'session closed' /var/log/auth.log
```
- Since users can delete the bash_history files there is accounting utilities that can be installed using psacct or acct package.
```bash
sudo apt install acct
```
```bash
sudo systemctl enable acct
```
```bash
sudo systemctl start acct
```
- With acct cames "lastcomm" which we can use to know latest Linux cmd
```bash
lastcomm
```

# What are the different metrics of health and performance of a system ?
- There are various metrics used to assess the health and performance of the system.
  > GPU usage <br>
  > Memory usage <br>
  > Disk usage <br>
  > Disk I/O <br>
  > Network Traffic <br>
  > Load Average <br>
  > Process Statistics <br>
  > Filesystem health <br>
  > System Logs <br>
  > Inode Usage <br>

# How can you check the uptime of a machine ?
- With psaact 
```bash
ac
```

# How can you assess the network traffic ?
- With iftop
```bash
sudo iftop -i enp0s1
```
- With iftop 
```bash
sudo iftop -i enp0s1
```
- With iptraf
```bash
sudo iptraf-ng
```

