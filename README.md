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
## CLIENT
import socket

s=socket.socket()

s.bind(('localhost',8000))

s.listen(5)

c.addr=s.accept()

while true:
       i=input("Enter Data:  ")
       
       c.send(i.encode())

       ack=c.recv(1024).decode()

       if ack:

          print(ack)
          continue
       else

        c.close()

        break

## SERVER

import socket

s=socket.socket()

s.connect(('localhost',8000))

while True:

      print(s.recv(1024).decode())
      
      s.send("Acknowledgement Received"encode())

       

## OUTPUT
CLIENT 
![1a client](https://github.com/PREETHI3312/2a_Stop_and_Wait_Protocol/assets/151625222/41f464a4-9344-4554-876d-6a1c436ed2af)
SERVER
![1a server](https://github.com/PREETHI3312/2a_Stop_and_Wait_Protocol/assets/151625222/73b1e3f6-8f3a-4067-9977-2e6318cd118c)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
