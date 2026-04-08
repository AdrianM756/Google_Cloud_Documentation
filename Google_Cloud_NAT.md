## Google Cloud NAT

Cloud NAT (Network Address Translation) is a managed Google Cloud service that allows Virtual Machine (VM) instances that do not have external IP addresses to connect to the internet.

Cloud NAT <b>is a regional resource</b>. You can configure it to allow traffic from all ranges of all subnets in a region, from specific subnets in the region only, or from specific primary and secondary CIDR ranges only.

While [Private Google Access](https://github.com/AdrianM756/Google_Cloud_Documentation/blob/main/Private_Google_Access(PGA).md) lets private VMs talk to Google services, Cloud NAT is what they need to talk to the rest of the world (ex., to run ```sudo apt-get update```, or download a library from GitHub).
<br>

## Configuring a Cloud NAT gateway

On the Google Cloud console, type ```Network services``` in the Search field, then click ```Network services``` in the ```Products & Page``` section.

<img width="547" height="425" alt="2026-04-08_20-17" src="https://github.com/user-attachments/assets/2a3e6f67-1132-4808-b9f4-ed9585104176" />
<br>
<br>

Click ```Cloud NAT```.

<img width="249" height="269" alt="2026-04-08_20-21" src="https://github.com/user-attachments/assets/db5bf0a7-d09f-4f27-9439-9c7d4a9089d8" />
<br>
<br>

Click Get started to configure a NAT gateway.

<img width="1126" height="451" alt="2026-04-08_20-21_1" src="https://github.com/user-attachments/assets/cfe1bf24-1041-4a00-b125-6c0a71c51463" />
<br>
<br>

We will name this NAT gateway as ```nat-config```, set the Network to ```privatenet```, then set to the Region to ```us-east4```.

<img width="562" height="566" alt="2026-04-08_20-24" src="https://github.com/user-attachments/assets/dde117b8-fab9-4e56-aadc-620c5c1264bd" />
<br>
<br>

For the Cloud Router, we will create a new router. We will name this as ```nat-router``` then click ```Create```.

<img width="550" height="213" alt="2026-04-08_20-25" src="https://github.com/user-attachments/assets/b9ee92ea-ebe4-406e-93a7-954043a8c3ca" />
<br>
<br>

<img width="570" height="631" alt="2026-04-08_20-26" src="https://github.com/user-attachments/assets/4207834f-0bf4-412b-8002-25aa3b318b24" />
<br>
<br>

Once done, scroll-down and click ```Create```.

<img width="296" height="125" alt="2026-04-08_20-28" src="https://github.com/user-attachments/assets/692d45ed-12b6-4d73-ae55-b557a84e8713" />
<br>
<br>











