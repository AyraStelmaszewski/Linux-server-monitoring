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
    We can use Logwatch, it's a free software to automate user monitoring which can send outpout directly to our mail. In our case we'll configure it to oupout the result in out CLI as we haven't configured a mail service on this server.
<img width="573" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/66d8a82a-be9d-4236-ba50-ee595c80a723">
<img width="557" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/dbadb1e7-2551-4a70-a534-b1fe28d237f8">
<img width="623" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/5d5c425c-c555-4e18-8f0a-70018ae68df6">
<img width="617" alt="image" src="https://github.com/AyraStelmaszewski/Linux-server-monitoring/assets/68444023/c7018871-aea5-49c3-b0b2-1c079dbfd6ba">




  


