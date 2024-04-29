# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.

   **NAME:SUBHASHINI.B**   
   **REGISTER NUMBER:212223040211**  
## PROGRAM
## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

```
## SERVER
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
## CLIENT
![WhatsApp Image 2024-04-29 at 13 47 22_8923e964](https://github.com/subha-shinibalasubramanian/3b_CHAT_USING_TCP_SOCKETS/assets/164154478/ee099f77-54e2-4cca-99a2-eca3de5c7216)

## SERVER
![WhatsApp Image 2024-04-29 at 13 47 12_cda8a4ad](https://github.com/subha-shinibalasubramanian/3b_CHAT_USING_TCP_SOCKETS/assets/164154478/902d2776-1d5c-4839-ad7d-b5da76a63599)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
