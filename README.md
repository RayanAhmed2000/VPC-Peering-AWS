# VPC-Peering-AWS
This repo contains steps and important points to remember for error free VPC Peering
# Create VPC's
- Create *vpc1*
  - 10.0.0.0/24
- Create *vpc2*
  - 192.168.0.0/24
# Create Subnets
- Create *vpc1subnet*
  - 10.0.0.0/28
- Create *vpc2subnet*
  - 192.168.0.0/28
# Create IGW's
- *vpc1-igw* attach it to vpc1
- *vpc2-igw* attach it to vpc2
# Create Route tables
- *vpc-rt-1* associate with *vpc1subnet*
- *vpc-rt-2* associate with *vpc2subnet*
- In route table add igw's accordingly
# Create Security Groups
- *vpc-1-sg* in *vpc1* and allow All TCP and ICMP v4
- *vpc-2-sg* in *vpc2* and allow All TCP and ICMP v4
# Create a peering connection 
- Accept the peering request
- Now we have to add path of peering in route tables of both vpc's
- Go to *vpc-rt-1* add route 192.168.0.0/16	as destination and peering ID as target
- Go to *vpc-rt-2* add route 10.0.0.0/16 as destination and peering ID as target





