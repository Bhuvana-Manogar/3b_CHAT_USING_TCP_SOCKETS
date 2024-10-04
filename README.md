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
![Screenshot 2024-10-04 110458](https://github.com/user-attachments/assets/f6fc440c-f713-4d33-b236-4ea05f7b9354)

![Screenshot 2024-10-02 115108](https://github.com/user-attachments/assets/0f6605c1-af6b-4d89-a092-9723bdf1936b)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
