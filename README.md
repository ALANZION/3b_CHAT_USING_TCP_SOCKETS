# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## NAME:ALAN ZION H
## REG:212223240004
## SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())

```
### CLIENT : 
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

```
## OUTPUT:
### SERVER : 
![image](https://github.com/user-attachments/assets/134a497a-3eaa-42a7-8e99-c534081b9b18)


### CLIENT: 
![image](https://github.com/user-attachments/assets/6553534f-e1e3-46b8-af94-c10caca7935a)



## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
