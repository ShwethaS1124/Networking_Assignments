
Question:
---------

12 ) Create an extended ACL to block specific applications, such as HTTP or FTP traffic.
Test the ACL rules by attempting to access blocked services.
10) Implement ACLs to restrict traffic based on source and destination ports.
Test rules by simulating legitimate and unauthorized traffic.

Topology:
---------

<img width="1139" height="460" alt="image" src="https://github.com/user-attachments/assets/70e30e24-79a2-44be-a3b9-569a8f7526b4" />
configs:
--------
<img width="801" height="199" alt="image" src="https://github.com/user-attachments/assets/d6be74fa-0f62-41e2-b810-d21eda8b29e5" />
<img width="886" height="177" alt="image" src="https://github.com/user-attachments/assets/cd2c7ae9-e0fb-451c-8c9b-8eb065665da7" />
<img width="786" height="185" alt="image" src="https://github.com/user-attachments/assets/5c0990d3-e11e-4979-acf7-d205102895de" />
<img width="884" height="177" alt="image" src="https://github.com/user-attachments/assets/755f1d58-0701-4681-a2e3-58b7391ba0d7" />
<img width="792" height="170" alt="image" src="https://github.com/user-attachments/assets/b56214db-683c-4547-ab05-bca470592079" />

used extended ACL config in router 2:
-------------------------------------
	
Router>enable
Router#show access-lists
Extended IP access list test
    10 permit tcp 192.168.0.0 0.0.0.255 192.168.3.0 0.0.0.255 eq www

( this only allows the PC0 to access the http service and blocks all other packets ) 

show IP interface o/p (router2) :
--------------------
Router#show ip interface
GigabitEthernet0/0 is up, line protocol is up (connected)
  Internet address is 192.168.0.1/24
  Broadcast address is 255.255.255.255
  Address determined by setup command
  MTU is 1500 bytes
  Helper address is not set
  Directed broadcast forwarding is disabled
  Outgoing access list is not set
  Inbound  access list is test


Ping (ICMP) from PC0 to server 0 :
------------------------------------

this should be blocked ...

<img width="814" height="115" alt="image" src="https://github.com/user-attachments/assets/523d9934-6d4c-4369-bae1-da252e6f22ca" />

the http from PC0 to server0 is given below indicating the working of the Extended ACL.
<img width="861" height="320" alt="image" src="https://github.com/user-attachments/assets/19a16368-7146-49b1-89f0-0a2e36bc1d27" />

