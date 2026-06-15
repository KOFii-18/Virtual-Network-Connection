Virtual Machine Setup and Remote Connection
Overview
This project demonstrates the process of configuring networking and security for Azure Virtual Machines (VMs), establishing secure remote connections (RDP for Windows, SSH for Linux), and applying best practices for session management. Due to subscription expiration, live connections could not be completed, but the documented steps reflect the correct procedure.

Steps Documented
1. Configure Networking and Security
    • Created a Network Security Group (NSG).
    • Allowed inbound traffic:
        ◦ Port 3389 (Windows RDP)
        ◦ Port 22 (Linux SSH)
    • Restricted rules to my IP address only for security.
Screenshot: NSG inbound rules showing allowed ports.

2. Identify Connection Endpoints
    • Normally, the VM overview blade displays the Public IP address and DNS name.
    • With an active subscription, this IP is used for RDP/SSH connections.
    • Placeholder IP used for documentation: 52.167.43.210.

3. Establish Windows Connection (RDP)
    • Use Remote Desktop Connection client.
    • Enter the VM’s Public IP.
    • Authenticate with admin credentials.
    • Navigate the desktop to verify access.

4. Establish Linux Connection (SSH)
    • Use SSH client (Terminal/PowerShell/PuTTY).
    • Command: ssh azureuser@<PublicIP>
    • Authenticate with password or SSH key.
    • Verify access with commands like ls, pwd, uname -a.

5. Verify System Access
    • Windows: open File Explorer or Settings.
    • Linux: list files, check installed packages.

6. Secure the Environment
    • Restricted NSG inbound rules to my IP only.
    • Disabled unused ports.
    • Documented SSH key‑based authentication for Linux VM.

7. Manage Remote Sessions
    • Properly terminate RDP and SSH sessions.
    • Ensure VM remains secure and responsive.

Configuration Details
Rule	Port	Protocol	Source
Windows RDP	3389	TCP	My IP only
Linux SSH	22	TCP	My IP only


Limitations Due to Subscription Expiration
At the time of submission, my Azure subscription had expired.
This prevented me from assigning a Public IP address and connecting to the VM via RDP or SSH.
To demonstrate understanding, I documented:
    • How to configure NSG rules for secure access.
    • How to assign a Public IP and DNS endpoint.
    • How to connect using RDP (Windows) and SSH (Linux).
    • Security best practices such as restricting NSG rules to my IP and using SSH keys.

Troubleshooting
    • Expired Subscription: Prevented live connection. Documented steps instead.
    • Firewall Issues: NSG rules must allow Ports 22/3389.
    • Credential Problems: Reset VM password in Azure Portal if login fails.
    • SSH Key Mismatch: Ensure correct public key is uploaded to VM.

Conclusion
Even though the subscription expired, this project demonstrates knowledge of secure remote connectivity to Azure VMs, proper NSG configuration, and best practices for managing sessions. Screenshots and documentation provide proof of understanding the required skills.
