# two-vpc-peering-connection

step 1 - create vpc1 -- create subnet -- create internet gateway -- create route table(in routes add inetnet traffic through igw )

step 2 - create vpc2 -- create subnet -- create internet gateway -- create route table(in routes add inetnet traffic through igw )

step 3 - create vpc peering connection between vpc1(requester) and vpc2(accepter).

step 4 - accept request in vpc2 peering connection 

step 5 - create ec2 instance in  custom vpc1 and vpc2 that recently created -- allow auth-assigned public ip -- launch instance

step 6 - in server1 and server2 ec2 instace edit security group inbound rules -- add  ALL ICMP protocol and HTTP.

step 7 - In route table edit routes and in vpc1-rt, add vpc2 traffic peering connection also in vpc2-rt , add vpc1 traffic(CIDR).

step 8 - check they pinging to each other or not
