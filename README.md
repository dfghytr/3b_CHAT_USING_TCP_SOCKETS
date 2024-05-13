# Name: Abdul kalaam K M
# Ref no: 212223230003

# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
```
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
```
## PROGRAM
# Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```
# Server
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

## OUPUT
# Client
![image](https://github.com/ramanpiritha/3b_CHAT_USING_TCP_SOCKETS/assets/147084116/cf17f7a9-8c0f-43ca-b4e7-bfb6837630d7)
# Server
![image](https://github.com/ramanpiritha/3b_CHAT_USING_TCP_SOCKETS/assets/147084116/eae4ba2a-8dd3-4dae-b2a7-0c6d1c305bf8)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
