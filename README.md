## APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER
## EXP : 9
## DATE : 03-05-2023
## AIM :
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM :
## Client :
```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the Socket module in server
4.Send and receive the message using the send function in socket.
```
## PROGRAM :
## CLIENT :
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```   
## SERVER :
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
## CLIENT OUTPUT :
![ex 9 cl output](https://github.com/MrSanthosh-dev/EX-9/assets/117916573/6cbf31e2-97a0-4c98-ae16-58933f7ca6b9)


## SERVER OUTPUT :

![ex 9 se output](https://github.com/MrSanthosh-dev/EX-9/assets/117916573/867a50ca-6996-433b-b9d7-e8d48e5bb4ec)

## RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed
