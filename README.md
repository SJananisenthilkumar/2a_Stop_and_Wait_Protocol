# 2a_Stop_and_Wait_Protocol
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
Developed by : JANANI S

Register Number : 212223230086
## CLIENT
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
## SERVER
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```
## OUTPUT
## CLIENT
![image](https://github.com/SJananisenthilkumar/2a_Stop_and_Wait_Protocol/assets/144871139/8ebef283-2ea2-4d42-98b5-5012f6c68e0e)
## SERVER
![image](https://github.com/SJananisenthilkumar/2a_Stop_and_Wait_Protocol/assets/144871139/bbf45cba-81e2-4e17-a423-892257d0bad5)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
