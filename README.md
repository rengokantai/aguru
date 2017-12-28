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
