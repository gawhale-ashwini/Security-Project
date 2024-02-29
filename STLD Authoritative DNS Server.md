Configuration on STLD Authoritative DNS Server:

The authoritative nameserver is the last step in the nameserver query. If the authoritative name server has access to the requested record, it will return the IP address for the requested hostname back to the DNS Recursor that made the initial request.
●	For this again install bind packages
```bash
yum install bind bind-utils bind-chroot bind-libs
```
●	Make changes on named.conf file
```bash
nano /etc/named.conf
```
Inside we have to edit this:- 

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/15feccdb-7441-4065-a4f4-f4f1fe1a21e4)

Disable recursion, dnssec-enable and dnssec-validation. Never disable these three 
lines by using uncomment.

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/234a2f01-ee97-4f42-9a5c-3ed28932a663)

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/5f8542a5-0491-4685-9b2e-f09e46e93845)

●	Create and edit stld.net
```bash
nano /var/named/stld.net
```
![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/db880833-a035-4ee7-8870-85e7a92b92d2)

●	Edit resolv.conf file

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/c508d9ef-96d1-4f10-ac60-6b9c4492f5c1)

```bash
systemctl restart named
```
●	Query some records that are stored in primary server's stld.net file by using nslookup command










