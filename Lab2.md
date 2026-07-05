# Lab 2 ISEA
## 2a-1 Total Cost of Ownership Analysis
### Assumptions
Comparison Period: 5 Years
Pages per week: 750
Power usage per week: 40 hours
Cost of electricity per kWh(Local provider): 
Cost of paper (ream of 500): $6
Ink yield per cartridge: 
### Printer Models Chosen
|Brand|Model|Type|Intended use|
|---|---|---|---|

### 2a-1 Reflection Questions
Based on the TCO, which printer is the most cost-effective over 5 years? 

Would the answer change for a home user who prints only 5 pages per week? 

What other non-financial factors could influence printer selection? 

What cost components are more significant for a large workgroup printer? 

At what point (in years/pages) do the two printer options break even in cost? 

## 2b-1 Cloud Web Server Deployment
### EC2 Instance Launched
Here I will launch the EC2 Instance
<img width="1675" height="724" alt="2b1 1 1" src="https://github.com/user-attachments/assets/10ebb888-254a-442f-9783-2e8efb1849de" />

### Security Group Configured
Here I will show the inbound rules that I have set
<img width="1635" height="753" alt="2b1 2 1" src="https://github.com/user-attachments/assets/ec211c2e-3156-4ccb-a6a2-93e665f9834b" />

### SSH Access Successful
Here I will demonstrate the terminal output showing successful SSH login using the .pem
<img width="863" height="419" alt="2b1 3 1" src="https://github.com/user-attachments/assets/dc184297-5e18-41ce-b6ac-7e0104758438" />

### Apache Installed and Tested
Here I will demonstrate that Apache has been successfully installed and running
The commands that I used are 
```bash
sudo apt install apache2
```
<img width="511" height="129" alt="2b1 4 1" src="https://github.com/user-attachments/assets/538d339c-5a82-4dd8-8a9d-e1ee29529796" />
<img width="1917" height="1025" alt="2b1 4 2" src="https://github.com/user-attachments/assets/27047ee9-6203-407c-80d0-c425948fc346" />

### Custom index.html
Here I will demonstrate editing of Apache's default page
The commands that I used are
```bash
sudo nano /var/www/html/index.html
cat /var/www/html/index.html
```
<img width="649" height="205" alt="2b1 5 1" src="https://github.com/user-attachments/assets/cb09f4ca-ef4a-4b68-9512-2688d68a1f31" />
<img width="925" height="533" alt="2b1 5 2" src="https://github.com/user-attachments/assets/9a994247-a694-451a-aa73-e9f0d65fb42c" />

### External File Downloaded with wget
Here I will demonstrate downloading of an external file using wget and saving it in /home/ubuntu
The commands that I used are
```bash
cd /home/ubuntu
pwd
wget http://www2.eecs.berkeley.edu/Pubs/TechRpts/2009/EECS-2009-28.pdf
ls -lh EECS-2009-28.pdf
```
<img width="856" height="539" alt="2b1 6 1" src="https://github.com/user-attachments/assets/9bb3485a-d07e-4980-9e2b-85078a358dd2" />

### Copying of file to web root
Here I will demonstrate copying of a file to /var/www/html
The commands that I used are
```bash
cd /home/ubuntu
sudo cp EECS-2009-28.pdf var/www/html
ls -l /var/www/html
```
<img width="644" height="197" alt="2b1 7 1" src="https://github.com/user-attachments/assets/a5007571-9af8-4414-85dd-192a264b454a" />

### PDF File Accesible via browser
Here I will demonstrate viewing the pdf from browser
<img width="929" height="915" alt="2b1 8 1" src="https://github.com/user-attachments/assets/bf73cab1-fcb3-4d7c-a4e2-e07376707823" />


### Link Inserted in HTML Page
Here I will demonstrate inserting a link in index.html
The commands I used are
```bash
sudo nano /var/www/html/index.html
cat /var/www/html/index.html
```
<img width="854" height="294" alt="2b1 9 1" src="https://github.com/user-attachments/assets/2448e800-3f0b-49e0-ac01-9f519f0476e8" />
<img width="929" height="346" alt="2b1 9 2" src="https://github.com/user-attachments/assets/363ba1b1-8d19-4f95-b5a3-83f064a9afcc" />

### Budget Monitoring
Here I will show my budget alert setup and the cost summary so far
<img width="1112" height="557" alt="2b1 10 1" src="https://github.com/user-attachments/assets/c3cc4e63-9e88-4465-823d-539930178716" />
<img width="1102" height="594" alt="2b1 10 2" src="https://github.com/user-attachments/assets/65128d62-167f-4fed-8b34-e6e10c8640e6" />

### Instance Termination
Here I demonstrated that I have stopped the EC2 instance once I am done using it
<img width="864" height="266" alt="2b1 11 1" src="https://github.com/user-attachments/assets/51c7f1db-ffa3-4378-8748-d7ad0a452293" />


### Ping International Servers
Here I ping to servers in US, Europe and Asia. 
The commands I used are
```bash
ping -c 4 google.com
ping -c 4 bbc.co.uk
ping -c 4 nus.edu.sg
```
|Ping comparison|
|---|
|US|Europe|Asia|
|3004ms|3004ms|3004ms|
<img width="838" height="565" alt="2b1 C1 1" src="https://github.com/user-attachments/assets/c9a516db-d808-44ab-bb37-1f38447e1e36" />

### Upload Local File via scp
Here I will demonstrate uploading a file on my local machine to EC2 VM
The commands I used are
```bash
 scp -i "aws-Ubuntu-key1.pem" C:\Users\User\Desktop test.txt ubuntu@54.87.22.131:/home/ubuntu
```
<img width="850" height="194" alt="2b1 C2 1" src="https://github.com/user-attachments/assets/35123d43-2b11-456e-ad4a-92cbacb0f228" />

### Reflection Questions
What were the benefits of cloud deployment over local virtualisation? 
Cloud deployment allows the web server to be accessed over the internet. While local virtualisation is limited to your own machine or local network.

How does Apache serve files, and how did you verify this? 
Apache serves files from its web directory. I verified this by opening the PDF through the browser.

What did you learn about file ownership and permissions? 
I learnt that file ownership and permissions defaults to the admin. However, chown, chgrp and chmod can change who owns the file and access it.

What risks are associated with leaving instances running? 
Leaving instances running increases security risks as SSH and HTTP are exposed to the internet. 

How would you explain the difference between DNS and /etc/hosts to a client? 
DNS is a public naming syustem that converts domain names into IP adresses. While /etc/hosts is local that manually maps names to IP addresses.


## 2b-2 Introduction to Bash Scripting & System Automation
### Directory and File Operations
Here I will demonstrate navigating the file system and managing files
The commands I used are
```bash
mkdir LabFiles
cd LabFiles
touch notes.txt
echo "This is a Bash scripting lab." > notes.txt
cat notes.txt
cp notes.txt backup_notes.txt
mv backup_notes.txt old_notes.txt
rm old_notes.txt
```
<img width="799" height="381" alt="2b 2a 1" src="https://github.com/user-attachments/assets/5092ccc4-a833-48c3-918f-0d3beb8f2011" />

### Reflection: File System Commands
What command did you use to create a directory?
I used mkdir to create a directory.

How can you view file content without a GUI editor?
I used cat to view file content without a GUI editor.

What is the difference between cp and mv?
cp copies the file contents to another file while mv renames the file.

### Basic Bash Script Created and Run
Here I will demonstrate creating a script file, executing the file, and modifying it. 
The commands I used are
```bash
cd LabFiles
nano hello_world.sg
chmod 777 hello_world.sh
./hello_world.sg
nano hello_world.sh
```
<img width="794" height="505" alt="2b2a 3 1" src="https://github.com/user-attachments/assets/511c93ca-6067-4b93-a00c-4d4465d51c9b" />
<img width="797" height="623" alt="2b2a 3 2" src="https://github.com/user-attachments/assets/1facb7fa-6887-4086-9d1d-83cdbf411e2a" />
<img width="799" height="604" alt="2b2a 3 3" src="https://github.com/user-attachments/assets/a257886d-be74-448c-8aed-6ac802d94116" />

### Reflection: Script Basics
What is chmod +x for? 
chmod +x gives the file execute permission.

Why is #!/bin/bash used? 
It tells Linux to use the Bash Shell.

How can you personalize script output?
You can personalize script output by modifying the echo line.

### Implementing Loop & Conditionals
Here I will demonstrate loops and conditionals
The commands I used are
```bash
cd LabFiles
nano system_info.sh
chmod 777 system_info.sh
./system_info.sh
```
<img width="798" height="519" alt="2b2a 5 1" src="https://github.com/user-attachments/assets/aabae7b0-7e0f-40fc-b333-3b0005b3e2f9" />
<img width="774" height="625" alt="2b2a 5 2" src="https://github.com/user-attachments/assets/2f387624-dd3f-4f0e-adaa-07590f8ac6c7" />

### Reflection Questions
How does the for loop work?
for i in {1..5}
do
    echo "Iteration: $i"
    sleep 1s
done
This runs 5 times, each time the number going up by 1, with a delay of 1 second.

What happens if number > 10?
If number > 10, it will print "number out of range"

How could invalid input be handled more gracefully?
Invalid input could be handled more gracefully with a while loop which loops until the user gives a valid input.

### Automating System Monitoring Tasks
Here I will demonstrate automation of the monitoring system resources such as CPU usage, memory usage, and disk space.
The commands I used are
```bash
nano resource_monitor.sh
ch 777 resource_monitor.sh
./resource_monitor.sh
```
<img width="800" height="641" alt="2b2a 7 1" src="https://github.com/user-attachments/assets/5bb343e0-57d6-4985-af6c-04798bccf9ea" />
<img width="799" height="657" alt="2b2a 7 2" src="https://github.com/user-attachments/assets/241c9fc5-7391-4d31-9e1c-19d5371c7645" />

### Reflection Questions
What information does the free -h command provide?
free -h shows the system's memory usage in a text format.

How can you modify the script to monitor network usage?
You can modify the script to monitor network usage by adding "ip -s link" to the script

Why is automating system monitoring beneficial for admins?
Automating system monitoring is beneficial for admins as it helps them check the system regularly without having them to manually check by themselves.
It saves time, reduces human error, and helps detect performance issues early which is important for keeping servers stable. 

