# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
# client:
```
import socket

s=socket.socket()

s.connect(('localhost',65124))

while(1):

  msg=input("Client>")

  s.send(msg.encode())

  print("Server>"+s.recv(1024).decode())

```
# server:
```

import socket

s=socket.socket()

s.bind(('localhost',65124))

s.listen(5)

c,addr=s.accept()

while(1):

   msg=c.recv(1024).decode()

   print(msg)

   c.send(msg.encode())

```
## OUTPUT:

# SERVER:
![eth echoserver2](https://github.com/user-attachments/assets/bcb039ef-f526-4e13-9acd-71bb7d258dc6)

# CLIENT:
![eth echoserver1](https://github.com/user-attachments/assets/b74a7dfe-2eab-42a8-b422-35ed03ee96b7)


## RESULT:
The program is executed successfully
