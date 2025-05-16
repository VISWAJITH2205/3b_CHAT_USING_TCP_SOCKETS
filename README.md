# NAME : VISWAJITH LALITHRAM R.V
# REG.NO : 212224240187

---

# 3b.CREATION FOR CHAT USING TCP SOCKETS

---

## AIM :
To write a python program for creating Chat using TCP Sockets Links.

---

## ALGORITHM:

1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.

---

## PROGRAM :

CLIENT :

```
import socket
s=socket.socket()
s.connect(('localhost',9000))
while True:
msg=input("Client > ")
s.send(msg.encode())
print("Server > ",s.recv(1024).decode())

```

SERVER :

```
import socket
s=socket.socket()
s.bind(('localhost',9000))
s.listen(5)
c,addr=s.accept()
while True:
ClientMessage=c.recv(1024).decode()
print("Client > ",ClientMessage)
msg=input("Server > ")
c.send(msg.encode())
```

---

## OUPUT :

CLIENT :

![CLIENT3B](https://github.com/user-attachments/assets/cd3c1c06-0c3c-479b-8e31-3f96f7fd976f)



SERVER :

![SERVER3B](https://github.com/user-attachments/assets/8a832cf4-0b4f-41fc-bb2e-977bba00be2f)


---

## RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
