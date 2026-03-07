## Creating a VPC Network

On this demo, we will create a VPC network, create a firewall rule, and attach it to a virtual machine to google cloud
<br>

## Create the managementnet network

In the Cloud console, navigate to Navigation menu (Navigation menu icon) > VPC network > VPC networks.
<br>
<img width="455" height="857" alt="vpc-network-1" src="https://github.com/user-attachments/assets/39dcc3de-20fa-45c3-8b05-e2c98f20a354" />

Notice the default and mynetwork networks with their subnets. Each Google Cloud project starts with the default network. In addition, the mynetwork network has been premade as part of your network diagram.
Click Create VPC Network.
<br>
<img width="783" height="299" alt="vpc-network-2" src="https://github.com/user-attachments/assets/a3818c81-0df3-46b6-a10d-b033f00386b5" />

Set the Name to managementnet.
<br>
<img width="827" height="181" alt="vpc-network-3" src="https://github.com/user-attachments/assets/08199042-eeb4-439b-981e-7b12dc958ee2" />

For Subnet creation mode, click Custom. Set the following values, leave all other values at their defaults:
* Name: ```managementsubnet-1```
* Region: ```us-west1```
* IPv4 range:	```10.130.0.0/20```
<br>

Click Done and create.
<br>
<img width="378" height="783" alt="vpc-network-4" src="https://github.com/user-attachments/assets/dbdc0e08-68d5-4fed-9009-433b7ab38a97" />
<br>
<img width="489" height="233" alt="vpc-network-6" src="https://github.com/user-attachments/assets/9ebca2fa-f6d0-4cc0-bf14-9d3b719dad12" />
<br>

## Create the firewall rules for managementnet
Create firewall rules to allow SSH, ICMP, and RDP ingress traffic to VM instances on the managementnet network. In the Cloud console, navigate to Navigation menu (Navigation menu icon) > VPC network > Firewall.
<br>
<img width="414" height="839" alt="vpc-firewall-1" src="https://github.com/user-attachments/assets/099991c9-c79d-46f1-8a08-333e59e9f2b2" />

Click + Create Firewall Rule.
<br>
<img width="816" height="191" alt="vpc-firewall-2" src="https://github.com/user-attachments/assets/33c07962-a3f4-469e-aaaf-17ad6e3fe709" />

Set the following values, leave all other values at their defaults:
* Name: ```managementnet-allow-icmp-ssh-rdp```
* Network: ```managementnet```
* Targets: ``All instances in the network```
* Source filter: ```IPv4 Ranges```
* Source IPv4 ranges: ```0.0.0.0/0```
* Protocols and ports: Specified protocols and ports, and then check ``tcp``, type: ``22``, ``3389``; and check Other protocols, type: ``icmp``.
<br>
<img width="657" height="888" alt="vpc-firewall-3" src="https://github.com/user-attachments/assets/b440ea68-2534-42c8-a601-a3ab7d44a099" />
<br>
<img width="594" height="911" alt="vpc-firewall-4" src="https://github.com/user-attachments/assets/8bdb5ca2-d883-4085-b573-93082572b44a" />
<br>
Click Close then Click Create.
<br>
<img width="364" height="145" alt="vpc-firewall-6" src="https://github.com/user-attachments/assets/c681d160-75a3-42ae-951c-eeb38ddba839" />
<br>

## Create an Instance

In the Cloud console, navigate to Navigation menu > Compute Engine > VM instances.
<br>
<img width="507" height="576" alt="vpc-instance-1" src="https://github.com/user-attachments/assets/1a407851-22fb-4198-b24e-6ac089d43eb4" />
<br>

Click Create Instance.
<br>
<img width="885" height="231" alt="vpc-instance-2" src="https://github.com/user-attachments/assets/0d221175-230a-441b-9307-d9791661ea70" />
<br>

In the Machine configuration, set the following values, leave all other values at their defaults:
Name: ```managementnet-vm-1```
Region: ```us-west1```
Zone: ```us-west1-a```
Series: ```E2```
Machine Type: ```e2-micro```
<br>
<img width="762" height="187" alt="vpc-instance-3" src="https://github.com/user-attachments/assets/d74b1bb9-bc82-4350-85f1-9299fdfc47c1" />
<br>
<img width="754" height="756" alt="vpc-instance-4" src="https://github.com/user-attachments/assets/567c5215-f8d8-47ea-9403-3ac90755dd52" />

Click Networking.
<br>
<img width="246" height="513" alt="vpc-networking-1" src="https://github.com/user-attachments/assets/f910409a-0a87-4df1-93c2-4902220647bb" />
<br>

For Network interfaces, click the dropdown to edit. Set the following values, leave all other values at their defaults:
* Network: ```managementnet```
* Subnetwork: ```managementsubnet-1```
<br>
<img width="500" height="160" alt="vpc-networking-2" src="https://github.com/user-attachments/assets/54b13f4b-3119-422c-916f-a29f1934fad3" />
<br>

Click Done.
<br>



