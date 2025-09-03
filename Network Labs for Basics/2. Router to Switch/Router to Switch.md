# Setting up for Router to Switch with Vlans 

## Overall view
- ![alt text](<Router to Switch connected-1.png>)
- Router0 is connected with Switch0 and Router0 used g0/0/1 and connect Switch0 using fa0/24 to connect.
- Router0 uses vlan to seperate networks so Switch0 can seperately connect networks for PC and Server.

## Router Vlan Setup
- ![alt text](<Vlan tagging for Router-1.png>)
- Since there is IP already assigned which isn't Vlan, delete it with command 'no ip shutdown'
- However, still did no shutdown since this port needs to be used. 
- 'interface g0/0/1.10' allows to configure for vlan 10 sub interface. 
- Using 10, 20, 30 and more will allow to create more sub interfaces.
- 'encapsulation dot1Q 10' This command makes g0/0/1.10 to process only vlan 10 interface. 
- 'ip address 192.168.1.1 255.255.255.0' Set ip address for vlan 10.
- Did the same with vlan 20 but as g0/0/1.20. 
- ![alt text](<Router Setup Result-1.png>)
- Then show ip interface will display like this, displaying both vlans

## Switch Setup
- ![alt text](<Switch Setup-1.png>)
- On Switch, set fa0/1 as vlan 10 and fa0/2 as vlan 20
- After accessing terminal mode, 'vlan 10' will allow configure for vlan 10.
- 'name CLIENT' will make vlan 10 name is CLIENT. Do the same for vlan 20 but as SERVER. 
- 'interface fa0/1' to access fa0/1 port then 'switch portmode access' to enter access mode. 
- On access mode, it allows assigning vlan to current port. 
- 'switchport access vlan 10' will set this port for vlan 10.
- Did the same for fa0/2 but as vlan 20.
- Then access to fa0/24. 'switchport mode trunk' will turn on trunk on this port.
- Since fa0/24 will take vlan 10 and 20 coming from router, it vlans to be seperated to different ports. 
