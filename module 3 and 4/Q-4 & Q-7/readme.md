Q-4 & Q-7:
---------
Troubleshoot coneectivity with ping and traceroute.


Software used:
--------------
cisco packet tracer

Topology used:
-------------
<img width="758" height="96" alt="image" src="https://github.com/user-attachments/assets/99b32ad5-4549-433e-8b1b-bf89c65bd48a" />

Problem:
-------
ping from pc0 to pc1 fails.... lets trouble shoot...

Troubleshooting;
---------------
-> try tracert from pc0 to pc3 

<img width="486" height="163" alt="image" src="https://github.com/user-attachments/assets/f5a6944c-3b51-41f5-aeef-e9d14c5a545d" />

since the default gateway is reachable and others are not lets go to router 1
and ping the neighbouring interfaces and check routing tables 

<img width="662" height="347" alt="image" src="https://github.com/user-attachments/assets/621f00df-3a10-48eb-a689-b2db42bd09bd" />

The routing table of router1 is found as above. It is found that no route the destination network available and thus
adding a static entry to the destination net and modifying the same on the other side ...

<img width="598" height="165" alt="image" src="https://github.com/user-attachments/assets/858c41c4-1c6b-4c1e-869e-1ac8e3c3db7e" />

<img width="514" height="254" alt="image" src="https://github.com/user-attachments/assets/94888fa5-ff93-4230-a212-a2483be425a9" />

thus the network has been troubleshooted and the network has been properly configured


-> try tracert from pc0 to pc3 
