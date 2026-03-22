Question-7:
----------

In Cisco Packet Tracer, create a small network with multiple devices (e.g., 2 PCs and a router). 
Use private IP addresses (e.g., 192.168.1.x) on the PCs and configure the router to perform
NAT to allow the PCs to access the internet. 

software used: cisco packet tracer
-------------

Network topology:
----------------
<img width="1144" height="548" alt="image" src="https://github.com/user-attachments/assets/cb21a1bf-4490-40eb-8527-5775aebe46b5" />
config done in router 0:
-----------------------
Router(config-if)#exit
Router(config)#interface Gig0/0
Router(config-if)#ip nat inside 
Router(config-if)#exit
Router(config)#interface Gig0/1
Router(config-if)#ip nat outside
Router(config-if)#exit
Router(config)#ip nat inside source static 192.168.0.2 55.55.55.2
Router(config)#ip nat inside source static 192.168.0.3 55.55.55.3
Router(config)#ip route 66.66.66.0 255.255.255.0 192.168.1.2

similar configration is done for router 1.

Testing:
--------

from the below figure it is evident that IP Masquerading in NAT has been achieved.

<img width="1420" height="222" alt="image" src="https://github.com/user-attachments/assets/75f2ef60-c1b8-4f70-9c73-ae65cd76e133" />

and pinging using the public IP from pc1 to pc0 and vice versa is successfull indicating the working of static NAT

From pc1:
----------

C:\>ping 55.55.55.3

Pinging 55.55.55.3 with 32 bytes of data:

Reply from 55.55.55.3: bytes=32 time<1ms TTL=126
Reply from 55.55.55.3: bytes=32 time<1ms TTL=126
Reply from 55.55.55.3: bytes=32 time=8ms TTL=126
Reply from 55.55.55.3: bytes=32 time=15ms TTL=126

Ping statistics for 55.55.55.3:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 0ms, Maximum = 15ms, Average = 5ms


From PC0:
---------

C:\>ping 66.66.66.2

Pinging 66.66.66.2 with 32 bytes of data:

Reply from 66.66.66.2: bytes=32 time<1ms TTL=126
Reply from 66.66.66.2: bytes=32 time<1ms TTL=126
Reply from 66.66.66.2: bytes=32 time<1ms TTL=126
Reply from 66.66.66.2: bytes=32 time=1ms TTL=126

Ping statistics for 66.66.66.2:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 0ms, Maximum = 1ms, Average = 0ms

C:\>

NAT Table:
---------
<img width="421" height="207" alt="image" src="https://github.com/user-attachments/assets/968a7449-2590-4cf2-baae-38484b15849f" />

<img width="317" height="121" alt="image" src="https://github.com/user-attachments/assets/fa1ff485-9230-46f3-a121-cbfd5bb65e7f" />
