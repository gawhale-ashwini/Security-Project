Configuration on TLD DNS Server:

This nameserver is the next step in the search for a specific IP address, and it hosts the last portion of a hostname (In example.net, the TLD server is “net”).
Create a file accordingly to point towards our own root DNS server with some changes.
●	Install bind packages
```bash
yum install bind bind-utils bind-chroot bind-libs
```
●	Make changes on named.conf file
```bash
nano /etc/named.conf
```
Inside we have to edit this:- 

![image](https://github.com/gawhale-ashwini/Project-0732/assets/149654320/db98b609-7bd0-4b7d-ab60-eca3dc5c9665)

![image](https://github.com/gawhale-ashwini/Project-0732/assets/149654320/d676f5f3-b8b5-4a00-8992-f456464ac9fa)

![image](https://github.com/gawhale-ashwini/Project-0732/assets/149654320/13a5cb58-ea07-48a4-bd21-cfc25a0a88e3)

●	Create and edit tld.net
```bash
nano /var/named/tld.net
```
![image](https://github.com/gawhale-ashwini/Project-0732/assets/149654320/8ad3f1a7-472e-4505-8156-454a38d9bf25)

●	Edit resolv.conf 

![image](https://github.com/gawhale-ashwini/Project-0732/assets/149654320/adf4e9ee-4e49-4c8b-b3c7-7bfee9e854a4)
```bash
systemctl restart named
```
●	Query some records that are stored in primary server's tld.net file by using nslookup command
