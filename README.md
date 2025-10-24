# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
### NAME   : RAGA SUSANTH
### REF NO : 212224230217
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
# Client:
```py
 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())  
```

# Server:
```py
 
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
## Client:
<img width="1009" height="321" alt="image" src="https://github.com/user-attachments/assets/ae5043cf-feba-435e-a0ca-ee0e6ac06fa8" />

## Server:
<img width="1007" height="330" alt="image" src="https://github.com/user-attachments/assets/94a85b85-470e-47b2-9af5-533d9d6274fa" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
