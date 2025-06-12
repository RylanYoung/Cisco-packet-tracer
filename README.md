# Cisco, Small home/Office netowrk

## Objective
Design and secure a small home office network in Cisco Packet Tracer featuring 4 subnets with VLANs, VLAN trunking, DHCP, full router/switch configuration, ACL-based access controls, and security best practices to simulate real-world network hardening. And enhance my practical networking security skills

### Skills Learned
[Bullet Points - Remove this afterwards]

- Network design and segmentation
- Router/Switch configurations
- Dynamuc Host Configurations Protocol (DHCP)
- Access Control Lists (ACLs)
- Network Security Hardening
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
[Bullet Points - Remove this afterwards]

- Cisco pascket tracer
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Steps
1️⃣ **Device Layout & Connections**
Add devices:

Cisco Router

2x Cisco Switches

2x Wireless Access Points

Multiple End Devices (PCs, Laptops, Wireless Devices)

Connect:

Router → Switches

Switches → Access Points

End Devices → Switches or Wireless

2️⃣ **VLAN Configuration**
Create 4 VLANs for departments:

VLAN 10: HR

VLAN 20: Sales

VLAN 30: IT

VLAN 40: Management

Assign switch ports to correct VLANs.

3️⃣ **Trunking**
Enable trunking between:

Router ↔ Switch 1

Switch 1 ↔ Switch 2

Allow all VLANs on trunk ports.

4️⃣ **Router Subinterfaces** (Router-on-a-Stick)
Create router subinterfaces for each VLAN.

5️⃣ **Subnetting the Network**
Subnet using 255.255.255.192 mask (4 subnets):

VLAN	Subnet	Gateway Example
10	192.168.1.0/26	192.168.1.1
20	192.168.1.64/26	192.168.1.65
30	192.168.1.128/26	192.168.1.129
40	192.168.1.192/26	192.168.1.193

6️⃣ **DHCP Configuration**
Create DHCP pools for each subnet.

Assign correct default gateways per VLAN.

7️⃣ **Recreate Subinterfaces** 
Ensure router subinterfaces match correct VLAN assignments and IP addressing.

8️⃣ **Wireless Access Points**
Configure SSIDs and WPA2-PSK passwords.

Assign IP addresses to APs.

Connect wireless clients to appropriate SSIDs.

9️⃣ **Connectivity Testing**
Ping between VLANs to verify routing.

Confirm DHCP assigns correct addresses to devices.

🔟 **Troubleshooting DHCP** (IT Department)
Identified the incorrect gateway in IT DHCP pool.

Updated DHCP default router.

Renewed DHCP leases for IT devices.

1️⃣1️⃣ **Inbound ACL** (Device Access Control)
Create ACL to limit external access:

Only 5 authorized workstations allowed inbound communication.

Apply ACL inbound on router.

1️⃣2️⃣ **Outbound ACL** (Service Filtering)
Create ACL to allow only:

HTTP (80)

HTTPS (443)

DNS (53)

ICMP (Ping)

Apply ACL outbound to restrict allowed services.

1️⃣3️⃣ **Router Security Hardening**
Apply security best practices:

Set console password: Passw0rd

Set VTY (Telnet/SSH) password: Passw0rd1

Configure enable secret for privileged access

Enable password encryption

Apply banner message (legal warning)

Disable unused services

1️⃣4️⃣ **Final Testing**
Verify:

VLAN routing

DHCP operation

Wireless connectivity

ACL filtering (inbound & outbound)

Router security configuration
