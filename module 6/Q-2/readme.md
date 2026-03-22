Question - 2:
-------------

Manually configure static routes on a router to direct packets to different subnets.
Use the ip route command and verify connectivity.

network: 192.168.0.0
--------------------

Dividing 192.168.0.0/24 into 4 Equal Subnets

When you divide a /24 network (which contains 256 addresses) into 4 equal subnets, each subnet gets 64 addresses. 
This results in a new subnet mask of /26 (since 2^(32-26)=64).

Subnet 1:
Network IP: 192.168.0.0/26
Address Range: 192.168.0.0 – 192.168.0.63
First Usable IP: 192.168.0.1
Last Usable IP: 192.168.0.62
Broadcast IP: 192.168.0.63

Subnet 2:
Network IP: 192.168.0.64/26
Address Range: 192.168.0.64 – 192.168.0.127
First Usable IP: 192.168.0.65
Last Usable IP: 192.168.0.126
Broadcast IP: 192.168.0.127

Subnet 3:
Network IP: 192.168.0.128/26
Address Range: 192.168.0.128 – 192.168.0.191
First Usable IP: 192.168.0.129
Last Usable IP: 192.168.0.190
Broadcast IP: 192.168.0.191

Subnet 4:
Network IP: 192.168.0.192/26
Address Range: 192.168.0.192 – 192.168.0.255
First Usable IP: 192.168.0.193
Last Usable IP: 192.168.0.254
Broadcast IP: 192.168.0.255


Implementaion:
-------------

Software used : Cisco packet tracer
------------

Topology:
----------

<img width="1385" height="537" alt="image" src="https://github.com/user-attachments/assets/9d5cac19-3bcb-488b-97dc-8c4faead727d" />
<img width="862" height="258" alt="image" src="https://github.com/user-attachments/assets/461a07f7-ab19-484d-971e-8e080731db5c" />
<img width="839" height="236" alt="image" src="https://github.com/user-attachments/assets/aa5259c3-2158-4045-94de-1448c490838b" />
<img width="990" height="246" alt="image" src="https://github.com/user-attachments/assets/1a9a1116-0924-42e9-958b-8bc3a62f83e1" />
<img width="988" height="253" alt="image" src="https://github.com/user-attachments/assets/c67c1f3e-56da-4055-b695-54022533ad58" />
<img width="881" height="255" alt="image" src="https://github.com/user-attachments/assets/48afc815-ca47-455b-a7ee-5783a815b265" />
<img width="874" height="260" alt="image" src="https://github.com/user-attachments/assets/99766ee4-2dd0-44b1-8b33-10c861d438ea" />

Final Ping results after implementation..


<img width="1496" height="219" alt="image" src="https://github.com/user-attachments/assets/1a96c6f7-11fc-4e46-976c-9b4c6467fae3" />




