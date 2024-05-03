# Honeypot
A honeypot is a computer security mechanism or decoy system set to detect, deflect, or, in some manner, counteract attempts at unauthorized use of information systems. Generally, a honeypot consists of data (for example, in a network site) that appears to be a legitimate part of the site which contains information or resources of value to attackers. It is actually isolated, monitored, and capable of blocking or analyzing the attackers. This is similar to police sting operations, colloquially known as "baiting" a suspect. It is intentionally vulnerable to be attacked.The benefit of this vulnerable system is to be able to analyze attackers patterns,passwords,usernames and where script kitties are attacking from.
Reason AWS virtual machine is used is because we dont want to use our own network and get hacked and threaten our own resources.AWS virtual machine is containerized and safer for this testing.

Prerequisites
SSH client
AWS account

STEPS
1.Choosing an EC2 in AWS console
A.Region (Tokyo for this example)
B.Type (Operating Sysytem:Debian 11) (Instance Type:T2.XL) in AWS marketplace
Depending on which REGION is chosen will determine the amount and type of attacks are recieved.\
C.Default VPC
D.Subnet: Any
E.Auto assign Public IP: Enabled (Access on public internet)
F.Storage: 128GB (logging attacks and collecting data which add up on storage)
G.Tags: Honey Pot
H.Security Group ; Default until further
Key Pair: Create key pair (This how we log/SSH into server)
Review and launch EC2 Instance

Step 2
2.SSH into the server (honey pot) just created
A.In AWS console go to EC2 dash board and select honey pot server.
B.Select connect option
C.Select SSH client
D.Locate downloaded key pair (usually automatically downloads into download folder)
E.Run the "chmod 400" command.The chmod (change modification) changes the permissions for authorization and logging into specified server.

Step 3 
3.Updates Upgrades Installs
A.Run command:[Sudo apt update] (sudo = super user do)
B.Run command:[Sudo apt upgrade]
C.Run command:[Sudo apt install Git]
D.Git clone (repository):Go to the github account [https://github.com/telekom-security/tpotce]
E.Go to the green button with the code and click on it. It shows three options to clone, we choose "HTTPS" and copy.
F.Go to terminal and Run the command :[git clone https://github.com/telekom-security/tpotce] and hit enter. (pulls all the code seen on this github repository into the server)
G.Run command:[ls] to check if the directory is present. The direcotry "tpotce" should show up. (ls = list)
H.Change from the current "home" directory into "tpotce" directory by running cd command. (cd = change directory)
I.Run command:[cd tpotce]
J:Run command:[ls] to check what files are in your directory/folder.
K:Choose the "install.sh" script
L.Run command:[Sudo ./insall.sh --type=user] This will install this bash script





 



