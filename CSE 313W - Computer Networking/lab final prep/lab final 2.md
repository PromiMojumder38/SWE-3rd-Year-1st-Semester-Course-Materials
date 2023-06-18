# Network Subnetting

Given an IP address of 192.168.10.0, we need to subnet the network to accommodate a maximum of 26 hosts in each subnet. Here's the solution:

Subnet mask: 255.255.255.224 (or /27 in CIDR notation)

The subnet mask in binary is 11111111.11111111.11111111.11100000.

Calculations:
- Number of hosts per subnet: 2^5 = 32
- Usable hosts per subnet: 32 - 2 = 30 (subtracting the network and broadcast addresses)
- Number of subnets: 2^3 = 8
- Network address: 11000000.10101000.00001010.00000000 (192.168.10.0/27)
- Range: 256 - 224 = 32

Subnet Details:

| Subnet | Network Address   | First Usable     | Last Usable      | Broadcast Address |
| ------ | ----------------- | ---------------- | ---------------- | ----------------- |
| 0      | 192.168.10.0      | 192.168.10.1     | 192.168.10.30    | 192.168.10.31    |
| 1      | 192.168.10.32     | 192.168.10.33    | 192.168.10.62    | 192.168.10.63    |
| 2      | 192.168.10.64     | 192.168.10.65    | 192.168.10.94    | 192.168.10.95    |
| 3      | 192.168.10.96     | 192.168.10.97    | 192.168.10.126   | 192.168.10.127   |
| 4      | 192.168.10.128    | 192.168.10.129   | 192.168.10.158   | 192.168.10.159   |
| 5      | 192.168.10.160    | 192.168.10.161   | 192.168.10.190   | 192.168.10.191   |
| 6      | 192.168.10.192    | 192.168.10.193   | 192.168.10.222   | 192.168.10.223   |
| 7      | 192.168.10.224    | 192.168.10.225   | 192.168.10.254   | 192.168.10.255   |
