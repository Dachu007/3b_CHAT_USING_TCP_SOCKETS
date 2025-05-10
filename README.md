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
Client
```
 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
```

Server
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

Client
![Screenshot 2025-05-10 115206](https://github.com/user-attachments/assets/ed35d67b-f589-455d-ad96-e8985e7c539e)

Server
![Screenshot 2025-05-10 115217](https://github.com/user-attachments/assets/0bda9dec-d086-4ff0-b608-debd162f8143)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
