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
```
if data:
    print(f"Received: {data}")
    conn.send("ACK".encode())

    if data.lower() == 'exit':  
        print("Connection closed by client")
        conn.close()
        break

client.send(msg.encode())
```

```
if msg.lower() == 'exit':  
    print("Connection closed by client")
    client.close()
    break

try:
    ack = client.recv(1024).decode()
    if ack == "ACK":
        print(f"Server acknowledged: {ack}")
except socket.timeout:
    print("No ACK received, retransmitting...")
    continue  
```
## OUTPUT
<img width="783" height="212" alt="Screenshot 2025-09-22 175805" src="https://github.com/user-attachments/assets/c65b2ac8-d296-43ff-8995-38436def34d5" />

<img width="791" height="345" alt="Screenshot 2025-09-22 175754" src="https://github.com/user-attachments/assets/19a1979d-77b7-4ff2-84b9-409dcd047629" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
