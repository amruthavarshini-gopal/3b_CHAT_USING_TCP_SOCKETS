# 3b.CREATION FOR CHAT USING TCP SOCKETS


## AIM:

To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM:

1. Import the necessary modules in python

2. Create a socket connection to using the socket module.

3. Send message to the client and receive the message from the client using the Socket module in
 server

4. Send and receive the message using the send function in socket.

## PROGRAM:

```
CLIENT

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
```
SERVER

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

## OUTPUT:

### CLIENT

![Screenshot 2024-10-20 124740](https://github.com/user-attachments/assets/5dd0c37d-d384-4729-8660-0e25d0e43f44)

### SERVER

![Screenshot 2024-10-20 124759](https://github.com/user-attachments/assets/ea736c04-2458-463a-ac5b-f7229ab42bb9)


## RESULT:

Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
