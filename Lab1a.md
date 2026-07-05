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

What did you learn about virtualisation tools and their differences?

How confident do you feel using Ubuntu after completing this lab?

In what ways can a virtualised Linux environment help in industry scenarios?

What would you do differently if setting up another VM?


#Lab 1b Ubuntu GUI & CLI Familiarisation + Software Installation Methods

## Ubuntu Linux Familiarisation
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
whoami
sudo whoami
adduser test
sudo adduser test
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
sudo nano /etc/hosts editing
ping GoogleEpicDNS
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

### 1b Reflection Questions
Which file editors are best for remote access and why?

Compare Software Installation Methods: Saas vs binaries vs repos vs source

what are the pros/cons of each method from user and developer perspectives

How did using CLI improve your understanding of Linux


