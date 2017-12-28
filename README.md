# aguru

When creating a NAT instance, disable source-destination check on the instance.
NAT instances must be in a public subnet.  
There must be a route out of the priate subnet to the NAT instance, in order for this to work


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
