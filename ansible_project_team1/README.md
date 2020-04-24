Create the VPC using ansible. Make sure the code work in every region of AWS.  
==============================================================================
<img width="756" alt="Screenshot_517" src="https://user-images.githubusercontent.com/13994900/80230019-ec4b9400-8616-11ea-95b5-dd19c6d8eefc.png">



Requirements
=============
In order to work with Python 2.7.16, install next packages:
* yum install ansible -y
* amazon-linux-extras install ansible2
* yum install python-boto3 -y
* yum install python-pip -y
*  pip install boto awscli

 Architecture
=============

<img width="562" alt="Screenshot_522" src="https://user-images.githubusercontent.com/13994900/80238182-94675a00-8623-11ea-8fae-ca0373688e1f.png">

Dependencies 
==============

* The architecture of VPC is the core for the project.
It is not depended on another team and is not solely built to be region depended, because of the flexibility of the code, it can be easily configured to work in any of the available regions.
Make changes in region.yaml file – to build the infrastructure described above.

* It is a must to enable DHCP in order to auto-assign Public IPs. DHCP - Dynamic Host Configuration Protocol is a network management protocol used on Internet Protocol networks whereby a DHCP server dynamically assigns an IP address and other network configuration parameters to each device on a network so they can communicate with other IP networks.

<img width="859" alt="Screenshot_526" src="https://user-images.githubusercontent.com/13994900/80239004-0c824f80-8625-11ea-986c-2aca47309d5d.png">



Flexibility
============
The project has built with a soft code. Our soft code works flexible with in every region because we have collected all the neccessery codes inside "all.yaml" file. The code should be changed just in region part. For example:
``` 
region: "us-west-2"
```
```
region: "us-east-1"
 ```
 ``` 
region: "eu-west-2"
 ```
 ## Steps: 
 1. Open file
 2. Change region part
 3. Save file 
 4. In your vm run `ansible-playbook all.yaml `




Issues 
=======
1)  This  issue you will get when the List of Elasti IPs will be 5. In order to solve the problem, delete one EIPs and run again.

<img width="954" alt="Screenshot_492" src="https://user-images.githubusercontent.com/13994900/80157006-e1e3b880-858a-11ea-8833-1b62cdc3e130.png">

2) To solve the next issue, use #map_public: yes , under each Public Subnet!
<img width="924" alt="Screenshot_491" src="https://user-images.githubusercontent.com/13994900/80157055-ffb11d80-858a-11ea-9e28-276768fd89b8.png">

<img width="244" alt="Screenshot_494" src="https://user-images.githubusercontent.com/13994900/80157606-2b80d300-858c-11ea-8a87-4f1b0ee8a178.png">
                              
 
Time spent on  project
===========================

<img width="350" alt="Screenshot_527" src="https://user-images.githubusercontent.com/13994900/80239295-96cab380-8625-11ea-9788-1bc1534122c0.png">

<img width="400" alt="Screenshot_529" src="https://user-images.githubusercontent.com/13994900/80239422-d6919b00-8625-11ea-9d4e-fecc255702b5.png">
