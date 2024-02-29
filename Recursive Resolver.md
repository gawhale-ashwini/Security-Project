Configuration on Recursive Resolver:-

The DNS recursor is a server designed to receive queries from client machines through applications such as web browsers. 
First you have to install bind packages

```bash
yum install bind bind-utils bind-chroot bind-libs 
```
●	 Edit named.conf file:	
```bash
nano /etc/named.conf
```
Don’t remove the recursion line. Of all the servers, this is the only one that must do recursion. Disable dnssec-enable and dnssec-validation. 

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/7ebf84b7-144f-4119-b2b1-1fa213da5d4e)

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/a7f48794-8ce0-4248-b409-d75350e90092)

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/89ad1500-adbf-4738-a3fc-b3658081321d)

●	Now edit named.ca file
```bash
nano /var/named/named.ca
```
![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/82d7046f-c924-4eec-a080-8b8f01dc7463)

●	Edit resolv.conf file

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/77b97054-233b-4dcd-9169-4013d2837e76)




```bash
systemctl restart named
```
●	Now query the domain name www.example.net by using nslookup command.

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/45f96f88-4256-4727-847d-c65b9956b10b)

