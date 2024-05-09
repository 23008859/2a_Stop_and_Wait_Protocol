# 2a_Stop_and_Wait_Protocol
## Name:Roshini
## Reg.No:212223230174
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
## CLIENT:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
   print(ack)
   continue
 else:
   c.close()
   break
```
## SERVER:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())

```

## OUTPUT
## CLIENT:
![image](https://github.com/23008859/2a_Stop_and_Wait_Protocol/assets/139117979/721db885-78ee-4523-8de3-fb3f2d7861a7)
## SERVER:
![image](https://github.com/23008859/2a_Stop_and_Wait_Protocol/assets/139117979/0f6868c4-3870-4786-b9c9-4c4a8bd74675)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
