Objective

The objective of this task was to use Nmap (Network Mapper) to scan a system on the local network in order to:

Detect active hosts

Identify open ports

Determine running services

Understand potential security risks associated with those services

Tool Used: Nmap

Nmap is a network scanning tool used for:

Host discovery

Port scanning

Service and version detection

Security auditing

It helps administrators understand what services are exposed on a machine and whether any unnecessary or risky ports are open.

Steps Performed
1. Installation of Nmap

Nmap was installed on the Ubuntu system using:

sudo apt install nmap


The installation was verified with:

nmap -v

2. Performing Network Scan

A basic scan was first executed:

nmap 192.168.1.7


Since the host blocked ping probes, the scan was repeated with:

nmap -Pn 192.168.1.7


To detect service versions:

nmap -Pn -sV 192.168.1.7


An aggressive scan for detailed information:

nmap -Pn -A 192.168.1.7
