Virtual Machine Setup and Remote Connection
Overview
This project demonstrates how to configure networking and security for Azure Virtual Machines (VMs), establish secure remote connections (RDP for Windows, SSH for Linux), and implement Azure Bastion for secure browser-based access. Due to subscription expiration, live screenshots could not be provided, but all steps are documented to reflect correct procedure and best practices.

VM Creation
Windows VM
    • Image: Windows Server 2019 Datacenter
    • Size: B2s (2 vCPU, 4 GB RAM)
    • Storage: Standard HDD, 30 GB
    • Authentication: Username + password
Linux VM
    • Image: Ubuntu 20.04 LTS
    • Size: B2s (2 vCPU, 4 GB RAM)
    • Storage: Standard HDD, 30 GB
    • Authentication: SSH key pair

Networking and Security
    • Created a Network Security Group (NSG).
    • Allowed inbound traffic:
        ◦ Port 3389 (Windows RDP)
        ◦ Port 22 (Linux SSH)
    • Restricted rules to my IP address only.
    • Disabled unused ports.

Connection Steps
Windows VM (RDP)
    1. Open Remote Desktop Connection.
    2. Enter Public IP or DNS name.
    3. Authenticate with admin credentials.
    4. Verify access by navigating desktop and system settings.
Linux VM (SSH)
    1. Open Terminal or PuTTY.
    2. Run: ssh azureuser@<PublicIP>
    3. Authenticate with password or SSH key.
    4. Verify access with commands (ls, pwd, uname -a).

Azure Bastion Setup
    • Deployed Azure Bastion in the same VNet as the VMs.
    • Configured Bastion to allow browser-based RDP/SSH.
    • Benefits:
        ◦ No need for Public IPs.
        ◦ Secure access directly from Azure Portal.
    • Connection steps:
        ◦ Navigate to VM → Connect → Bastion.
        ◦ Enter credentials.
        ◦ Access VM securely in browser.

Configuration Details
Rule	Port	Protocol	Source
Windows RDP	3389	TCP	My IP only
Linux SSH	22	TCP	My IP only


Troubleshooting
    • Expired Subscription: Prevented live connection. Documented steps instead.
    • Firewall Issues: NSG rules must allow Ports 22/3389.
    • Credential Problems: Reset VM password in Azure Portal if login fails.
    • SSH Key Mismatch: Ensure correct public key is uploaded to VM.

Limitations Due to Subscription Expiration
At the time of submission, my Azure subscription had expired.
This prevented me from assigning a Public IP address and connecting to the VM via RDP or SSH.
To demonstrate understanding, I documented:
    • VM creation (Windows + Linux).
    • NSG configuration and security best practices.
    • RDP and SSH connection steps.
    • Azure Bastion deployment and usage.

Conclusion
This project demonstrates knowledge of secure remote connectivity to Azure VMs, proper NSG configuration, and Bastion deployment. While live screenshots could not be provided due to subscription expiration, the documentation reflects the correct procedure and best practices required by the rubric.
