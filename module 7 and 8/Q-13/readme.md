question 13:
------------
Try Static NAT, Dynamic NAT and PAT to translate IPs

Answer:
-------

Dynamic NAT:
----------- 

used topology...

<img width="829" height="354" alt="image" src="https://github.com/user-attachments/assets/7ba462c6-af7e-4c81-9945-bf7896cc706b" />

outbound pdu with translated IP address ...

<img width="821" height="430" alt="image" src="https://github.com/user-attachments/assets/f5320538-0c5b-4dc7-818c-a1989d32253f" />

dynamic nat table of router0 ...

<img width="478" height="187" alt="image" src="https://github.com/user-attachments/assets/dada00ba-e809-41d5-bfb4-44e221e31709" />

PAT implementation for the same network on interface Gig 0/1 ...

<img width="1536" height="562" alt="image" src="https://github.com/user-attachments/assets/1455e0f5-0288-44a8-a3fb-33533da701c0" />
<img width="460" height="148" alt="image" src="https://github.com/user-attachments/assets/48c8abc6-f2e6-493b-b077-b3c67e1e2e96" />

SNAT implementation on Gig0/1...

<img width="496" height="162" alt="image" src="https://github.com/user-attachments/assets/8e315697-c4af-4a95-b8bf-067e92308697" />
<img width="1540" height="438" alt="image" src="https://github.com/user-attachments/assets/f5c8fd13-c5af-4c02-94c5-d7058f7bdebd" />

