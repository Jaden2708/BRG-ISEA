# Lab 1a Setting up Ubuntu, VMware and Command Line Familiarisation
## Installing a Virtual Machine


## 1a-1 Virtualisation and Linux setup
### This is the VMware version that I will be using.
<img width="487" height="385" alt="vmware installation" src="https://github.com/user-attachments/assets/582580df-bd0f-47bf-a2f7-b0b5bdab17a2" />

###This is the VMware successfully installed
<img width="729" height="597" alt="vmware homepage" src="https://github.com/user-attachments/assets/63e16325-0029-41c1-95e2-dbe75efbdda4" />

### This is the Ubuntu version that I will be using.
<img width="1798" height="880" alt="Ubuntu installation" src="https://github.com/user-attachments/assets/4375da70-3a67-4cf0-a6d6-895375df7830" />

### This is Ubuntu Successfully intsalled
<img width="749" height="724" alt="Created Ubuntu" src="https://github.com/user-attachments/assets/96fe9b3f-1522-47ef-bda3-d3594b1499fb" />

<img width="1278" height="906" alt="Ubuntu installed in vmware" src="https://github.com/user-attachments/assets/0e6c5816-c399-4b82-804e-a5f36f5e3aba" />
After installing, it should look something like this. 

### This is to show that NAT/Networking Mode is configured
<img width="749" height="724" alt="Ubuntu NAT" src="https://github.com/user-attachments/assets/55191dae-bf06-4ddc-a7db-0055dda8842d" />


<img width="1276" height="850" alt="Ubuntu update complete" src="https://github.com/user-attachments/assets/ddd480db-b7b4-4d15-8f04-5503ee93817f" />
Once installed, I opened up the terminal and updated the system by using the commands
sudo apt update (This is to tell the system to search for the latest updates)
sudo apt upgrade -y (This is to tell the system to proceed with the update)

Package manager is an Advanced Package Tool that helps you install, update, remove, and manage software using the terminal. For example, "sudo apt update" checks for the latest updates.

Repository concept is a online storage where software packages are kept which you can download and install from.

The difference between update and upgrade is that update refreshes the list of available package versions from repositories. While upgrade installs the newer versions of packages already installed in the system.

### This is to show that Ubuntu is running successfully
<img width="643" height="479" alt="Ubuntu running successfully" src="https://github.com/user-attachments/assets/2d0b932d-7e03-4a8e-a35b-025c070a5221" />

### 1a Reflection Questions
What challenges did you encounter during the virtual machine setup?
I encounted a graphics card driver error. I solved it by switching to vmware instead.

What did you learn about virtualisation tools and their differences?
I learnt that there are differernt virtualisation tools that are used for different purposes. A local VM is easier to reset, clone, test, and free. While cloud virtualisation are ahrder to reset, clone, and are usually paid subscriptions.

How confident do you feel using Ubuntu after completing this lab?
I feel more confident as compared to previously as this lab has given me hands on experience.

In what ways can a virtualised Linux environment help in industry scenarios?
A virtualised Linux environment helps in industry scenarios as it allows developers to create safe test environments before deloying live updates. 

What would you do differently if setting up another VM?
I would immediately use vmware as it is more beginner friendly.


# Lab 1a Ubuntu GUI & CLI Familiarisation + Software Installation Methods

## 1a-2 Ubuntu Linux Familiarisation
### GUI Familiarisation
Ubuntu desktop applications such as firefox, File manager, terminal and appstore were explored
<img width="1276" height="849" alt="github in firefox ubuntu" src="https://github.com/user-attachments/assets/707deac6-82a1-4abe-9a22-11394394ad81" />
<img width="1273" height="789" alt="Libre office with text" src="https://github.com/user-attachments/assets/f6fb937d-fdf8-459f-9e28-4d85679e0edc" />
<img width="1276" height="798" alt="Navigating directories file manager" src="https://github.com/user-attachments/assets/5b3a3ff3-3479-4967-a580-6e5e066ba086" />
<img width="1274" height="853" alt="Software Installed" src="https://github.com/user-attachments/assets/ef510bff-1e8a-4e24-905a-df341c4a3ca7" />


### Terminal Commands
These are the commands that I used to explore the Linux environment
```bash
ps -e
top
ls
ls -la
ls -alt
touch
nano
gedit
cat
less
```
<img width="641" height="492" alt="ps -e" src="https://github.com/user-attachments/assets/02e4afb4-df74-40c2-a58a-db7daf6b5647" />
<img width="646" height="476" alt="top" src="https://github.com/user-attachments/assets/79fb6e57-6dd4-493f-88c9-2bec90734237" />
<img width="633" height="481" alt="ls and ls -la" src="https://github.com/user-attachments/assets/6e2c70df-df8d-4414-8254-fb09a68b3ed4" />
<img width="632" height="479" alt="ls -alt" src="https://github.com/user-attachments/assets/5bc6d003-d57d-4850-a6af-405dd8c90564" />
<img width="818" height="411" alt="touch" src="https://github.com/user-attachments/assets/70f25e9c-1abb-4ca2-80e8-001619dcd40a" />
<img width="640" height="484" alt="nano" src="https://github.com/user-attachments/assets/9a49aa67-9fc5-433f-824f-519a79f49706" />
<img width="1269" height="731" alt="gedit" src="https://github.com/user-attachments/assets/8867d05a-dce6-4983-b457-9b68223b50be" />
<img width="650" height="485" alt="cat" src="https://github.com/user-attachments/assets/fbc791da-e8fe-40b9-9441-b1785ff46480" />
<img width="652" height="493" alt="less" src="https://github.com/user-attachments/assets/2b1961b3-363e-4ae1-b188-53f35f171a09" />


### Terminal Commands Instead Of Desktop GUI
I created files, moved files, deleted files and check file sizes using Linux terminal commands instead of using the desktop GUI
The commands I used are 
```bash
cp note.txt copy.txt
mv copy.txt testfolder
rm ~/testfolder/copy.txt
ls -lah
```
<img width="1265" height="713" alt="cp" src="https://github.com/user-attachments/assets/130f409e-f484-4ab7-863f-c2380b445ed8" />
<img width="1276" height="724" alt="mv" src="https://github.com/user-attachments/assets/eac04bc3-4c19-466c-bfca-7849ba2e060a" />
<img width="585" height="490" alt="ls -lah" src="https://github.com/user-attachments/assets/8bbab922-4813-4939-bcbb-a6ef52f8310a" />
<img width="1262" height="670" alt="rm" src="https://github.com/user-attachments/assets/8bf414bc-0a2e-413e-b412-2752e70aaa7a" />

### System Information Commands
I explored system information using the terminal commands
The commands I used are
```bash
uname -a
lsb_relaese -a
hostnamectl
/proc/cpuinfo
```
<img width="802" height="615" alt="uname -a, lsb_release -a, hostnamectl" src="https://github.com/user-attachments/assets/cbe5b349-de30-4f37-8281-332ed2923387" />
<img width="1207" height="681" alt="cpu info" src="https://github.com/user-attachments/assets/1f5dca61-4529-4def-a271-246a1380a8e9" />

### User Privilege Experiment
Here I will experiment with sudo
The commands I experimented with are
```bash
whoami
sudo whoami
adduser test
sudo adduser test
```
<img width="575" height="108" alt="whoami sudo and no sudo" src="https://github.com/user-attachments/assets/f485ab9c-008a-4a57-be63-06a16ba79e4d" />
<img width="459" height="271" alt="add user with and without sudo" src="https://github.com/user-attachments/assets/04450179-333b-4d36-9289-2dc0f178e2e6" />


### Networking Tests
Here I will try to ip an output and ping to ip 8.8.8.8
The commands I used are
```bash
ip a
ping 8.8.8.8
```
<img width="801" height="275" alt="ip " src="https://github.com/user-attachments/assets/06957ad3-f6ae-4817-8d84-24fda7cb2a0a" />
<img width="695" height="315" alt="ping 8888" src="https://github.com/user-attachments/assets/dfd02867-54aa-472f-80be-98edce390629" />
<img width="973" height="635" alt="network setting window" src="https://github.com/user-attachments/assets/9a775a03-1a97-4d14-8813-4199a64bcda8" />

### Edit host file name and ping GoogleEpicDNS
Here I will edit the hosts file and create a custom name, and also try and ping GoogleEpic DNS
The commands I used are 
```bash
sudo nano /etc/hosts editing
ping GoogleEpicDNS
```
<img width="789" height="616" alt="sudo nano GoogleEpicDNS" src="https://github.com/user-attachments/assets/a00537b8-6fdc-4d1d-aac4-c3443cbdd97f" />
<img width="602" height="244" alt="ping GoogleEpicDNS" src="https://github.com/user-attachments/assets/5ef2da15-dc07-4ba3-8ad7-3072732aeeb4" />

### DNS Lookup
Here I will perform a DNS lookup for google.com I will use nslookup and whois.
When I tried using whois, the system prompted me that I do not have it installed. Thus, I used sudo apt install whois.
The commands I used are
```bash
nslookup google.com
sudo apt install whois
whois google.com
```
<img width="651" height="495" alt="nslookup google" src="https://github.com/user-attachments/assets/2dd64b95-493d-4f6a-9886-329171a92373" />
<img width="793" height="499" alt="installing whois" src="https://github.com/user-attachments/assets/a4c7e000-04b1-4543-b68a-46bc86142140" />
<img width="783" height="620" alt="whois google" src="https://github.com/user-attachments/assets/7451103b-9ecc-4a13-bb44-c99b7acb0745" />

### Public vs Private IP Reflection
Here I find my ip using https://whatismyipaddress.com and I noticed that it is different.
The IP address shown by ip a is the private IP address assigned to Ubuntu inside the network. While the IP address shown by whatismyipaddress.com is the public IP address which is seen by the websites and is provided by the router.
The commands I used are 
```bash
ip a
```
<img width="801" height="275" alt="ip " src="https://github.com/user-attachments/assets/451abf57-0ba4-4d88-953d-05cfe00b664b" />
<img width="1262" height="678" alt="ipaddress" src="https://github.com/user-attachments/assets/87ceb01b-7ba6-4423-b5ae-cd95f4caf2f0" />

### Hardware Info Commands
Here I will show the difference between the terminal hardware info and the GUI hardware info
The commands I used are
```bash
lsusb
lspci
less /proc/cpuinfo
```
<img width="800" height="618" alt="lsusb lspci" src="https://github.com/user-attachments/assets/2578ea31-15dc-48fd-acf2-f7ca4b30d80e" />
<img width="1207" height="681" alt="cpu info" src="https://github.com/user-attachments/assets/316b4a77-d7af-493b-8f12-32ae392a8c91" />
<img width="728" height="613" alt="aboutthisdevice ubuntu" src="https://github.com/user-attachments/assets/52d369fa-8565-44a4-b74b-b88b00dfe0ae" />

### Output Redirection
Here I will save a command line output into a file, view it and delete it all using just the terminal
The commands I used are
```bash
command lsusb > output_of_lsusb
ls -lah
less output_of_lsusb
rm output_of_lsusb
```
<img width="619" height="492" alt="outputlsusb" src="https://github.com/user-attachments/assets/bd3e48fb-f68c-4a36-a776-8c5f3b925fb3" />
<img width="807" height="608" alt="less outputoflsusb" src="https://github.com/user-attachments/assets/09543f7e-da9c-408a-9cdd-ea026373d32b" />
<img width="567" height="481" alt="rm outputoflsusb" src="https://github.com/user-attachments/assets/bcb7b51a-fef2-4aa5-9986-f99538e7cf6e" />

### Software Installed
Here I will demonstrate the 3 ways of using softwares in Ubuntu. Through the browser, through binary download, and through a repository install
The commands I used are
```bash
ls -lah
```
<img width="1278" height="852" alt="Saas" src="https://github.com/user-attachments/assets/971a7616-70f3-4856-b846-ad09b62cda9b" />
<img width="486" height="67" alt="chrome download" src="https://github.com/user-attachments/assets/2ad16035-ba9c-4db2-8d68-8dde8593381c" />
<img width="1274" height="853" alt="Software Installed" src="https://github.com/user-attachments/assets/f02cc67f-acbc-4b06-a80c-46662ddb26da" />

### Command Line Install via Apt
Here I will use APT to update package lists. When I tried to run less /etc/apt/sources.list, the system prompted me that since my Ubuntu is a newer version, it has been moved to /etc/apt/sources.list.d/ubuntu.sources
The commands I used are
```bash
sudo apt update
sudo apt upgrade
sudo apt install vlc
vlc --version
less /etc/apt/sources.list.d/ubuntu.sources
```
<img width="802" height="561" alt="sudo update and upgrade" src="https://github.com/user-attachments/assets/09ca38f3-a608-4dcb-abb5-84ed4a796a6c" />
<img width="796" height="611" alt="vlc download" src="https://github.com/user-attachments/assets/b6ddab62-af83-469c-974d-df1bdc0bd550" />
<img width="799" height="623" alt="sources list" src="https://github.com/user-attachments/assets/6ec7b25e-a079-4bad-8817-d9e93a241f76" />

### Source Code Compilation
Here I will file hello_world.c with source code, compile it using gcc, and execute it. 
When I tried to compile it using gcc, the system prompted me that I do not have gcc installed. Thus, i used sudo apt install gcc
The commands I used are
```bash
nano hello_world.c
sudo apt install gcc
gcc hello_world.c -o hello_world_executable
ls -lah
./hello_world_executable
```
<img width="798" height="604" alt="code hello world" src="https://github.com/user-attachments/assets/f358223c-978d-4295-bf31-5d6eb25344dc" />
<img width="793" height="243" alt="install gcc" src="https://github.com/user-attachments/assets/b773c118-fbac-42ac-87d4-f7e6fa583c2e" />
<img width="802" height="616" alt="hello world executable" src="https://github.com/user-attachments/assets/fb8f7453-a665-4c66-bec5-743cd5186cc4" />
<img width="803" height="609" alt="run helloworld" src="https://github.com/user-attachments/assets/49acd9b0-d10f-4235-bc2b-85d860fc3e95" />

### Reflection Summary
During this lab, I was able to experience both GUI and CLI. GUI was more familiar and what I was most used to. Especially since I knew where to find everything such as settings and navigating the folders. However, CLI felt more efficiently as short codes such as rm, cp, nano, allowed me to move, change, or copy a file without having to navigate there physically. I also learnt different software installations methods. Saas is convenient as it can run in the browser without having to install anything. However, it requires internet access. Binary downloads are better as it can be used offline, but it is more complex. Lastly, repository installation. It is guaranteed safe as each app is verified before it is put onto the Software Centre. However, the updates may be released slower than the other methods. 
Personally, I would prefer GUI and binary downloads as thats what I am most used to coming from windows. However, as a future software developer, I would prefer CLI as it is faster, and you are able to do almost everything in 1 window. 

### 1a-2 Reflection Questions
Which file editors are best for remote access and why?
Nano file editor is best for remote access as it is a terminal editor. While gedit is a GUI editor which you cannot use in remote access. 

Compare Software Installation Methods: Saas vs binaries vs repos vs source
Saas are softwares accessed through online through a browser. For example Google Docs
Binaries are ready made installers direct from the source. They are simple to install but might not update automatically.
Repos are package managers downloaded from the app store. They are safer as they have been certified before being uploaded.
Source is compiling software from its source code. This gives developers more control on what they download but is not beginner friendly. 

what are the pros/cons of each method from user and developer perspectives
User
Saas: Easiest as there is no download needed. However, it might have limited functions.
Binaries: Average for full functionality. However, less secure as not all downloads are safe.
Repos:  Easiest for full functionality. However, updates might not come as fast as straight from the source.
Source: Hardest as this requires programming knowledge. 

Developer
Saas: Allows for fast updates for users.
Binaries: Best for full functionality.
Repos: Might be harder to get verified which might delay version updates.
Source: Full flexibility but users might have problems installing.


How did using CLI improve your understanding of Linux
Using CLI allows me to better understand Linux better as I was exposed to terminal commands instead of a full GUI interface. 

## 1b-1 Linux Services, SSH, Firewalls & Compression
### Apache Web Server Installed
Here I will Install Apache and show that it is running in firefox
The commands I used are
```bash
sudo apt install apache2
```
<img width="800" height="612" alt="1b1 1 2" src="https://github.com/user-attachments/assets/d5d5c300-849e-4037-a554-35459bb5aece" />
<img width="1274" height="799" alt="1b1 1 1" src="https://github.com/user-attachments/assets/a7892ca0-4a6f-4045-a26f-5519eddef123" />


### Modified index.html page
Here I will modify Apache's default page to make it my own. I first tried nano /var/www/html/index.html since nano is to edit, but I could not save the file as i did not have permission. Hence, I had to use sudo nano to edit the file instead.
The commands I used are
```bash
sudo nano /var/www/html/index.html
```
<img width="791" height="588" alt="accessing apache code" src="https://github.com/user-attachments/assets/8d24d189-ec97-41d0-9907-9db8aa961dcc" />
<img width="795" height="616" alt="editted apache code" src="https://github.com/user-attachments/assets/fc95546a-9dd4-4e46-b0e3-d53fff0e0404" />
<img width="1273" height="744" alt="Apache edited" src="https://github.com/user-attachments/assets/8c24eff7-998e-4608-bca4-48cb04cdf1a4" />

### IP Address Identified and Shared
Here I will show my local IP and loopback IP and that I can access my partner's IP. For this excercise, I used my host OS to demonstrate.
```bash

```
This shows my both my vm's loopback IP labelled lo and my local IP. 
<img width="805" height="615" alt="vm IP" src="https://github.com/user-attachments/assets/754f1bf9-1a75-4884-9c87-5deae22faa32" />
<img width="1905" height="1014" alt="Accessing vm IP in host os" src="https://github.com/user-attachments/assets/da460b3b-aed6-4238-ac36-3bf283b0d4c1" />

### Nmap Port Scan Result
Here I will demonstrate that my port in vm while apache is installed is open but when i removed, it closes. First, I have to install nmap on my windows pc through the nmap downloader. 
<img width="1744" height="739" alt="nmap scan ubuntu from windows" src="https://github.com/user-attachments/assets/0f47c846-7dda-4815-bd60-e404a76bf786" />
<img width="793" height="591" alt="removing apache from ubuntu" src="https://github.com/user-attachments/assets/18ca9aad-e865-4c2d-87f3-df15624f9971" />
<img width="855" height="728" alt="port closed " src="https://github.com/user-attachments/assets/dcc1f01a-31e0-4976-b164-f15190919464" />

### Firewall (UFW) Status and Rules
Here I will show you the status before and after enabling firewall, and show youthat port 80 is allowed and verified. I also had to reinstall apache as the previous excercise asked us to remove apache.
The commands I used are
```bash
sudo ufw status verbose
sudo ufw allow "Apache"
sudo apt install apache2
```
<img width="794" height="608" alt="firewall off" src="https://github.com/user-attachments/assets/5be188ec-4c73-4a22-9bcf-fdc0344ddc2c" />
<img width="794" height="368" alt="allow apache and firewall active" src="https://github.com/user-attachments/assets/42affe7f-df13-4310-aaa7-0541c2c8e982" />
<img width="853" height="302" alt="port open" src="https://github.com/user-attachments/assets/4d2817a1-6641-4c9a-a3b0-3b45e18f5719" />

### SSH Enabled and Tested
Here I will attempt to login via ssh to my partner's machine using both default and explicitly declared usernames
The commands I used are
```bash
sudo apt install openssh-server
sudo ufw allow 22/tcp
ssh 192.168.138.128
ssh jaden@192.168.138.128
```
<img width="806" height="611" alt="ssh open " src="https://github.com/user-attachments/assets/c149165e-defd-4a75-b284-25251d8672ca" />
<img width="796" height="611" alt="allow 20tcp" src="https://github.com/user-attachments/assets/4d2b5682-ad3d-4fb4-96d3-c376f1a99a1b" />
<img width="837" height="440" alt="default login ssh" src="https://github.com/user-attachments/assets/2553cd19-5e44-4d80-b625-82ff79c44468" />
<img width="851" height="367" alt="explicitly named ssh login" src="https://github.com/user-attachments/assets/d473b739-9c52-48f0-af10-d3822d867477" />

### New User Created and Verified
Here I will add a user and verify it with /etc/passwd
The commands I used are
```bash
sudo adduser testuser
cat /etc/passwd
```
<img width="796" height="566" alt="add user" src="https://github.com/user-attachments/assets/4e6d0ffd-6b55-443e-96e2-f0437c32714e" />
<img width="784" height="691" alt="cat show ttestuser" src="https://github.com/user-attachments/assets/c7527599-d111-478d-9db7-8f04ee4142dd" />

### Compression and Decompression Tested
Here I will compress and decompress files using terminal codes and show the output using ls -la. when using bzip the system prompted me to install, so I used sudo apt install bzip2.
The commands I used are
```bash
tar cf testfolder.tar testfolder
ls -la
sudo apt install bzip2
bzip2 testfolder.tar.bz2
bunzip2 testfolder.tar.bz2
mkldir testfolder1
tar -xvf testfolder.tar -C testfolder1
ls -la testfolder1
```
<img width="796" height="697" alt="tar" src="https://github.com/user-attachments/assets/30346771-6ab2-46c8-8bf9-b5ffd0ba04e7" />
<img width="792" height="701" alt="install bzip2" src="https://github.com/user-attachments/assets/292949f2-68bf-475a-aa02-f0f12249f622" />
<img width="796" height="531" alt="archieve testfolder" src="https://github.com/user-attachments/assets/43f70807-7f1d-47e6-b0c6-6908459f4700" />
<img width="710" height="534" alt="decompress testfolder" src="https://github.com/user-attachments/assets/58d591d8-bf50-4a64-8e4e-3b04279cfebd" />
<img width="798" height="701" alt="extract files" src="https://github.com/user-attachments/assets/11d0f036-3e85-43ea-ad11-c8b6368d9b58" />
<img width="760" height="116" alt="testfolder1 documents" src="https://github.com/user-attachments/assets/e40c1dbe-7165-46ec-bd5a-74af1d42b543" />

### SCP File Transfers Between Machines
Here I will copy a file from host machine to vmmachien through ssh
The commands I used are
```bash
echo "test test" > test.txt
scp test.txt jaden@192.168.138.128:/home/jaden
ls -la
```
<img width="816" height="137" alt="scp to ubuntu" src="https://github.com/user-attachments/assets/b192624c-16cd-4c05-ab6b-669025dfb0ef" />
<img width="624" height="544" alt="successfully transfered test" src="https://github.com/user-attachments/assets/16ad0dd4-69cd-41c1-85ac-fca4fc03f9b2" />

### /etc/hosts File Modified
Here I will add a custom hostname "GoogleEpicDNS" and ping it
The commands I used are 
```bash
sudo nano /etc/hosts editing
ping GoogleEpicDNS
```
<img width="789" height="616" alt="sudo nano GoogleEpicDNS" src="https://github.com/user-attachments/assets/a00537b8-6fdc-4d1d-aac4-c3443cbdd97f" />
<img width="602" height="244" alt="ping GoogleEpicDNS" src="https://github.com/user-attachments/assets/5ef2da15-dc07-4ba3-8ad7-3072732aeeb4" />

### nslookup and whois Commands Run
Here I will perform a DNS lookup for google.com I will use nslookup and whois.
When I tried using whois, the system prompted me that I do not have it installed. Thus, I used sudo apt install whois.
The commands I used are
```bash
nslookup google.com
sudo apt install whois
whois google.com
```
<img width="651" height="495" alt="nslookup google" src="https://github.com/user-attachments/assets/2dd64b95-493d-4f6a-9886-329171a92373" />
<img width="793" height="499" alt="installing whois" src="https://github.com/user-attachments/assets/a4c7e000-04b1-4543-b68a-46bc86142140" />
<img width="783" height="620" alt="whois google" src="https://github.com/user-attachments/assets/7451103b-9ecc-4a13-bb44-c99b7acb0745" />

### Public vs Private IP Comparison
Here I find my ip using https://whatismyipaddress.com and I noticed that it is different.
The IP address shown by ip a is the private IP address assigned to Ubuntu inside the network. While the IP address shown by whatismyipaddress.com is the public IP address which is seen by the websites and is provided by the router.
The commands I used are 
```bash
ip a
```
<img width="801" height="275" alt="ip " src="https://github.com/user-attachments/assets/451abf57-0ba4-4d88-953d-05cfe00b664b" />
<img width="1262" height="678" alt="ipaddress" src="https://github.com/user-attachments/assets/87ceb01b-7ba6-4423-b5ae-cd95f4caf2f0" />

### Hardware Info Commands
Here I will show the difference between the terminal hardware info and the GUI hardware info
The commands I used are
```bash
lsusb
lspci
less /proc/cpuinfo
```
<img width="800" height="618" alt="lsusb lspci" src="https://github.com/user-attachments/assets/2578ea31-15dc-48fd-acf2-f7ca4b30d80e" />
<img width="1207" height="681" alt="cpu info" src="https://github.com/user-attachments/assets/316b4a77-d7af-493b-8f12-32ae392a8c91" />
<img width="728" height="613" alt="aboutthisdevice ubuntu" src="https://github.com/user-attachments/assets/52d369fa-8565-44a4-b74b-b88b00dfe0ae" />

### Output Redirection
Here I will save a command line output into a file, view it and delete it all using just the terminal
The commands I used are
```bash
command lsusb > output_of_lsusb
ls -lah
less output_of_lsusb
rm output_of_lsusb
```
<img width="619" height="492" alt="outputlsusb" src="https://github.com/user-attachments/assets/bd3e48fb-f68c-4a36-a776-8c5f3b925fb3" />
<img width="807" height="608" alt="less outputoflsusb" src="https://github.com/user-attachments/assets/09543f7e-da9c-408a-9cdd-ea026373d32b" />
<img width="567" height="481" alt="rm outputoflsusb" src="https://github.com/user-attachments/assets/bcb7b51a-fef2-4aa5-9986-f99538e7cf6e" />

### Extension Challenge 1 Completed
Here I will SSH into my vm and create a file on its desktop from my host machine
The commands I used are
```bash
cd ~/Desktop
touch Hi_Jaden
ls -la Desktop
```
<img width="480" height="270" alt="create file in ubuntu from host" src="https://github.com/user-attachments/assets/99182fb5-e80b-49cf-8e00-90f02bb2ede5" />
<img width="501" height="114" alt="File created" src="https://github.com/user-attachments/assets/eb8d4383-dc61-45dd-a7e0-1febcc9a84c1" />

### Extension Challenge 2 Completed
Here I will attempt to launch gedit over SSH. I am unable to launch gedit over SSH as is a GUI text editor and SSH only allows for command line access. 
The commands I used are
```bash
ssh jaden@192.168.138.128
gedit
```
<img width="1027" height="89" alt="cant launch gedit" src="https://github.com/user-attachments/assets/636576a7-eab5-46fb-876a-c000e700e68a" />

### Extension Challenge 3 Completed
Here i will create new files and attempt to transfer them from my host machine to my vm
The commands I used are
```bash
echo "test test" > test1
ehco "test test" > test2
scp test.txt test1.txt test2.txt jaden@192.168.138.128
ls -la
```
<img width="426" height="36" alt="create test files for transfer" src="https://github.com/user-attachments/assets/88d28a55-7f2c-4f8b-bbe3-418ad0c59980" />
<img width="847" height="162" alt="file transferred" src="https://github.com/user-attachments/assets/7a196550-b77b-4254-affc-92606bce7ea5" />
<img width="647" height="588" alt="proof of successful transfer" src="https://github.com/user-attachments/assets/9802980e-9d05-4c35-8bb3-4695ee2d933a" />

### Extension Challenge 4 Completed
Here I will download the top 10 books from Gutenberg, compress them using tar and bzip2, then transfer them to my host machine from vm via scp
The commands I used are
```bash
mkdir gutenberg_top10
cd gutenberg_top10
wget https://www.gutenberg.org/files/2701/2701-0.txt -O 01_moby_dick.txt
wget https://www.gutenberg.org/files/1342/1342-0.txt -O 02_pride_and_prejudice.txt
wget https://www.gutenberg.org/files/27509/27509-0.txt -O 03_2006_cia_world_factbook.txt
wget https://www.gutenberg.org/files/1513/1513-0.txt -O 04_romeo_and_juliet.txt
wget https://www.gutenberg.org/files/42486/42486-0.txt -O 05_two_magics.txt
wget https://www.gutenberg.org/files/2641/2641-0.txt -O 06_room_with_a_view.txt
wget https://www.gutenberg.org/files/27558/27558-0.txt -O 07_2003_cia_world_factbook.txt
wget https://www.gutenberg.org/files/2554/2554-0.txt -O 08_crime_and_punishment.txt
wget https://www.gutenberg.org/files/65662/65662-0.txt -O 09_der_zauberberg_zweiter_band.txt
wget https://www.gutenberg.org/files/67979/67979-0.txt -O 10_blue_castle.txt
ls -la
tar cf gutenbergtop10.tar gutenbergtop10
bzip2 gutenbergtop10.tar
scp jaden@192.168.138.128:/home/jaden/gutenbergtop10.tar.bz2 Desktop
```
<img width="808" height="269" alt="create gutenberg folder" src="https://github.com/user-attachments/assets/f46f321c-da13-4d24-b9c8-a509a3ceff2f" />
<img width="766" height="334" alt="download top 10" src="https://github.com/user-attachments/assets/44f2cbb9-4368-421e-8eee-1e230a16bcb8" />
<img width="802" height="173" alt="archieve gutenber" src="https://github.com/user-attachments/assets/7e2dfc22-d91d-4dc7-8603-41c053fcc044" />
<img width="597" height="442" alt="compressed guntengerg" src="https://github.com/user-attachments/assets/18314f09-b9f7-4f20-be9c-5dd3e4384595" />
<img width="838" height="112" alt="transferred gutenberg to host" src="https://github.com/user-attachments/assets/e0e0cd77-1982-4c5c-9b16-aa90027939bc" />

### Two VMs Networked
Here I will attempt to ping my host machine and my ubuntu to each other
The commands I used are 
```bash
ping 192.168.138.128
ipconfig
ping 192.168.138.1
```
<img width="460" height="221" alt="ping ubuntu" src="https://github.com/user-attachments/assets/afc9cb37-cc4a-40ce-8727-b1d46a332802" />
<img width="567" height="58" alt="ping host" src="https://github.com/user-attachments/assets/cb6bb8af-a48a-4d7d-a0d2-d0c462987732" />

### Reflection Paragraph
During this lab, I have worked with Linux networking. It has helped me understand better on how machinese communicate to each other. Commads like ip a, ip config showed me the difference in the VM's ip address and the host machine's ip address. Using SSH taught me how remote access works. When i logged into Ubuntu from my host machine, I could run commands, create files and manage the system without using a GUI. File compressions and transfers allowed me to better understand more of command line control. Such as tar to archieve files, bzip2 to compress files and scp to transfer files between systems.

### 1b-1 Reflection Questions
Whats the role of a firewall in managing services?
The role of a firewall in managing services is to control the traffic going to the server. 

How did SSH access deepen your understanding of Linux as a server?
SSH access helped me to understand how to install softwares, edit files, restart services, transfer files, and troubleshoot problems using only the command line. 

Why is file compression important in server contexts?
File compression is important in server contexts as by compressing the file, it reduces the size, which in turn ensures that transfers are moreefficient.

How does user privilege management help secure system?
User privilege management helps secure the system as you are able to control what users are able to access and edit what files.

## 1b-2 Linux File Permissions & Gropu Access Control
### Three Users Created
Here i will create three new users using adduser
The commands I used are
```bash
sudo adduser alice
sudo adduser bob
sudo adduser mallory
cat /etc/passwd
```
<img width="1101" height="717" alt="add 3 new users" src="https://github.com/user-attachments/assets/894f01a6-4ba3-4235-811c-2ade11325f7a" />
<img width="508" height="79" alt="proof add 3 new user" src="https://github.com/user-attachments/assets/7a7ce16d-2dec-4ee5-b344-06d9933c9bda" />

### Group Created and Configured
Here I will create a groupp with alice and bob via adduser [user][group]
The commands I used are
```bash
sudo groupadd sharedgroup
sudo adduser alice sharedgroup
sudo adduser bob sharedgroup
less /etc/group
```
<img width="635" height="59" alt="create and add user to shared group" src="https://github.com/user-attachments/assets/01b0dd73-9b90-4d5f-80e2-cb3a72e929fb" />
<img width="363" height="43" alt="proof added user to shared group" src="https://github.com/user-attachments/assets/693d5a19-a352-4879-92c2-d787f14cbab1" />

### 'Shared' Directory Created in /home/
Here I will output mkdir /home/shared and update ownership and group via chown, chgrp
The commands I used are
```bash
sudo mkdir /home/shared
sudo chown alice /home/shared
sudo chgrp sharedgroup /home/shared
ls -ld /home/shared
```
<img width="614" height="125" alt="chown chgrp" src="https://github.com/user-attachments/assets/5018b526-eb0f-4cee-98f8-5df8abadacd6" />

### Ten Files Created in 'shared' Folder
Here I will create 10 files inside the "shared" folder
The commands I used are
```bash
sud touch /home/shared file1.txt
sud touch /home/shared file2.txt
sud touch /home/shared file3.txt
sud touch /home/shared file4.txt
sud touch /home/shared file5.txt
sud touch /home/shared file6.txt
sud touch /home/shared file7.txt
sud touch /home/shared file8.txt
sud touch /home/shared file9.txt
sud touch /home/shared file10.txt
ls -l /home/shared
```
<img width="759" height="428" alt="1b2 4 Create 10 files using touch" src="https://github.com/user-attachments/assets/f41f8d42-5cbd-4d1f-973b-4a966b6214be" />

### Permissions Assigned Properly
Here I will give permission to alice and bob in the shared group
The commands I used are
```bash
sudo chown alice:sharedgroup /home/shared/file*txt
sudo chmod 750 /home/shared/file*txt
ls -l /home/shared
```
<img width="781" height="368" alt="1b2 5 Permissions Assigned Properly" src="https://github.com/user-attachments/assets/7a2f8b97-85b1-4dfc-bef4-ec242a403e47" />

### Access Verified as Each User
Here I will check the permissions of the users
The commands I used are
```bash
su - alice
su - bob
su - mallory
whoami
ls -l /home/shared
echo "test" >> /home/shared/file1.txt
echo "test" >> /home/shared/file2.txt
cat /home/shared/file1.txt
```
<img width="800" height="478" alt="1b2 6 alice permissions" src="https://github.com/user-attachments/assets/f0d69a1d-056a-49aa-b0ee-ba2ee3b62aa1" />
<img width="800" height="581" alt="1b2 6 bob permissions" src="https://github.com/user-attachments/assets/3338e083-c055-4711-9181-f338d1101275" />
<img width="803" height="378" alt="1b2 6 Mallory permissions" src="https://github.com/user-attachments/assets/103c5805-3b43-4d56-a545-289357a34b0c" />

### Use of chmod/chown/chgrp -R
Here I will show the usage of recursive flags
The commands I used are
```bash
sudo chown -R alice /home/shared
sudo chgrp -R sharedgroup /home/shared
sudo chmod -R 750 /home/shaared
sudo ls -ld /home/shared
sudo ls -l /home/shared
```
<img width="771" height="98" alt="1b2 7 1" src="https://github.com/user-attachments/assets/bd739ff5-ff1a-40bc-84f7-d6d6a3546411" />
<img width="791" height="346" alt="1b2 7 2" src="https://github.com/user-attachments/assets/3b607846-b271-44be-890a-e9308792a9d9" />

### Add Mallory to Sudo
Here I will add mallory to sudo group
The commands I used are
```bash
sudo addusers mallory sudo
groups mallory
```
<img width="630" height="93" alt="1b2 8 1" src="https://github.com/user-attachments/assets/8cb9001c-d90a-4dbb-9f95-500a1a6b59a9" />

### Mallory Sudo Access
Here I will use Mallory's new sudo permission to access protected files
The commands I used are
```bash
su - mallory
ls -l /home/shared
sudo ls -l /home/shared
```
<img width="795" height="397" alt="1b2 9 1" src="https://github.com/user-attachments/assets/a0f6fee3-862e-495c-ab5b-579e282fa133" />

### Clean Up Folder
Here I will delete the shared directory and its contents
The commands I used are
```bash
sudo rm -r /home/shared
sudo ls -ld /home/shared
```
<img width="801" height="226" alt="1b2 10 1" src="https://github.com/user-attachments/assets/4b831ffe-50d8-4b36-9031-1ac5d9fda268" />

### 1b-2 Reflection Questions
How do Linux permissions differ from Windows ACL? 
Linux permissions are simpler, which windows ACL are more complex.
Linux only has read, write, execute. While Windows ACL has read, write, modify, full control, inheritance, and deny rules.

Whats the effect of chmod 770 vs 750?
chmod 770 gives the owner and group permission to read, write and execute. 
chmod 750 gives the owner full access, while the group can only read and execute, but unable to write. 

What is the risk of adding users to the sudo group?
By adding users to the sudo group, it gives them admin privileges. If given to the wrong user, this could lead to the user misusing the privilege to damage the system.

Why is it important to verify with 'su' and 'whoami'?
By verifying su with whoami, it confirms which user you are currently controlling. 

## 1b-3 File Search, Analysis & Archiving in Linux
### Archieve Extraction
Here I will extract the archieved guntenberg.tar.bz2. I had to transfer the file from my host machine to VM
The commands I used are
```bash
scp 1b-3-Gutenberg.tar.bz2 jaden@192.168.138.128L /home/jaden/
ls -l 1b-3-Gutenberg.tar.bz2
bunzip2 1b-3-Gutenberg.tar.bz2
tar -xvf 1b-3-Gutenberg.tar
ls -l
```
<img width="856" height="208" alt="1b3 1 1" src="https://github.com/user-attachments/assets/ca37b0b5-195b-4d59-bea1-86ea14ef7dae" />
<img width="796" height="716" alt="1b3 1 2" src="https://github.com/user-attachments/assets/cbed9636-4f25-48d4-8c46-9f97e16ed27e" />

### File Listing of Extracted Directory
Here I will show you the output of ls -l where Gutenberg was extracted to. 
The commands I used are
```bash
ls -l
```
<img width="794" height="653" alt="1b3 2 1" src="https://github.com/user-attachments/assets/ee1e2a16-05ea-4e43-ad73-7d412abd8754" />

### Filename Search
Here I will demonstrate filename search
The commands I used are
```bash
find ./Gutenberg -name "*.txt"
```
<img width="802" height="189" alt="1b3 3 1" src="https://github.com/user-attachments/assets/201471d9-edb0-457a-9fb9-e08d1e545eb2" />


### Text Seach via Grep
Here I will demonstrate a text search using grep
The commands I used are 
```bash
ls -l
grep -r "verdigris"
```
<img width="807" height="603" alt="1b3 4 1" src="https://github.com/user-attachments/assets/3ee3c11c-119a-4126-8782-9013ff2f7f50" />

### Contextual Text Search
Here I will demonstrate a contextual text search using grep. There was no phrase matching "Next day there was a surprise for Jack". Thus, there was no output given
The commands I used are
```bash
grep -r -C 3 "Next day there was a surprise for Jack"
```
<img width="803" height="664" alt="1b3 5 1" src="https://github.com/user-attachments/assets/c1cae6ab-4d78-4d06-b288-ecd81fd54eee" />

### Data Based File Search
Here I will demonstrate data based file search using find. find . -type f -printf '%T+ %p\n' lists the files, sort sorts the results with oldest being first and sed -n '3p' prints only the 3rd line 
The command I used are
```bash
find . -type f -printf '%T+ %p\n' | sort | sed -n '3p'
```
<img width="789" height="166" alt="1b3 6 1" src="https://github.com/user-attachments/assets/4f78a232-b8e5-4c2e-8cfe-bd91b06f12a5" />

### Size Based File Search
Here I will demonstrate a file search based on size. soze 255258c has no files, thus, there is no output
The commands I used are
```bash
find . -type f -size 255258c -exec ls -lh {} \;
find . -type f -size +512k -exec ls -lh {} \;
```
<img width="1216" height="747" alt="1b3 7 1" src="https://github.com/user-attachments/assets/4647198d-ccac-48d6-9cd0-a122e090a85a" />

### Find Largest File
Here I will demonstrate the Largest File found
The command line I used are 
```bash
du -a ./Gutenberg | sort -nr | head
```
<img width="792" height="270" alt="1b3 8 1" src="https://github.com/user-attachments/assets/7c491aa0-1d23-4ad6-8979-577dcfc45497" />


### Text Frequency Analysis Performed
Here I will demonstrate text frequency analysis
The command i used are
```bash
sed -e 's/\s/\n/g' < test.txt | sort | uniq -c | sort -nr | head -200
```
<img width="789" height="193" alt="1b3 9 1" src="https://github.com/user-attachments/assets/218438f0-12a5-4d50-9fbd-045e861e77ec" />

### Answers to Questions Provided
How many times does the string “verdigris” appear? (enter a number only) 
1
What is the surname of the author of the filename “1107.txt”? (case sensitive) 
NIL
What is the surname of the author of the file that is exactly 255258 bytes? (case sensitive) 
NIL
What is the filename of the file with the 3rd oldest creation date? 
frankenstein.txt
Find the word that follows the text: “Next day there was a surprise for Jack” (Case-sensitive, no spaces) 
NIL

### 1b-3 Reflection Questions
Which command-line tool was the most useful in solving the questions? 
The most useful was grep. This allowed me to search text inside files. 

How might these search tools help in cybersecurity investigations? 
These search tools help in cybersecurity investigations as investigators can quickly search through large number of files for key strings that are useful in their investigation.

How could scripting improve repetitive search tasks? 
By scripting, you can combine multiple commands into one automated process. This inturn, saves time and reduces human error.

What limitations did you encounter using grep and find? 
grep only finds exact matches unless -i is used. find would not work if the command is ran in the wrong directory. 
 
