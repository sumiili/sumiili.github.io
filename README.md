# sumiili.github.io

# Sandboxed Network Configuration Report

## Overview
This report describes the setup of a sandboxed network designed for testing and learning within the Networking and Security Practice module. The network consists of a gateway router, a web server, and a Kali Linux desktop with Juice Shop connected to the web server, whilst Burpsuite is hosted through the Kali Linux for security analysis and testing. The assigned IP ranges that were used are 192.168.36.x and 192.168.136.x.

## VirtualBox Setup
Virtual machines were created for each component via VirtualBox: Ubuntu Gateway router, Wordpress web server, and Kali Linux desktop.

### Configured network adapters for each VM:
Ubuntu Gateway Router: Connected to the internet via NAT to ensure connection, and to internal networks using Internal Network adapters.
Web Server and Kali Desktop: Configured on the internal network with static IPs
## IP Configuration
Assigned the static IP addresses in which were given to members of the class
Verified connectivity between machines using the command "ping"
## Web Server and Juice Shop
Installed a web server on the designated VM and deployed the Juice Shop application.
Configured the web server to accept traffic from the internal network, via port 3000.
## Kali Desktop and Burp Suite
Created a Kali Linux machine and configured it as the primary desktop for testing.
Set up Burp Suite to intercept and analyze traffic between the Kali machine and Juice Shop.
## Gateway Router
Configured the router to enable communication between subnets (192.168.36.2 and 192.168.136.2).
Enabled internet access for internal machines via NAT.
## Testing and Validation
Verified the functionality of Juice Shop by accessing it from the Kali machine.
Tested routing and internet access from all VMs using the ping command and ensuring they can connect to the internet by pinging 8.8.8.8

## Challenges Faced

### Ubuntu Desktop Corruption
The initial plan to use an Ubuntu desktop was revised due to system corruption, where the virtual machine that was being used aborted each time upon launch. Kali Linux was used as an alternative, which offered enhanced tools for testing, as Burpsuite could be installed directly instead of routed.

### Routing Issues
Initially, the gateway router was misconfigured, leading to connectivity issues. The problem was resolved by correctly setting up IP forwarding and NAT rules.

### Application Deployment
Initially, I tried installing Juiceshop via a console command, however this did not work as it would error often. This led to the decision to use a Juiceshop virtual machine host which would be routed via my sandboxed network ecosystem.

## Conclusion
Overall, this sandboxed networking practice provided me with skills to create a simple network of static IP addresses. It served as a foundation for experimenting with tools like Burpsuite and exploring vulnerabilities in Juice Shop. In the future, i would integrate additional services to simulate a pen testing environment.
