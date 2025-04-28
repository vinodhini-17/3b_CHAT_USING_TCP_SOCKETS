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

CLIENT:

       client.py
       import socket 
       s=socket.socket() 
       s.connect(('localhost',8000)) 
       while True: 
           msg=input("Client > ") 
           s.send(msg.encode()) 
           print("Server > ",s.recv(1024).decode())
 SERVER:

      server.py
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

## OUPUT

![386929854-2d209d29-5d17-4fb7-8237-163e96b92e4c](https://github.com/user-attachments/assets/7d170831-5c88-4cae-bc52-a553b1f65cf3)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
