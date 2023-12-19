# regions in aws: 

Amazon cloud computing resources are hosted in multiple locations world-wide. These locations are composed of AWS Regions, Availability Zones, and Local Zones. Each AWS Region is a separate geographic area. Each AWS Region has multiple, isolated locations known as Availability Zones.

# main problems for creating asw regions:

1:  Compliance (a country adheres to the applicable rules and laws.)
2:  Latency. Latency is the time it takes for the data to travel from the user to your
    servers.
3:  Costs

# AWS EC2 Security Group:

port 80 use for http webservers
port 443 for https webservers
port 22 for ssh
port 3389 for accessing windows mechine

# Difference between inbound and outbound rules in AWS EC2 security groups?

1: Inbound Rules: These rules control the incoming traffic that's allowed to reach the instances that are associated with the security group. In other words, they define which external services can initiate communication with the instances in your security group. For example, if you want to allow web traffic to your instances, you would specify an inbound rule that allows traffic on port 80 (HTTP) and port 443 (HTTPS).

2: Outbound Rules: These rules control the outgoing traffic that's allowed to leave the instances associated with the security group. This means they define which external services your instances can initiate communication with. By default, security groups allow all outbound traffic. However, you might want to restrict this for security reasons, for instance, to only allow your instances to communicate with specific IP addresses or to access specific services.

#  Most commonly used ports in AWS EC2 inbound rules

The most commonly used ports for inbound rules in AWS EC2 instances are:

1: HTTP (Port 80): This is the default port for unencrypted web (HTTP) traffic. If you're running a web server on your instance and want it to be accessible publicly, you would allow traffic on port 80 1.

2: HTTPS (Port 443): This is the default port for secure web (HTTPS) traffic. If your web server is using SSL/TLS for encrypted connections, you would allow traffic on port 443 1.

3: SSH (Port 22): This port is used for Secure Shell (SSH) traffic, which is typically used for administering the instance remotely in a secure way 1.
RDP (Port 3389): If your instance is running Windows, the Remote Desktop Protocol (RDP) on port 3389 is used for remote administration 1.

4: Database Ports: Depending on the type of database you're running on your instance, you might allow traffic on the default port for that database type. For example, MySQL uses port 3306, PostgreSQL uses port 5432, and Microsoft SQL Server uses port 1433 1.

# What is Elastic IP in AWS EC2?

An Elastic IP address in AWS is a static, public IPv4 address that you can allocate to your AWS resources, such as EC2 instances. Unlike the default public IP address assigned to EC2 instances, which can change when you stop and start the instance, an Elastic IP remains constant as long as you choose to retain it.
