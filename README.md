# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
Name:Infancia Felcy P
Reg No:212223040067
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client>")
 s.send(msg.encode())
 print("Server>",s.recv(1024).decode())
```
Server:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
   ClientMessage=c.recv(1024).decode()
   c.send(ClientMessage.encode())
```
## OUTPUT
Client:
![image](https://github.com/user-attachments/assets/1ac6d650-506d-4f9f-a8ec-1a9c3cdddac8)

Server:
![image](https://github.com/user-attachments/assets/26785326-6dea-4601-8a87-7022a7403ccf)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
