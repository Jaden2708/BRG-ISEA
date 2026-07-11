# Lab 3 ISEA
## 3a-1 Domain, DNS, and TLS certificates
### Activity 1
### Domain name registered
Here, my domain name is registered on Duck DNS
<img width="1261" height="109" alt="3a1 1 1" src="https://github.com/user-attachments/assets/ffd819c2-dac2-4425-a008-f8c509525fe1" />

### A record created
Here, a DNS A record was created, pointing to my amazon web server ip address
<img width="1271" height="384" alt="3a1 2 1" src="https://github.com/user-attachments/assets/ad93d45b-900c-43fe-8059-bb9886549a1a" />

### Apache installed
Here is my terminal showing apache is installed and accessible via port 80
The commands I used are
```bash
sudo systemctl status apache2
sudo ss -tulnp | grep :80
```
<img width="975" height="290" alt="3a1 3 1" src="https://github.com/user-attachments/assets/e0aca95b-2ca0-4751-9f5f-759f11b1cb09" />
<img width="1362" height="62" alt="3a1 3 2" src="https://github.com/user-attachments/assets/5d091ab5-30e2-4fe6-927d-e6af62ce325e" />

### Public IP to Domain mapping verified
Here I will test DNS is working using browser, dig, nslookup. 
The commands I used are
```bash
nslookup jadenwebapp.duckdns.org
dig jadenwebapp.duckdns.org
```
<img width="913" height="550" alt="3a1 4 1" src="https://github.com/user-attachments/assets/a6484ac8-1949-4d7b-903f-74c44b8d0d78" />
<img width="631" height="153" alt="3a1 4 2" src="https://github.com/user-attachments/assets/48f84047-f349-4be1-b923-979f9a103a7f" />
<img width="624" height="396" alt="3a1 4 3" src="https://github.com/user-attachments/assets/64ddf2cc-6885-48f9-baa5-877b41f31a17" />

### Screenshot: Apache Welcome Page via Domain 
Here is the Apache Welcome Page via Domain name
<img width="919" height="447" alt="3a1 5 1" src="https://github.com/user-attachments/assets/067f380b-faed-4782-aa04-d9775a333098" />

### Screenshot: DNS Test Output 
Here I will test DNS output using nslookup and dig
The commands I used are 
```bash
nslookup jadenwebapp.duckdns.org
dig jadenwebapp.duckdns.org
```
<img width="631" height="153" alt="3a1 4 2" src="https://github.com/user-attachments/assets/36abb8ef-5e12-47e6-a445-4ca3f4d9bd8e" />
<img width="624" height="396" alt="3a1 4 3" src="https://github.com/user-attachments/assets/657a3706-de83-4c42-a743-e503c39ff5dd" />

## Activity 2
### Certbot installed
Here I show that certbot and apache is installed using snap
<img width="791" height="492" alt="3a1 8 1" src="https://github.com/user-attachments/assets/e9050e0c-df8b-43d7-bee4-c5b6cf75ad37" />
<img width="1088" height="283" alt="3a1 8 2" src="https://github.com/user-attachments/assets/78efbe47-b44f-4613-8e21-9f730ae976bd" />

### HTTPS Enabled on Domain 
Here I will show that my domain is secure
<img width="1744" height="761" alt="3a1 9 1" src="https://github.com/user-attachments/assets/116666d0-3360-4583-9a71-cacc3bdb2a07" />

### Valid TLS Certificate 
Here is my valid TLS Certificate that is viewed from a browser
<img width="535" height="657" alt="3a1 10 1" src="https://github.com/user-attachments/assets/7ab96ca2-6b51-469f-93b5-cae789354029" />

### Screenshot: HTTPS with Lock Icon 
Here is a screenshot from my browser showing the lock icon and certificate issuer
<img width="1658" height="722" alt="3a1 11 1" src="https://github.com/user-attachments/assets/dd947702-f20f-40f9-80ce-858ab416c167" />

### Screenshot: Certbot Success Message 
Here is the certbot success message
The command I use is
```bash
sudo certbot --apache
```
<img width="1154" height="368" alt="3a1 12 1" src="https://github.com/user-attachments/assets/7586b020-0249-4cd6-8ed9-f4df839752ce" />

### Screenshot: Renewal Dry-Run Output 
Output of sudo certbot renew --dry-run showing success 
The command I used is
```bash
sudo certbot renew --dry-run
```
<img width="739" height="319" alt="3a1 13 1" src="https://github.com/user-attachments/assets/21d1c86e-3f5e-418c-a356-a79467d91413" />

### 3a-1 Reflection questions
- What is the role of DNS in Internet presence? 
The role of dns in Internet presence is to allow users to access a website using a domain name instead of remembering an IP address.

- Why does DNS propagation take time? 
DNS propagation takes time as DNS records are stored and cached by different DNS servers globally. 

- How does Let’s Encrypt validate domain ownership?
  Let's Encrypt checks that the user requesting the certificate controls the domain. It does this by placing a temporary file on the web server, and tries to visit the domain. If the file is reachable from the internet, it proves that the domain points to your server and the certificate is issued.

- What are the risks if TLS is not configured on a public-facing site?
  If TLS is not configured on a public facing site, data between the user and website would not be encrypted. This would allow attackers to intercept or modify information being sent.

- What could happen if you leave your cloud VM running for months?
  If you leave your cloud VM running for months, it can cause extra charges to be paid, and increases security risk as it is exposed to the internet. 

## 3ba-2 Enabling HTTPS with Let's Encrypt & Certbot
### Pre-Condition Verified: Domain Points to Server
Show that the domain name is linked via DNS A record to the VM and accessible via http://yourdomain.com. 
<img width="1271" height="384" alt="3a1 2 1" src="https://github.com/user-attachments/assets/af56f196-a66d-448e-8882-657b5ec58c68" />
<img width="919" height="447" alt="3a1 5 1" src="https://github.com/user-attachments/assets/da340a3d-11cd-4ff8-b8ba-d19cbee7e687" />

### Certbot Installed via Snap 
Confirm installation of Certbot using the Snap package manager. Command: sudo snap install --classic certbot
<img width="791" height="492" alt="3a1 8 1" src="https://github.com/user-attachments/assets/e38998fa-d52c-42e8-ac31-1cd105610945" />

### Certificate Successfully Issued
Output of sudo certbot --apache showing that Let’s Encrypt issued a certificate for your domain. 
<img width="1154" height="368" alt="3a1 12 1" src="https://github.com/user-attachments/assets/8e667816-185d-4c17-971f-281f61320c22" />

### HTTPS Enabled on Apache
Apache has been reconfigured to support HTTPS, typically through Certbot’s automation.
<img width="1744" height="761" alt="3a1 9 1" src="https://github.com/user-attachments/assets/8b613b94-4ba2-4935-bf9b-97dc0afefb84" />

### Browser Lock Icon (Secure Connection) 
<img width="1744" height="761" alt="3a1 9 1" src="https://github.com/user-attachments/assets/5b75712f-f910-4a65-95bd-16b8987cb495" />

### View Certificate Issuer
<img width="535" height="657" alt="3a1 10 1" src="https://github.com/user-attachments/assets/d0c5c339-e920-4a0f-8889-8823a2a34a5f" />

### Certbot Auto-Renewal Dry Run Successful
Output of sudo certbot renew --dry-run showing “Congratulations, all renewals succeeded.” 
<img width="739" height="319" alt="3a1 13 1" src="https://github.com/user-attachments/assets/2838d784-f413-41a2-b26e-be36a86d0f32" />

### 3b-2 Reflection Questions
Why is HTTPS important for modern web applications? 
HTTPS is important for modern web applications as it encrypts the connection between the user and the web server. This protects data from being intercepted or modified by attackers.

What entity issued your site’s TLS certificate? 
Let's Encrypt issued my site's TLS certificate.

How long is your certificate valid for, and how can it be renewed? 
The certificate is vaild for 90 days and can be renewed by cron job.

What happens if a certificate expires and is not renewed? 
If a certificate expires and is not renewed, the browser would show a security warning when users visit the site, HTTPS protection will no longer be trusted.

Why does Let’s Encrypt require port 80 or 443 to be open for verification? 
Let's Encrypt requires port 80 or 443 to be open as it needs to connect to the site to ensure that the domain points to my the server.

## 3b-1 Bash Backup Scripting, Cron Jobs & Cloud Export
### Practice Bash Commands Executed 
Output or screenshots showing: 
• echo, variables 
• Arithmetic with (( )) 
• Basic for loop summation 
Commands used
```bash
echo "Hello"

name="Jaden"
echo "My name is $name"

a=10
b=5
((sum=a+b))
((difference=a-b))
((product=a*b))
((division=a/b))
echo "a = $a"
echo "b = $b"
echo "Sum = $sum, Difference = $difference, Product = $product, Division = $division"

total=0
for i in 1 2 3 4 5
do
    echo "Adding $i"
    ((total=total+i))
done

echo "Final total is $total"
```
<img width="1024" height="577" alt="3b1 1 1" src="https://github.com/user-attachments/assets/67261d62-e5f4-4f97-988d-3607278ccd39" />

### Test Files & Directories Created 
Screenshot of terminal showing files and folders in /home/ubuntu/Documents/ using ls -R 
Commands used
```bash
mkdir -p /home/ubuntu/Documents/folder1
mkdir -p /home/ubuntu/Documents/folder2
echo "This is file 1" > /home/ubuntu/Documents/file1.txt
echo "This is file 2 inside folder1" > /home/ubuntu/Documents/folder1/file2.txt
echo "This is file 3 inside folder 2" > /home/ubuntu/Documents/folder2/file3.txt
echo "This is another test file" > /home/ubuntu/Documents/folder2/file4.txt

ls -R /home/ubuntu/Documents
```
<img width="944" height="397" alt="3b1 2 1" src="https://github.com/user-attachments/assets/ab34150f-6967-4032-a9d7-85bdacd1cec0" />

### Basic Script Working (testscript) 
File /home/ubuntu/testscript created and tested with: 
• Recursive copy from Documents to /home/ubuntu/backup/ 
• Script has execute permission (chmod 777) and produces expected output
Commands used
```bash
nano testscript
chmod 777 /home/ubuntu/testscript
/home/ubuntu/testscript
ls -l /home/ubuntu/testscript
ls -R /home/ubuntu/backup
```
<img width="820" height="270" alt="3b1 3 1" src="https://github.com/user-attachments/assets/fa809482-4a60-4234-bdd5-8406f3fa1a32" />
<img width="619" height="337" alt="3b1 3 2" src="https://github.com/user-attachments/assets/aef8177a-d774-4d9b-9993-1f30e3706ec4" />

### Script Moved to /usr/bin and Tested 
Output showing: 
• Script moved to /usr/bin/testscript 
• sudo chown applied 
• testscript works from any directory 
Commands used
```bash
sudo cp /home/ubuntu/testscript /usr/bin/testscript
sudo chown root:root /usr/bin/testscript
sudo chmod 777 /usr/bin/testscript

ls -l /usr/bin/testscript

cd / testscript
pwd
ls -R /home/ubuntu/backup
```
<img width="715" height="500" alt="3b1 4 1" src="https://github.com/user-attachments/assets/071403f3-8df2-43ce-b45e-f468a75129e1" />

### ZIP Archive with Date Filename 
Script updated to: 
• Use zip -r to archive backup 
• Use now=$(date +"%d_%m_%y") to name the ZIP file 
• Screenshot of dated ZIP in /home/ubuntu/ 
Commands used
```bash
sudo apt update
sudo apt install zip -y
sudo nano /usr/bin/testscript
testscript
ls -lh /home/ubuntu/*.zip
```
<img width="943" height="707" alt="3b1 5 1" src="https://github.com/user-attachments/assets/72186d3a-b841-4492-9d64-6b20c59a5530" />
<img width="519" height="456" alt="3b1 5 2" src="https://github.com/user-attachments/assets/1059a02e-e09a-4b51-b5c4-64d0ae6181ce" />
<img width="687" height="401" alt="3b1 5 3" src="https://github.com/user-attachments/assets/f5cc0070-6131-4e79-b276-76ee11b4c7f2" />

### Cronjob Set Up for Hourly Backup 
Screenshot or output of /etc/crontab edited to include: 
9 * * * * ubuntu /usr/bin/testscript or similar hourly cron job 
Commands used
```bash
sudo nano /etc/crontab
sudo systemctl status cron
tail -n 10 /etc/crontab
```
<img width="931" height="258" alt="3b1 6 1" src="https://github.com/user-attachments/assets/44c643b7-c8ad-4623-b771-5bb4f3cef502" />
<img width="954" height="545" alt="3b1 6 2" src="https://github.com/user-attachments/assets/e79ab027-df75-480f-adb3-f99e630ee09d" />
<img width="939" height="230" alt="3b1 6 3" src="https://github.com/user-attachments/assets/10108d09-b6fc-4b61-9772-653cfae65d5b" />


### Successful Cron Execution Verified 
Evidence that the script runs every hour: 
• ZIP file created hourly 
• Timestamps or ls -lh output confirming multiple backups created 
<img width="669" height="60" alt="3b1 7 1" src="https://github.com/user-attachments/assets/5800ed3c-0448-49e3-b3f4-e25e955a3acd" />

### SCP to Cloud Working 
Script contains a line using: 
scp -i key.pem $now.zip ubuntu@<server>:~/ 
• Confirmed file reached cloud VM (ls ~/ on remote server) 
Commands used
```bash
cd C:\Users\User\Desktop
scp -i "aws-ubuntu-key1.pem" ubuntu@3.81.214.1:/home/ubuntu/*.zip .
dir *.zip
scp -i "aws-ubuntu-key1.pem" "11_07_26.zip" ubuntu@3.81.214.1:/home/ubuntu/
ls -lh /home/ubuntu/*.zip
```
<img width="826" height="287" alt="3b1 8 1" src="https://github.com/user-attachments/assets/9114959d-07a9-4ea9-88e5-bfb461e4e167" />
<img width="838" height="559" alt="3b1 8 2" src="https://github.com/user-attachments/assets/583e3916-31d2-4dad-aead-288b279116b8" />
<img width="684" height="136" alt="3b1 8 3" src="https://github.com/user-attachments/assets/b981b876-785f-4073-9647-a15ed994cca4" />

### SSH Certificate Accepted by Root 
Output of sudo ssh -i key.pem ... showing manual acceptance of SSH key fingerprint 
Commands used
```bash
scp -i "aws-ubuntu-key1.pem" "aws-ubuntu-key1.pem" ubuntu@3.81.214.1:/home/ubuntu/aws-ubuntu-key1.pem
chmod 400 /home/ubuntu/aws-ubuntu-key1.pem
sudo ssh -i /home/ubuntu/key.pem ubuntu@3.81.214.1
```
<img width="536" height="382" alt="3b1 9 1" src="https://github.com/user-attachments/assets/25299dea-0b3e-446b-ae46-3915e4203505" />

### Final Script Submitted 
Full contents of script provided, with: 
• Dated ZIP backup 
• SCP transfer 
• Full paths used for cron 
```bash
cat /usr/bin/testscript
```
<img width="862" height="327" alt="3b1 10 1" src="https://github.com/user-attachments/assets/2a9d3acb-25e5-446d-8dc8-6296537d934e" />
<img width="868" height="347" alt="3b1 10 2" src="https://github.com/user-attachments/assets/524a3637-a126-44b3-82fd-ddcd4f2b8ea6" />
<img width="931" height="219" alt="3b1 10 3" src="https://github.com/user-attachments/assets/e69a3c61-c2f5-4b57-9473-a46bed88f0c9" />




### 3b-1 Reflection Questions
Why is using absolute paths important in scripts run by cron? 
Using absolute paths is important in scripts run by cron as cron runs scripts in a limited environment. If relative paths are used, the script may not find the correct files or folders.

What are the benefits of cloud exporting for backups? 
Cloud exporting for backup keeps the files in a separate location. This is useful as the backup still exists elseware incase of a system failure.

How does cron differ from manual execution? 
Cron runs the script automatically at a scheduled time while manual execution requires the user to run the scripts by themselves.

What happens if SSH keys are not accepted ahead of time? 
if SSH keys are not accepted ahead of time, it might cause automated cron jobs to fail as cron is unable to continue. 

How can login messages help improve user/system engagement? 
Login messages help improve usuer/system engagement as it shows that a user is connected to the system successfully. 

## 3b-2 Additional Server Services
### System Preperation
I first updated the system and installed basic prerequisites if needed. There were some errors but I managed to fix them using sudo apt update --fix-missing
Commands used
```bash
sudo apt update
sudo apt update --fix-missing
sudo apt upgrade -y
sudo apt install -y curl wget gnupg lsb-release ca-certificates
```
<img width="793" height="606" alt="3b2 1 1" src="https://github.com/user-attachments/assets/95133af1-9667-4f5c-92c0-b77153313704" />
<img width="791" height="611" alt="3b2 1 2" src="https://github.com/user-attachments/assets/a2fdd9ff-43b2-408f-b1b6-fee9805e1f05" />
<img width="806" height="255" alt="3b2 1 3" src="https://github.com/user-attachments/assets/ebbd1de0-cddf-401c-ae5e-d486fd636937" />
<img width="798" height="612" alt="3b2 1 4" src="https://github.com/user-attachments/assets/0296393f-194d-49b7-a026-c9dc40059f76" />

### Installing Docker in Ubuntu
I first check if docker is installed. Since docker is not installed, I proceed to install docker.
When I tried to run newgrp, I had to install using sudo apt install util-linux-extra
```bash
sudo apt remove -y docker-engine docker.io containerd runc
sudo apt install -y docker.io
sudo systemctl start docker
sudo systemctl enable docker
docker --version
sudo docker run hello-world
sudo usermod -aG docker $USER
newgrp docker
sudo apt install util-linux-extra
```
<img width="795" height="620" alt="3b2 2 1" src="https://github.com/user-attachments/assets/a487c6f4-bb3c-4119-831b-deb789d80e2e" />
<img width="563" height="100" alt="3b2 2 2" src="https://github.com/user-attachments/assets/0d621fc8-9b60-4194-a195-cdc1e88baa5b" />
<img width="646" height="542" alt="3b2 2 3" src="https://github.com/user-attachments/assets/93d822b2-e1c1-4ba6-85d3-bbb321d1d0f9" />
<img width="805" height="605" alt="3b2 2 4" src="https://github.com/user-attachments/assets/f6b5c6e1-0eaf-4924-aaba-20aef63a8140" />

### Installing MariaDB
First I install MariaDB, start and enable MariaDB, and perform a secure MariaDB installation, then verify MariaDB. When I used sudo mysql-secure-installation, it said command not found. Turns out, the command was sudo mariadb-secure-installation instead. 
```bash
sudo apt install -y mariadb-server mariadb-client
sudo systemctl start mariadb
sudo systemctl enable mariadb
sudo mariadb-secure-installation
sudo mysql -u root -p
SHOW DATABASES;
EXIT;
```
<img width="790" height="617" alt="3b2 3 1" src="https://github.com/user-attachments/assets/f9fe0320-178d-4836-a60a-52746b97a7b3" />
<img width="816" height="117" alt="3b2 3 2" src="https://github.com/user-attachments/assets/2948146a-395d-484e-a7f7-4e5b1b3f82d5" />
<img width="795" height="612" alt="3b2 3 3" src="https://github.com/user-attachments/assets/356e7533-3048-444e-b96b-c361f517d289" />
<img width="811" height="248" alt="3b2 3 4" src="https://github.com/user-attachments/assets/239fec2d-e586-4f40-91b8-4db3f0a0463c" />
<img width="414" height="252" alt="3b2 3 5" src="https://github.com/user-attachments/assets/e57f84a6-85c4-4ba1-91b6-74c84b7e8329" />

### Installing Syslog Server
Here I install the Syslog Server. There were no troubles encountered.
```bash
sudo apt install -y rsyslog
sudo systemctl start rsyslog
sudo systemctl enable rsyslog
sudo nano /etc/rsyslog.conf
sudo systemctl restart rsyslog
sudo ufw allow 514/udp
sudo ufw allow 514/tcp
sudo tail -f /var/log/syslog
```
<img width="564" height="144" alt="3b2 4 1" src="https://github.com/user-attachments/assets/4112834d-c7b3-4361-8116-77738baf4899" />
<img width="789" height="620" alt="3b2 4 2" src="https://github.com/user-attachments/assets/1dcc46e1-3d4b-404d-a1b9-ddf26f5a7f89" />
<img width="794" height="528" alt="3b2 4 3" src="https://github.com/user-attachments/assets/67e0ba8c-ac53-4cb5-bce8-c9768907384b" />

### Installing NTP Server
Here I install NTP Server for time synchronisation. No troubles encountered.
```bash
sudo apt update
sudo apt install -y chrony
sudo nano /etc/chrony/chrony.conf
sudo systemctl restart chrony
sudo systemctl enable chrony
chronyc sources
timedatectl
```
<img width="601" height="273" alt="3b2 5 1" src="https://github.com/user-attachments/assets/7cfc7dd8-84b3-4118-bb79-913eec2d2136" />
<img width="785" height="617" alt="3b2 5 2" src="https://github.com/user-attachments/assets/dcf053d7-fa12-44ff-97b4-422535b5a080" />
<img width="798" height="610" alt="3b2 5 3" src="https://github.com/user-attachments/assets/1e4b8277-094c-4fe2-a112-3cda02d1b2a1" />

### DHCP Server
Here I will install DHCP Server and assign the ip
```bash
sudo apt install -y isc-dhcp-server
sudo nano /etc/default/isc-dhcp-server
sudo nano /etc/dhcp/dhcp.conf
sudo systemctl restart isc-dhcp-server
sudo systemctl enable isc-dhcp-server
systemctl status isc-dhcp-server
```
<img width="799" height="618" alt="3b2 6 1" src="https://github.com/user-attachments/assets/b03cfa03-87cb-4347-8ad5-6f0e6a148909" />
<img width="779" height="616" alt="3b2 6 2" src="https://github.com/user-attachments/assets/ba3ab220-cb18-46e1-8137-3fdd84e8864a" />
<img width="776" height="619" alt="3b2 6 3" src="https://github.com/user-attachments/assets/71909d0d-b304-4231-b416-63446e007f1b" />
<img width="807" height="519" alt="3b2 6 4" src="https://github.com/user-attachments/assets/3d595dc2-0c10-4fcf-b26d-d3f544310fdb" />

### Installing NFS Server
Here I will install NFS Server, created shared directory, and configure NFS export
```bash
sudo apt install -y nfs-kernel-server
sudo mkdir -p /srv/nfs/share
sudo chown nobody:nogroup /srv/nfs/share
sudo chmod 777 /srv/nfs/share
sudo nano /etc/exports
sudo exportfs -a
sudo systemctl restart nfs-kernel-server
sudo systemctl enable nfs-kernel-server
showmount -e localhost
```
<img width="805" height="615" alt="3b2 7 1" src="https://github.com/user-attachments/assets/32483b29-bc1f-4f21-8880-bd6622678006" />
<img width="791" height="626" alt="3b2 7 2" src="https://github.com/user-attachments/assets/f1ebffe0-1e3a-4b33-bfad-05df3c8cea7c" />
<img width="803" height="265" alt="3b2 7 3" src="https://github.com/user-attachments/assets/e16563c5-c15b-4f6f-8b09-1b3753c7111a" />

### Installing Samba
Here I will install Samba, create shared folder, configure samba share, and verify. When I tried to run smbclient -L localhost -N, it said I had to install. So i ran sudo apt install smbclient command to install it, then I had no other errors.
```bash
sudo apt install -y samba
sudo mkdir -p /srv/samba/share
sudo chmod 777 /srv/samba/share
sudo nano /etc/samba/smb.conf
sudo systemctl restart smbd
sudo systemctl enable smbd
smbclient -L localhost -N
```
<img width="799" height="615" alt="3b2 8 1" src="https://github.com/user-attachments/assets/90390d83-ca98-4b37-b14c-fc6ec0e96be8" />
<img width="799" height="610" alt="3b2 8 2" src="https://github.com/user-attachments/assets/1a0eb6d1-c258-44a6-8ac6-54605d47f73e" />
<img width="607" height="93" alt="3b2 8 3" src="https://github.com/user-attachments/assets/13e9c22d-22e3-481e-8a12-b86c158c07b3" />
<img width="807" height="229" alt="3b2 8 4" src="https://github.com/user-attachments/assets/0da55484-0c26-497b-a514-5cc06acc0c1c" />
<img width="797" height="571" alt="3b2 8 5" src="https://github.com/user-attachments/assets/debf941e-5c73-4397-af02-ac236172a987" />
