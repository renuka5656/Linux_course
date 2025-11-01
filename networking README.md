 A quick reference guide for understanding IPs, Subnets, and Private vs Public Networks.
 1
 IP Address
 An IP address identifies a device in a network, just like a house address. IPv4 example:
 192.168.10.5
 2
 Subnet & Subnet Mask
 Subnets divide large networks into smaller, manageable sections. Example: 192.168.10.0/24
 (Mask: 255.255.255.0).
 Total = 256 IPs, Usable = 254 (−2 for network & broadcast).
 3
 Why −2?
 Because the first IP is reserved as Network ID and the last IP as Broadcast Address.
 4
 Private vs Public IPs
 Type
 Description
 Usage
 Private
 Used within local networks (LAN, VPC)
 Not accessible from Internet
 Public
 5
 Globally unique on Internet
 Private IP Ranges
 Used by websites & servers
 Range
 CIDR
 Meaning
 10.0.0.0 – 10.255.255.255
 10.0.0.0/8
 All 10.x.x.x are private
 172.16.0.0 – 172.31.255.255
 172.16.0.0/12
 192.168.0.0 – 192.168.255.255 192.168.0.0/16
 6
 Only 172.16–31 are private
 Only 192.168.x.x are private
 Public vs Private Subnet (Cloud Context)
 Feature
 Public Subnet
 Internet Gateway
 Yes
 Private Subnet
 No
 Internet Access
 Used For
 Security
 7
 Key Formulas
 Yes
 Web servers, Load balancers
 Lower (exposed)
 • Total IPs = 2^(32 − subnet bits)
 • Usable IPs = Total − 2
 • Host Range = Between Network ID & Broadcast
 No direct access
 Databases, App servers
 Higher (internal only)
 Tip: “IP tells who you are, Subnet tells where you belong, Private/Public tells who can reach you.
