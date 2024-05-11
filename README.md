# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
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
client
```
Thanjiyappan k
212222240108

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
server
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
## OUPUT
client![Screenshot 2024-05-11 164104](https://github.com/vijayr21/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149347607/d4b8c224-be65-4db2-b420-35fab51f598e)
server![Screenshot 2024-05-11 164111](https://github.com/vijayr21/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149347607/50fee020-540d-483f-bd50-aad397e68061)
## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
