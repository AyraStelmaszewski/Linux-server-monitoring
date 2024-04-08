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

***CPU***
    CPU usage is one of the first places to look when a Linux server shows signs of slowing down. Monitoring CPU usage regularly will help analyze the CPU load over a stipulated            period and overcome performance regression.
     > We can use "vmstat" that provides information about CPU activity in addition to memory. <br>
     > "mpstat" displays the statistics of CPU usage in the system by initializing the first processor with CPU 0, the second with CPU 1, and so on.

***System load***
    System load averages, also called Linux load averages, show the running thread demand on the system as the average number of running plus waiting threads. <br>
    Average system load is calculated over a given period of one, five, and 15 minutes. 

     
- Harddrive storage 
- Network statistics 
