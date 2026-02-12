The objective of this task was to configure a basic host-based firewall on a Linux system using UFW (Uncomplicated Firewall) in order to:

Protect the system from unauthorized network access

Allow only required services (e.g., SSH)

Block unnecessary or insecure services (e.g., HTTP)

Verify that firewall rules are correctly applied

Tool Used: UFW (Uncomplicated Firewall)

UFW is a user-friendly interface for managing the iptables firewall on Linux.
It allows administrators to:

Enable or disable the firewall

Allow or deny traffic based on ports or services

View active security rules

Strengthen system security with minimal complexity

Steps Performed
1. Installation of UFW

UFW was installed using:

sudo apt install ufw


The initial status was checked with:

sudo ufw status


At this stage the firewall was inactive by default.

2. Enabling the Firewall

The firewall was activated using:

sudo ufw enable


This ensures that filtering rules are applied automatically on system startup.

3. Configuring Access Rules

To meet the task requirements:

Allow SSH Access (port 22)
sudo ufw allow ssh


or

sudo ufw allow 22


This rule permits remote administration while keeping other ports closed.

Deny HTTP Traffic (port 80)
sudo ufw deny 80


Blocking HTTP prevents unencrypted web access that could expose the system.

4. Verifying Firewall Status

The active rules were confirmed with:

sudo ufw status


Expected result:

SSH → ALLOWED

HTTP → DENIED

All other ports → BLOCKED by default

Significance of the Configuration

A firewall acts as the first line of defense for a system.

Allowing only SSH ensures:

Secure remote login

Encrypted communication

Denying HTTP reduces:

Exposure to web-based attacks

Unauthorized service access

Principle followed: least privilege security model

This configuration demonstrates how a Linux machine can be hardened with only a few commands.
