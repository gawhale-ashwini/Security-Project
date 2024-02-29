Configuration on Root DNS Server:

The root server is the first step in translating (resolving) human readable host names into IP 
addresses. It maintains information regarding top-level domains. Root-zone servers for internet 
top-level domains are already deployed, with this we can create our own internet naming scheme.
● Install bind packages
```bash
yum install bind bind-utils bind-chroot bind-libs
```
● Make changes on named.conf file
```bash
nano /etc/named.conf
```
Inside we have to edit this:-

![image](https://github.com/gawhale-ashwini/Project-0732/assets/149654320/ae37d399-b467-46b6-b511-0bff88e5fc62)

Disable recursion, dnssec-enable and dnssec-validation. Never disable these three 
lines by using comment.

![image](https://github.com/gawhale-ashwini/Project-0732/assets/149654320/7c9ca8b7-b331-45ee-958c-34b9f003f6d5)
![image](https://github.com/gawhale-ashwini/Project-0732/assets/149654320/3917296d-2cbd-461f-aab8-0a652c63bf00)


●	Create and edit root.net
```bash
nano /var/named/root.net
```
![image](https://github.com/gawhale-ashwini/Project-0732/assets/149654320/678daeac-c2cc-4630-b9d4-9e5ed372398f)

●	Edit resolv.conf file

![image](https://github.com/gawhale-ashwini/Project-0732/assets/149654320/66d4d01d-fa68-4769-a1cf-faadf2fdc805)

●	Now edit named.ca file
```bash
nano /var/named/named.ca
```
![image](https://github.com/gawhale-ashwini/Project-0732/assets/149654320/082ba105-7d74-4c89-998d-612aeb9ae92a)

```bash
systemctl restart named
```
```
```bash
iptables -F
```

