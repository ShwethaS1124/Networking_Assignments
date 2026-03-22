KALI VM TERMINAL OUTPUT ( telnet - server):
-------------------------------------------                                           

                                                                     
┌──(kali㉿kali)-[~/Desktop]
└─$ sudo service xinetd restart             

                                                                                                                   
┌──(kali㉿kali)-[~/Desktop]
└─$ sudo netstat -tulpn | grep :23

tcp6       0      0 :::23                   :::*                    LISTEN      82300/xinetd        
                                                                                                                   
┌──(kali㉿kali)-[~/Desktop]
└─$ hostname -I
192.168.1.4 2401:4900:1ce2:1b88:681:2083:4e1e:1c1e 2401:4900:1ce2:1b88:a00:27ff:fed8:50e3 

(after connecting) 
                                                                                                                   
┌──(kali㉿kali)-[~/Desktop]
└─$ sudo netstat -tnp | grep ESTABLISHED  

tcp        0      0 192.168.1.4:23          192.168.1.5:40390       ESTABLISHED 83295/telnetd       
                                                                                                                   
┌──(kali㉿kali)-[~/Desktop]
└─$ 


--------------------------------------------------------------------------------------------------




