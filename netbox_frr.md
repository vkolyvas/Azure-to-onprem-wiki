# NetBox + FRRouting – Installation & Configuration
NetBox is a network Source of Truth (SoT). FRRouting (FRR) is an open-source network routing stack.
**NetBox – Installation**
1.	Install PostgreSQL and Redis.
2.	Install the NetBox release (package or from source).
3.	Configure Gunicorn as the WSGI application server.
4.	Put Nginx (or another reverse proxy) in front of Gunicorn.
**NetBox – Configuration**
•	Create and manage:
  - Sites, regions, racks
  - Prefixes and IP addresses
  - VLANs and VRFs
  - Devices, interfaces, and connections
•	Integrate with automation tools (Ansible, Nornir, etc.) for dynamic inventory and config generation.
**FRRouting – Installation**
bash
```
sudo apt update
sudo apt install -y frr frr-pythontools
```
**FRRouting – Configuration**
1.	Edit ```/etc/frr/daemons``` to enable the protocols you need (e.g., bgpd, ospfd).
2.	Edit ```/etc/frr/frr.conf``` to define routing:
•	OSPF configuration
•	BGP neighbors and address families
•	VRFs and route redistribution
3.	Restart FRR:
bash
```
sudo systemctl restart frr
```
