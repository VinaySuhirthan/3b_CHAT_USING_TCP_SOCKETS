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
## CLIENT:
```python
Developed by: K S VINAY SUHIRTHAN
Reg no: 212224230305
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## SERVER:
```python
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
![image](https://github.com/user-attachments/assets/fbf20e02-2e8e-43e6-9a59-ff7562eec872)

![image](https://github.com/user-attachments/assets/0170eba8-26a2-4463-a9ff-816300e6adfb)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
