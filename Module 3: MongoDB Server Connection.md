Module 3: MongoDB

MongoDB was not able to be started on my Kali machine. Numerous attempts at troubleshooting this problem were made. Multiple attempts at removing, wiping, and reinstalling were done as well.
sudo apt install mongodb
Error: Sub-process /usr/bin/dpkg returned an error code (1)
sudo apt --fix-broken install
sudo dpkg --configure -a
sudo apt clean
sudo apt update
sudo apt upgrade
─$ sudo systemctl status mongod
Unit mongod.service could not be found.
sudo apt autoremove
─$ sudo systemctl status mongod
Unit mongod.service could not be found.
sudo apt install -f 
─$ sudo systemctl status mongod
Unit mongod.service could not be found.
Apparently, my CPU could not run the latest version of MongoDB, so I get out to fix that by installing it another way.
curl -fsSL https://www.mongodb.org/static/pgp/server-4.4.asc | sudo gpg --dearmor -o /usr/share/keyrings/mongodb-archive-keyring.gpg
echo "deb [ arch=amd64 signed-by=/usr/share/keyrings/mongodb-archive-keyring.gpg ] https://repo.mongodb.org/apt/debian buster/mongodb-org/4.4 main" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list > /dev/null
sudo apt update
sudo apt update
sudo apt install -y mongodb-org
Unit mongod.service could not be found.
Numerous forums were looked through, official MongoDB guides were also attempted. These databases could not be worked on at this stage. However, Hack the Box provided testing instances that covered traversing through databases. This was covered in Module 4.
