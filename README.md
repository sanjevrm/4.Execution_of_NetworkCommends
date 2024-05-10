
# 4.Execution_of_NetworkCommands
## Name:Sanjev R M
## REG NO:212223040186
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege de
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## PING COMMAND
## AIM:
To write the python program for simulating ping command.
## ALGORITHM:
Step 1: start the program

Step 2: Include necessary package in java.

Step 3: To create a process object p to implement the ping command.

Step 4: declare one Buffered Reader stream class object.

Step 5: Get the details of the server

 5:1: length of the IP address.

 5:2: time required to get the details.
 
 5:3: send packets, receive packets and lost packets. 
 
 5.4: minimum, maximum and average times.

Step 6: print the results. 

Step 7: Stop the program.
## PROGRAM:
### CLIENT:
```pyton
import socket
from pythonping import ping
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    hostname=c.recv(1024).decode()
    try:
        c.send(str(ping(hostname, verbose=False)).encode())
    except KeyError:
        c.send("Not Found".encode())
```
### SERVER:
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 ip=input("Enter the website you want to ping:")
 s.send(ip.encode())
 print(s.recv(1024).decode())
```
## Output
### CLIENT:
![image](https://github.com/sanjevrm/4.Execution_of_NetworkCommends/assets/155142423/3856094b-c5a4-4c65-8cdf-478935f72874)


### SERVER:
![image](https://github.com/sanjevrm/4.Execution_of_NetworkCommends/assets/155142423/d2e2aece-ec75-40a1-8e48-ffcafb327cf3)


## TRACEROUTE COMMAND
## AIM:
To write the python program for simulating ping command.
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user.
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client
otherwise it will sendNACK signal to client.
6. Stop the program
## PROGRAM:
```python
from scapy.all import*
target = ["www.google.com"]
result, unans = traceroute(target,maxttl=32)
print(result,unans)
```
## Output
![image](https://github.com/sanjevrm/4.Execution_of_NetworkCommends/assets/155142423/2fdc8cae-e45f-4f62-9e2e-351fd9ec3d97)



## Result
Thus Execution of Network commands Performed 
