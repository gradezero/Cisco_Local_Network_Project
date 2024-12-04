# Cisco_Local_Network_Project
Three PC's connect to a router through a switch - Local Network Project
# Cisco Packet Tracer Local Network Project

## **Project Overview**
This project involves creating and configuring a basic local area network (LAN) in Cisco Packet Tracer. It demonstrates the foundational skills required to design and manage networks, including assigning IP addresses, configuring routers and switches, and ensuring connectivity between devices.

## **Objectives**
- Design a network topology using Cisco Packet Tracer.
- Configure devices with IP addressing.
- Test and verify connectivity between all devices.

## **Topology Diagram**
Include a screenshot of your network topology here (exported from Cisco Packet Tracer).

![Network Topology](path/to/your/screenshot.png)

## **Components Used**
- **1 Router**: Configured as the default gateway.
- **1 Switch**: To connect all devices.
- **3 PCs**: Simulating end-user devices.
- **Cables**: Used to establish connections between devices.

## **IP Addressing Scheme**
| Device        | Interface              | IP Address      | Subnet Mask    |
|---------------|------------------------|-----------------|---------------|
| Router        | GigabitEthernet0/0     | 192.168.1.1     | 255.255.255.0 |
| PC1           | -                      | 192.168.1.2     | 255.255.255.0 |
| PC2           | -                      | 192.168.1.3     | 255.255.255.0 |
| PC3           | -                      | 192.168.1.4     | 255.255.255.0 |

## **Configuration Steps**

### **1. Router Configuration**
1. Access the router CLI.
2. Configure the IP address for the router's interface:
   ```bash
   enable
   configure terminal
   interface gigabitethernet0/0
   ip address 192.168.1.1 255.255.255.0
   no shutdown
   exit
   write memory
   ```

### **2. PC Configuration**
For each PC:
1. Go to the **Desktop tab > IP Configuration**.
2. Assign the following settings:
   - **IP Address**: 192.168.1.x (replace `x` with the respective PC number).
   - **Subnet Mask**: 255.255.255.0
   - **Default Gateway**: 192.168.1.1

### **3. Test Connectivity**
1. Use the `ping` command from each PC to test connectivity:
   ```bash
   ping 192.168.1.1
   ping 192.168.1.3
   ping 192.168.1.4
   ```
2. Ensure successful replies to verify network functionality.

## **Key Features**
- Basic static IP configuration.
- Full connectivity between all devices.
- Router setup as a default gateway.

## **Challenges Encountered**
- Misconfigured IP addresses leading to connectivity issues.
- Resolved by verifying IP settings and ensuring all cables were properly connected.

## **Future Improvements**
- Implement DHCP for dynamic IP allocation.
- Configure VLANs for better traffic segmentation.
- Add internet connectivity simulation using NAT.

## **How to Use This Project**
1. Open the `.pkt` file in Cisco Packet Tracer.
2. Review the topology and configuration.
3. Modify or expand the project to include additional features like VLANs or DHCP.

## **Project Files**
- [Local Network Project File](path/to/your/project-file.pkt)
- [Network Topology Screenshot](path/to/your/screenshot.png)

## **Acknowledgments**
This project was created as part of learning networking fundamentals using Cisco Packet Tracer.
