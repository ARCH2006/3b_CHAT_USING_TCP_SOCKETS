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
# client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
# server:
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
# client:
![Screenshot 2024-10-20 151723](https://github.com/user-attachments/assets/9eb25ac6-7f9c-45a6-bc76-319dc888b1a1)
# server:
![Screenshot 2024-10-20 151734](https://github.com/user-attachments/assets/e533777f-7436-4886-921d-a4f5ec6c66d6)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
