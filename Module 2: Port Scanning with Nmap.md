![Image](https://github.com/user-attachments/assets/eb668557-9efd-4166-81bf-3acaa40c3c74)

Nmap scans show two ports open both allowing the usage of  ‘tcp’. While open, they do say ‘tcpwrapped’ which usually hints at traffic being filtered or blocked through these ports with firewalls or other protections. HTTPS is a secure transfer protocol and encrypts data between client and server.
Nmap -sV allows service versions to be discovered along with the scan.

![Image](https://github.com/user-attachments/assets/e816bb86-8683-49ca-85db-593fffd63b16)

Nmap -sS performs a three-way handshake and tries to establish a tcp connection without making too much “noise’”.
Nmap -sU searches for UDP protocols and may be less stealthy by being faster and a little less secure.
Nmap -O finds out what operating system the target is utlizing. 

![Image](https://github.com/user-attachments/assets/cfd8d217-0b03-448c-891c-d6c6769b693e)
Nmap -Pn does not ping the target in the regular way. To avoid detection and even sometimes get around firewalls, it will assume that the target is up.
