# Third Class

# ACL

Network Access Control List Meaning. A network access control list (ACL) is made up of rules that either allow access to a computer environment or deny it. In a way, an ACL is like a guest list at an exclusive club. Only those on the list are allowed in the doors.

**Note Start VPC > Security >Network ACL**

*Security Groups:*

Operate at the instance level.

Act as a virtual firewall for your instance to control inbound and outbound traffic.

Stateful, meaning if you allow inbound traffic, the corresponding outbound traffic is automatically allowed.

*Network ACLs (Access Control Lists):*

Operate at the subnet level.

Control traffic in and out of one or more subnets.

Stateless, meaning rules define what traffic is allowed, but responses to allowed inbound traffic are not automatically allowed.

So, in summary, security groups are associated with instances and operate at the instance level, while network ACLs are associated with subnets and operate at the subnet level. They are both tools used to control and secure the flow of traffic within a cloud environment.

**Note End VPC > Security >Network ACL**

**DHCP (Dynamic Host Configuration Protocol)**

The function of DHCP is to automatically provide IP addresses.

# Public ip vs Private ip in AWS:

**Public IP Address:**

A public IP address is an address that is routable over the Internet. It is assigned to the instances or resources in AWS that need to be directly accessible from the Internet.

Instances with public IP addresses can communicate with the Internet, and external users can reach these instances over the Internet using the public IP.

Public IP addresses are often associated with resources like Elastic Load Balancers (ELB), Amazon EC2 instances, and other services that need to be accessible publicly.

**Private IP Address:**

A private IP address is used for communication within a private network. Instances within the same Virtual Private Cloud (VPC) can communicate with each other using their private IP addresses.

Private IP addresses are not routable over the Internet and are used for internal communication within the AWS infrastructure.

AWS resources, such as EC2 instances, can have both a private IP address and, if needed, a public IP address.


# IP v4 vs IP v6:


IPv4 (Internet Protocol version 4) and IPv6 (Internet Protocol version 6) are two versions of the Internet Protocol that are used to identify and locate devices on a network. Here are some key differences between IPv4 and IPv6:

**IPv4:**

*Address Length:*

IPv4 addresses are 32-bit numerical labels, which results in a finite number of unique addresses—approximately 4.3 billion.
The addresses are expressed in dotted-decimal format, such as 192.168.1.1.

*Address Exhaustion:*

Due to the limited number of available IPv4 addresses and the rapid growth of the Internet, IPv4 address exhaustion is a significant concern. This has led to the widespread adoption of Network Address Translation (NAT) to conserve IPv4 addresses.

*Private and Public Addresses:*

IPv4 has reserved address ranges for private use within a local network, and these addresses are not routable over the Internet.

*Header Format:*

The IPv4 header is more complex compared to IPv6 and includes fields such as checksum, header length, and options.

*Broadcast:*

IPv4 supports broadcast communication, where a single packet is sent to all devices on a network segment.

**IPv6:**

*Address Length:*

IPv6 addresses are 128-bit, providing an exponentially larger address space than IPv4.
IPv6 addresses are represented in hexadecimal notation separated by colons, such as 2001:0db8:85a3:0000:0000:8a2e:0370:7334.

*Address Notation:*

IPv6 includes the use of double colons (::) to represent consecutive blocks of zeros, making the addresses more concise.

*Address Allocation:*

IPv6 is designed to address the issue of IPv4 address exhaustion by providing a significantly larger pool of unique addresses.

*Header Format:*

The IPv6 header is simpler and more efficient than the IPv4 header, with fewer fields and a more streamlined design.

*No Broadcast:*

IPv6 eliminates broadcast communication, and multicast and anycast are used for similar purposes.

*Auto-Configuration:*

IPv6 includes built-in support for stateless address configuration, allowing devices to configure their own addresses automatically.

