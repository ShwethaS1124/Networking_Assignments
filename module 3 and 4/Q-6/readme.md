Question:
---------

ping from one machine to another and if the ping fails, use ifconfig to ensure the pings are configured correctly.

software used:
---------------
cisco packet tracer

Used topology:
-------------
<img width="786" height="98" alt="image" src="https://github.com/user-attachments/assets/29ba45cf-49e4-4cce-abac-d1eedd9bf47c" />
problem:
-------

ping from pc0 to pc1 fails... 

problem:
-------

<img width="369" height="137" alt="image" src="https://github.com/user-attachments/assets/7d6c6ea5-a0dd-430d-8e52-603655c44dde" />

lets use ifconfig and check if the end ip is 192.168.2.2...

below is the ipconfig output of pc1

<img width="491" height="339" alt="image" src="https://github.com/user-attachments/assets/c9ad41af-ba43-41c3-84c6-6617442d172d" />

It is found that the IP of pc1 is 192.168.2.3... thus modifying the ping command accordingly

<img width="520" height="213" alt="image" src="https://github.com/user-attachments/assets/c9943229-21ae-4809-bc2d-84b573b8c02a" />

this the ping is successfull and use of ipconfig command has been done


