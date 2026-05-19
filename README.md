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
```
Client side:

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

 Server side:

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
Client side:

<img width="881" height="287" alt="Screenshot 2026-05-19 112620" src="https://github.com/user-attachments/assets/b12c45c2-bb8b-4ccd-bc93-c392c1278ddf" />

Server side:

<img width="847" height="257" alt="Screenshot 2026-05-19 112722" src="https://github.com/user-attachments/assets/7aa4d3c1-6792-4f98-bec8-84855ec30bc8" />


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
