![Image](https://github.com/user-attachments/assets/bdb5f8da-92d8-4099-a375-d94bbd543027)

FTP means file transfer protocol. Usually, it is used to upload or download files from servers via TCP. If a vulnerable IP or host is discovered, a ftp shell can be entered as shown above. Sometimes, certain nmap scan commands will automatically connect.
ftp test.rebex.net
name: anonymous
skip password
enter ftp shell

![Image](https://github.com/user-attachments/assets/20df8d69-195d-41c1-8b3b-ab6ad6cbdd17)
![Image](https://github.com/user-attachments/assets/ad3a7d9e-df89-43a9-aa3e-8b4e1329a60b)

While dated and unsecure, telnet allows for the connection to remover servers over TCP in the command line. Oftentimes, these plain text communications can be manipulated.
telnet freechess.org

![Image](https://github.com/user-attachments/assets/29d25340-679a-418a-b3e6-3f7face263a2)

Smb allows for file sharing between Windows systems. Smbclient allows Linux systems to connect to those same shares. Similarly to FTP, certain nmap scan commands will automatically connect with vulnerable targets.
smbclient -L {ip} -N
enter smb shell
