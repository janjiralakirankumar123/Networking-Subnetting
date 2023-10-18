## Question: calculate the four subnets for Original IP: 192.167.35.0/16.

## Solution:

**Step 1: Understand the Original IP Address**
- The original IP address is "192.167.35.0/16."
- In binary, this IP address looks like this:
  - 11000000.10100111.00100011.00000000
- The "/16" subnet mask indicates that the first 16 bits are reserved for the network portion, and the remaining 16 bits are for host addresses.
- **IP Address Class:** This IP address falls into Class C because the first octet (192) falls within the range of 192-223, which is the designated range for Class C addresses. Class C addresses are typically used for small to medium-sized networks.

**Step 2: Determine How Many Subnets Are Needed**
- We want to create four smaller subnets from the original IP address.

**Step 3: Borrow Bits for Subnetting**
- To create four subnets, we need to borrow additional bits from the host portion of the IP address. We calculate how many bits to borrow using the formula 2^x = number of subnets needed, where "x" is the number of bits to borrow.
- In this case, 2^x = 4, so we need to borrow 2 bits because 2^2 = 4.

**Step 4: Calculate the New Subnet Mask**
- The original subnet mask was /16, which is represented in binary as:
  - 11111111.11111111.00000000.00000000
- When we borrow 2 bits, we add them to the host portion of the subnet mask, resulting in a new subnet mask of /18, which is represented in binary as:
  - 11111111.11111111.11000000.00000000

**Step 5: Divide the Original IP Address into Subnets**

Now, let's calculate the four subnets:

**Subnet 1:**
- Network Address (Decimal): 192.167.0.0
- Network Address (Binary): 11000000.10100111.00000000.00000000
- Usable IP Range (Decimal): From 192.167.0.1 to 192.167.63.254
- Usable IP Range (Binary): From 11000000.10100111.00000000.00000001 to 11000000.10100111.00111111.11111110
- Broadcast Address (Decimal): 192.167.63.255
- Broadcast Address (Binary): 11000000.10100111.00111111.11111111
- Total Number of Hosts: 16,382

**Subnet 2:**
- Network Address (Decimal): 192.167.64.0
- Network Address (Binary): 11000000.10100111.01000000.00000000
- Usable IP Range (Decimal): From 192.167.64.1 to 192.167.127.254
- Usable IP Range (Binary): From 11000000.10100111.01000000.00000001 to 11000000.10100111.01011111.11111110
- Broadcast Address (Decimal): 192.167.127.255
- Broadcast Address (Binary): 11000000.10100111.01011111.11111111
- Total Number of Hosts: 16,382

**Subnet 3:**
- Network Address (Decimal): 192.167.128.0
- Network Address (Binary): 11000000.10100111.10000000.00000000
- Usable IP Range (Decimal): From 192.167.128.1 to 192.167.191.254
- Usable IP Range (Binary): From 11000000.10100111.10000000.00000001 to 11000000.10100111.10011111.11111110
- Broadcast Address (Decimal): 192.167.191.255
- Broadcast Address (Binary): 11000000.10100111.10011111.11111111
- Total Number of Hosts: 16,382

**Subnet 4:**
- Network Address (Decimal): 192.167.192.0
- Network Address (Binary): 11000000.10100111.11000000.00000000
- Usable IP Range (Decimal): From 192.167.192.1 to 192.167.255.254
- Usable IP Range (Binary): From 11000000.10100111.11000000.00000001 to 11000000.10100111.11011111.11111110
- Broadcast Address (Decimal): 192.167.255.255
- Broadcast Address (Binary): 11000000.10100111.11011111.11111111
- Total Number of Hosts: 16,382

This subnetting configuration divides the original /16 network into four /18 subnets, each accommodating approximately 16,382 hosts.
