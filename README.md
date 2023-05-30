# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## DATE : 02/05/2023

## AIM :
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM :

1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.

## PROGRAM :
### client :
```python
Developed by : Tejusve Kabeer.F
Register no : 212222100054

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```
 ### server :
 ```python
 Developed by : Tejusve Kabeer.F
Register no : 212222100054

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

## OUTPUT :

### clientoutput :
![6co](https://github.com/Reebak04/EX-9/assets/118364993/2797481a-6edf-4cb6-b23f-90896c710e13)

### serveroutput :
![6so](https://github.com/Reebak04/EX-9/assets/118364993/ef99d885-7e1c-47db-8d91-aaced21a5920)

## RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully
created and executed.
