## Private Google Access (PGA)

Private Google Access (PGA) is a Google Cloud feature that allows Virtual Machine (VM) instances with only internal (private) IP addresses to reach Google APIs and services (like Cloud Storage, BigQuery, or Pub/Sub). 

PGA provides a "private" bridge to these services without requiring a public IP or a NAT. This helps keep workloads private while still interacting with Google services.

**NOTE:** By default, Private Google Access is disabled on a VPC network.
<br>

## Enable Private Google Access (PGA)

Private Google Access is enabled at the subnet level. When it is enabled, instances in the subnet that only have private IP addresses can send traffic to Google APIs and services through the default route (```0.0.0.0/0```) with a next hop to the default internet gateway. On this demo, we will enable PGA on an existing network(privatenet).
<br>

In the Cloud console, in the Navigation menu, click ```VPC network``` > ```VPC networks```.

<img width="476" height="904" alt="2026-04-08_19-59" src="https://github.com/user-attachments/assets/225beeb8-9c5c-4ed9-86d1-3bf1718f7f48" />
<br>
<br>

Click ```privatenet``` to open the network.

<img width="340" height="187" alt="2026-04-08_20-01" src="https://github.com/user-attachments/assets/115e6d83-5efb-4937-95fa-c9c30a408ab4" />
<br>
<br>

Click ```Subnets```, and then click ```privatenet-us```.

<img width="274" height="384" alt="2026-04-08_20-02" src="https://github.com/user-attachments/assets/adc9179a-8f41-4128-8837-c7a7f1eacc54" />
<br>
<br>

Click ```Edit```.

<img width="423" height="320" alt="2026-04-08_20-03" src="https://github.com/user-attachments/assets/dd2bbd7b-c2d4-429b-9a73-a092470a62f8" />
<br>
<br>

For Private Google access, select ```On``` then click ```Save```.

<img width="397" height="375" alt="2026-04-08_20-05" src="https://github.com/user-attachments/assets/c01b2976-5c42-4603-911b-33e9fdc67457" />
<br>
<br>












