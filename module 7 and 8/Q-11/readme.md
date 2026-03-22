Question:
---------

Configure a standard Access Control List (ACL) on a router to deny traffic from a specific IP range.
Test connectivity to verify the ACL is working as intended.

Topology:
---------
<img width="1118" height="487" alt="image" src="https://github.com/user-attachments/assets/8db61f5c-047b-41a6-aaff-aba97b778d32" />
config:
-------
<img width="784" height="167" alt="image" src="https://github.com/user-attachments/assets/56a0099e-1e4e-43b6-948b-3169e68d74ba" />
<img width="787" height="147" alt="image" src="https://github.com/user-attachments/assets/9c09fb02-8aff-4a19-a26f-111861adeabc" />
<img width="784" height="163" alt="image" src="https://github.com/user-attachments/assets/1c07b0ce-b686-442f-9c45-99f0fbd526ea" />
<img width="885" height="172" alt="image" src="https://github.com/user-attachments/assets/6853af78-7a53-4243-9334-8675da5666a5" />
<img width="884" height="172" alt="image" src="https://github.com/user-attachments/assets/c12a5892-b9f8-4b13-9c99-7142901ead03" />
<img width="789" height="191" alt="image" src="https://github.com/user-attachments/assets/953c1684-bb78-48a1-8e58-5f8df80810bc" />

since the standard ACL needs to be placed closer to dest the standard ACL is placed in router7 here.

in router 7 ....

Router>enable
Router#show access-lists
Standard IP access list 1
    10 deny 192.168.1.0 0.0.0.255
    20 permit any

Router#

Show ip interface in router7:

GigabitEthernet0/1 is up, line protocol is up (connected)
  Internet address is 192.168.3.1/24
  Broadcast address is 255.255.255.255
  Address determined by setup command
  MTU is 1500 bytes
  Helper address is not set
  Directed broadcast forwarding is disabled
  Outgoing access list is 1

packet captures:
---------------
the pings from 192.168.1.0 fails to 192.168.2.0 but
pings from other networks (192.168.0.0) is successfull in 192.168.2.0 due to standard ACL

<img width="866" height="168" alt="image" src="https://github.com/user-attachments/assets/1b157da5-e91f-4109-9a29-49c1aff9d680" />
