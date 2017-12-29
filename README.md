# aguru
RDS- OLTP
Redshift- OLAP


When creating a NAT instance, disable source-destination check on the instance.
NAT instances must be in a public subnet.  
There must be a route out of the priate subnet to the NAT instance, in order for this to work



Encryption
- Once your RDS instance is encrypted the data stored at rest in the underlying storage is encrypted, as are its automated backups,
read replcas,and snapshots.
- At the present time, encryptong an existing DB instance, is not supported. To use amazon RDS encryption for an existing database, create a new DB instance with encryption enabled and migrate your data into it.

NAT gateways:
- No need to patch
- Not associated with security group

NACL
- rules are evaluated in numerical order
- default nacl, by default it allows all outbound and inbound traffic.
- custom nacl, by default it denies all inbound and outbound traffic until you add rules
- each subnet in your VPC myst be associated with a network ACL, if you dont explicitly associate a subnet with a network ACL, the subnet
is automatically associated with the default network ACL
- You can associate a network ACL with multiple subnets, however a subnet can be associated with only one network ACL at a time. When you associate a network ACL with a subnet, the previous association is removed.


VPC Flowlogs
- You cannot enable flow logs for VPCs that are peered with your VPC unless the peer VPC is in your account.
- You cannot tag a flow log
- After you've created a flow log you cannot change its configuration. you cannot associate a different IAM role with the flow log



NAT is used to provide internet traffic to EC2


if we want private instance to visit s3,
- enable s3 iam on private instance.or
- associate private route table to endpoint


Summary
#### NaT gateways
- scale automatically up to 10GBPs
- No need to patch
- Not associated with security groups
- Automatically assigned a public ip address

- block ip address using nacl, not sg

quiz
- How many VPC am I allowed in each Aws region by default? 5
