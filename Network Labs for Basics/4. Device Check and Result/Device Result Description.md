# Description for Results of connections

## Overall 
- This section will be results of DHCP service applied well and pings.
- Two PC that are connected to same AP (vlan10) will ping other side and ping Router.
- Server will be static ip and ping Router to check if it's connected. 

## Overall device connections
- ![alt text](<Overall Connection-1.png>)
- Two PCs are connected to AP and it uses fa0/1 port of Switch.
- Server is connected to Switch on fa0/2.
- As described before, switch is connected to router and router is connected to ISP Router. 

## DHCP results and PCs 
-![alt text](<DHCP results-1.png>)
- Both PCs are using DHCP and it is within bendwidth of vlan 10 set up.
- Also uses subnet for vlan 10 and DNS server. 
- ![alt text](<ping results-1.png>)
- Pinged PC0 from Laptop0, successful to ping each other. 
- Also, 192.168.1.1 which is Router vlan 10 ip address, pinged successfully. 

## Server static ip and Ping
- ![alt text](<Server Setup-1.png>)
- This is server ip configuration which is static ip so set them as 192.168.2.100.
- Did same for subnet as vlan 20 also DNS too.
- ![alt text](<Server Ping result-1.png>)
- Pinged 192.168.2.1 which is vlan 20 address of Router successfully.