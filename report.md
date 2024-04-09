### MONITORING REPORT 

## Introduction 
Report about an ubuntu server 22.04 running multiples services with e.g. DHCP, DNS, Apache2 etc. 
## Background and context 
We want our server secure/stable as possible and being able to be alerted for any errors/intrusion on it. 
## Programme
It's an ubuntu server 22.04 running to deserve service as DNS for our librarykali domain and DHCP for the client on the network. 
The server is also hosting a website on http://librarykali which is configured with glpi to have an admin panel. 

## Analysis of outcomes & impacts 

1) Monitoring users
   - Without framework : 
```bash
last
```
<img width="544" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/d905caf7-dd0d-4ed8-8e27-eec78f368dbf">
We have an outpout with users log in/out informations. 

  - With framework : 
  


