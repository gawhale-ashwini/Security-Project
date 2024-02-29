# TLD (ARPA) DNS Server Configuration for reverse lookup tree:

## 1. The TLD (ARPA) hold the information about two different domains : 
I.	"ip6.arpa"  for ipv6 reverse lookup.
II.	"in-addr.arpa" for IPv4 reverse lookup. 


The "named.conf" file for TLD ("ARPA") DNS server is as follows:

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/d77041aa-7a58-4eeb-83d5-cac6b8c640bf)

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/52cf80a7-aa7f-43f4-8eea-a4ea6b96ddbb)

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/6a146b9c-917d-4352-aaee-452e84ecab3c)

## 2. Zone file "arpa-zone" for TLD ("ARPA")  DNS: A glue record for STLD "in-addr.arpa" domain
             for IPv4 reverse lookup has been added that list's the name servers for "in-addr.arpa" domains. Zone file for TLD (ARPA) DNS is shown below :

![image](https://github.com/gawhale-ashwini/Security-Project/assets/149654320/8f17b014-bbfa-470a-9420-1d2318db47a7)

