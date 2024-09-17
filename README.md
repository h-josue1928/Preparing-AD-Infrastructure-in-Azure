# Preparing-AD-Infrastructure-in-Azure

Setup Domain Controller in Azure
—
Create a Resource Group
Create a Virtual Network and Subnet
Create the Domain Controller VM (Windows Server 2022) named “DC-1”
Username: labuser
Password: Cyberlab123!
After VM is created, set Domain Controller’s NIC Private IP address to be static
Log into the VM and disable the Windows Firewall (for testing connectivity)

![image](https://github.com/user-attachments/assets/5c6f977f-2b47-4478-8d79-3772cd75385c)

![image](https://github.com/user-attachments/assets/7b6f115c-77b9-423a-b865-1f2a50e3b3d7)

![image](https://github.com/user-attachments/assets/fe950f04-abac-4d24-b7fd-6cfe6f75afde)

Setup Client-1 in Azure
—
Create the Client VM (Windows 10) named “Client-1”
Username: labuser
Password: Cyberlab123!
Attach it to the same region and Virtual Network as DC-1
After VM is created, set Client-1’s DNS settings to DC-1’s Private IP address
![image](https://github.com/user-attachments/assets/9f48427e-c110-423d-a343-aae804a1a6a3)

From the Azure Portal, restart Client-1
Login to Client-1
Attempt to ping DC-1’s private IP address
Ensure the ping succeeded
![image](https://github.com/user-attachments/assets/222938d1-12d7-42a4-8b6e-787e287fd48c)

From Client-1, open PowerShell and run ipconfig /all
The output for the DNS settings should show DC-1’s private IP Address
![image](https://github.com/user-attachments/assets/89aae8a1-3351-4844-856a-3d55786a6e62)
