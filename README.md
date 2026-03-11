# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name:Shreenidhi 
## Ref.no:212225040410
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
server
~~~
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
~~~
client
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())

~~~
## OUPUT
server

<img width="625" height="253" alt="Screenshot 2026-03-11 135622" src="https://github.com/user-attachments/assets/624eaeb1-8b31-4f0d-9e85-b5de295866b2" />
client 

<img width="616" height="275" alt="Screenshot 2026-03-11 135632" src="https://github.com/user-attachments/assets/84c67864-bc0f-43db-bf14-eeec98c28b21" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
