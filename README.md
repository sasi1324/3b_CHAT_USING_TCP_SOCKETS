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
## client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## server:
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

## OUTPUT
## client:
![Screenshot 2024-04-14 214220](https://github.com/praveen2p/3b_CHAT_USING_TCP_SOCKETS/assets/151658061/e0650656-4d5f-4eb5-b6ce-70fa2b9c8155)

## server:
![Screenshot 2024-04-14 214233](https://github.com/praveen2p/3b_CHAT_USING_TCP_SOCKETS/assets/151658061/dd8296af-dae4-41f6-bd40-5641a21f1257)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
