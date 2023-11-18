# get-ip-ish-app
get your ip in network in ish app using python 

This script create by [Abo5](https://github.com/Abo5) using python 

To get your ip in ish app do this steps 

Usage:

```
cat > get-my-ip.py
```

```
import socket

#creating a socket object
s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)

#sending a dummy packet to a public DNS server
s.connect(("8.8.8.8", 80))

#getting the local IP address
ip = s.getsockname()[0]

#printing the IP address
print("Your IP address is:", ip)

#closing the socket connection
s.close()
```
and run the script 

```
python3 get-my-ip.py
```

output is 

```
Your IP address is: 192.168.1.100
```
