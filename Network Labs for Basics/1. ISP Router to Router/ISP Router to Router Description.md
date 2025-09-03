# Description for ISP Router to Router

## Two Devices explanation
- ![alt text](<Two device connection-1.png>)
- Considering a router as a router given by Internet Service Provider(ISP).
- And there is another router for the company itself and those two will be connected together. 
- Which will bring internet access from ISP Router to company Router, then to other devices.
- Two devices are connected with Copper Cross-Over cable, used for connecting same devices.
- Both used Gigabit port 0/0/0 to connect each other. 

## ISP Router Setup 
- ![alt text](<ISP Router Setup-1.png>)
- On this image, it displays that IP used for connecting them is 198.51.100.1 for g0/0/0. 
- It's the port that's directly connected to company Router. 

## Used command and process 
- First, 'enable' command is used to open previliged mode for router. It's where command as admin works. 
- It will change command line as 'Router>' to 'Router#'
- Second, conf t or configure terminal which allows user to manage configuration of devcies 
- It will change command line as 'Router#' to 'Router(config)#'
- 'interface g0/0/0' will directly enter to change configuration for g0/0/0 port also Router will be 'Router(config-if)#'
- 'ip address 198.51.100.1 255.255.255.0' This will set ip address for the port and subnet as /24.
- 'no shutdown' This command will make the port up. 
- 'exit' allowed it to quit current mode then 'show ip interface brief' displays settings of each port

## Company Router Setup
- ![alt text](<Router Setup-1.png>)
- On port g0/0/0 is connected with ISP Router shares same bandwidth to connect each other. 
- Entered terminal mode then changed g0/0/0 port ip address to 198.51.100.2
- g0/0/1 will be used for different purpose, which is connecting to Switch with Vlans