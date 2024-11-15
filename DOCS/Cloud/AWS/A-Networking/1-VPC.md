* VPC has a range of IP address assigned to it know as CIDR Block.
*  Optional secondary IPv4 Block
* Optional IPv6 /56 CIDR Block
* Can have up to 5 IPv6 CIDR blocks, but this limit is adjustable

# CIDR (Classless Inter Domain Routing) Block:
* Used to define the range of IP address that can be used by different resources within a VPC.
* Block size can be between /16 to /28
* Example CIDR Block 192.168.0.0/16 can have IPs ranging between 192.168.0.0 - 192.168.255.255
# VPC Types:
## Default  VPC : Configured by AWS on users behalf & has some default configuration.
* ![[Pasted image 20240827085819.png]]
* ![[Pasted image 20240827090105.png]]
* Default Security Group will allow outbound traffic.
* Default Network Access Control List will allow both inbound & outbound traffic.
## Custom VPC: Configured by user as per the use case.


# Summary:
* ![[Pasted image 20241024104942.png]]
* ![[Pasted image 20241024105006.png]]
* ![[Pasted image 20241024105019.png]]