# 2a_Stop_and_Wait_Protocol
## Name: VESHWANTH.
## REG NO: 212224230300
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
     Client:
     import socket
     s=socket.socket()
     s.bind(('localhost',9000))
     s.listen()
     c,addr=s.accept()
     while True:
          i=input("Enter the Data:")
          c.send(i.encode())
          ack=(c.recv(1024).decode())
          if ack:
             print(ack)
             continue
          else:
             c.close()
             break    

             
         Server:
             import socket
             s=socket.socket()
             s.connect(('localhost',9000))
             while True:
                 print(s.recv(1024).decode())
                 s.send("Acknowledgement Received".encode())
    




## OUTPUT
![Screenshot 2025-03-29 104616](https://github.com/user-attachments/assets/5396dfbe-2f25-4965-906f-d2746602b251)
![Screenshot 2025-03-29 104642](https://github.com/user-attachments/assets/84fb4914-5afa-4b3f-8098-b1bda3403f8e)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
