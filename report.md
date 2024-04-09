### MONITORING REPORT 

## Introduction 
Report about an ubuntu server 22.04 running multiples services with e.g. DHCP, DNS, Apache2 etc. 
## Background and context 
We want our server secure/stable as possible and being able to be alerted for any errors/intrusion on it. 
## Programme
It's an ubuntu server 22.04 running to deserve service as DNS for our librarykali domain and DHCP for the client on the network. 
The server is also hosting a website on http://librarykali which is configured with glpi to have an admin panel. 

## Analysis of outcomes & impacts 

**1) Monitoring users** <br>
1) Watch users logs :
```bash
last
```
<img width="544" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/d905caf7-dd0d-4ed8-8e27-eec78f368dbf"> <br>
~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~ <br>
2) We have an outpout with users log in/out informations :    
```bash
cat ~/.bash_history
```
   > Care this file can be delete. /!!How to see bash history if the file got deleted?/!!


~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~ <br>
    
3) We can use Logwatch, it's a free software to automate user monitoring which can send outpout directly to our mail. In our case we'll configure it to oupout the result in out CLI as we haven't configured a mail service on this server.
<img width="573" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/66d8a82a-be9d-4236-ba50-ee595c80a723">
<img width="557" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/dbadb1e7-2551-4a70-a534-b1fe28d237f8">
<img width="623" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/5d5c425c-c555-4e18-8f0a-70018ae68df6">
<img width="617" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/c7018871-aea5-49c3-b0b2-1c079dbfd6ba">
~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~ <br>

**2) CPU**
```bash
top
```
<img width="751" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/a4ec6d30-e6b7-4fa6-9254-7da93eb54189">

~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~ <br>

```bash
mpstat
```
<img width="751" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/662b2d92-b6ee-49d0-8691-e44e6e80630e">

**3) Load average**
```bash
uptime
```
<img width="449" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/5291bbba-0a9e-4f0b-8a21-87ff1e1076ea">

```bash
cat /proc/loadavg
```
<img width="313" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/41d87221-0c7f-494d-ab6d-cea662a9e389">

```bash
w
```
<img width="529" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/3516aacb-837a-4187-b476-3fbc05a2a5f8">

**3) Load average**
```bash
ps
```
<img width="756" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/821641e5-30bf-4fdf-ab2c-a4402c250aa2">

```bash
top
```
<img width="751" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/a4ec6d30-e6b7-4fa6-9254-7da93eb54189">
<img width="677" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/a3acb27b-df42-432a-b2ac-9ee6e962b4a6">

**4) Network statistics**
```bash
netstat
```
<img width="674" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/62185748-1967-405f-9405-8b4b1a7129bb">

```bash
tcpdump
```
<img width="755" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/7cdbefa6-4b95-437c-892f-2a0806b174d0">

```bash
tcpdump
```
<img width="750" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/23cf15cf-b84f-4fc7-a3fd-12d61a3bb90b">

```bash
sudo iftop -i enp0s1
```
<img width="747" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/ad71add7-e1ff-4d13-88e8-cc2840cf61d2">

```bash
sudi iptraf
```
<img width="747" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/ad71add7-e1ff-4d13-88e8-cc2840cf61d2">

**5) Inode**

```bash
find . -maxdepth 1 -type d -exec sh -c '(echo -n "{}: "; find "{}" | wc -l)' \;
```



**5) Inode**

```bash
find . -maxdepth 1 -type d -exec sh -c '(echo -n "{}: "; find "{}" | wc -l)' \;
```
```bash
find . -maxdepth 1 -type d -exec sh -c '(echo -n "{}: "; find "{}" | wc -l)' \;
```

<img width="756" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/872bdad9-de80-4d8a-ae4e-a87be7a33081">

**5) iptraf**

```bash
sudo find . -maxdepth 1 -type d -exec sh -c '(echo -n "{}: "; find "{}" | wc -l)' \; 
```

<img width="760" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/e3d2a545-3e06-40a1-be28-20eb9c4ba618">







  


