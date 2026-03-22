Question-2:
-----------
2) Using Packet Tracer. simulate an ARP spoofing attack. Analyze the behavior of devices
on the network when they receive a malicious ARP response. 

Topology used:
-------------

<img width="815" height="604" alt="image" src="https://github.com/user-attachments/assets/2a976d55-ffea-4077-bd30-8555a457d4c1" />

attacker: PC3  - IP 192.168.0.3
--------
Poisoned Arp: 192.168.0.5 's arp ( here default gateway ) 
------------
Compromised network: 192.168.0.0 (entire network since attacker poisoned the default gateway)
--------------------

Insights:
---------
we can see that pc3 (attacker) and router (default gateway ) has same MAC

<img width="890" height="301" alt="image" src="https://github.com/user-attachments/assets/b9c0eb82-e400-4863-8bbc-39c5dbd5b6ae" />

Lets look at poisoned arp entries in switch MAC table... 
here instead of port 3 it has been modified as port 2 by the attacker...

<img width="391" height="231" alt="image" src="https://github.com/user-attachments/assets/05bc485f-533e-49ae-b994-c9e1f6488afa" />

from PC1 (compromised system POV)

<img width="594" height="170" alt="image" src="https://github.com/user-attachments/assets/f9fee0da-816d-441c-9d03-61de75bbadb3" />

dropped ICMP packets are follows ...

<img width="829" height="174" alt="image" src="https://github.com/user-attachments/assets/4c1b7e29-29f6-43d8-aaf6-4b20e584ed25" />
