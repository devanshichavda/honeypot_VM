# honeypot_VM
Objective

To build a cloud-based security monitoring lab in Azure, utilizing Microsoft Sentinel to detect and respond to suspicious login activity on a Windows virtual machine


Skills Learned

- Cloud Security:
  - Gained practical experience in implementing security monitoring and incident response in a cloud environment using Microsoft Sentinel and Azure Security Center.
- SIEM Deployment and Configuration:
  - Learned to deploy and configure a Security Information and Event Management (SIEM) system, integrating it with a Log Analytics workspace for log collection and analysis.
- Azure Virtual Machine Management:
  - Enhanced skills in deploying, configuring, and securing Windows virtual machines in Azure, including network configuration and access management.
- Security Event Log Analysis:
  - Developed proficiency in analyzing security event logs to identify suspicious activity and potential security threats.
- Alerting and Incident Response:
  - Learned to create custom alert rules in Sentinel to trigger incidents based on specific security events, enabling proactive threat response.
- Azure Monitoring Agent (AMA):
  - Gained experience in deploying and configuring the Azure Monitoring Agent for efficient and secure log forwarding.
- Log Analytics Query Language (Kusto Query Language - KQL):
  - Developed skills in using KQL to query and analyze logs within the Log Analytics workspace.
- Azure Networking:
  - Furthered understanding of Azure networking concepts, including virtual networks, Network Security Groups (NSGs), and public IP addresses.
 

Tools Used:

- Microsoft Azure:
  - Cloud platform for hosting the virtual machine and security services.
- Microsoft Sentinel:
  - Cloud-native SIEM platform for security monitoring, threat detection, and incident response.
- Log Analytics Workspace:
  - Centralized log management service for collecting and analyzing logs from various sources.
- Azure Virtual Machine:
  - Windows Server operating system instance running in Azure.
- Azure Monitoring Agent (AMA):
  - Agent for collecting and forwarding logs and metrics from the virtual machine to Log Analytics.
- Microsoft Remote Desktop:
  - Application for remotely accessing the Windows virtual machine.
- Network Security Groups (NSGs):
  - Firewall rules for controlling network traffic to and from the virtual machine.
- Kusto Query Language (KQL):
  - Query language used for analyzing logs in Log Analytics.
- Windows Security Event Log:
  - Source of security-related events on the Windows VM.


Steps

1. Resource Group Provisioning: Created a resource group in Azure to organize and manage all lab resources. Specified resource group name and location.<img width="1435" alt="Screenshot 2025-04-18 at 9 58 15 AM" src="https://github.com/user-attachments/assets/3bb9ef37-3e5a-4165-a1e7-b89c3f25e6bc" />

2. Virtual Network Setup: Deployed a virtual network (VNet) within the resource group, defining the address space and subnet configuration.<img width="1434" alt="Screenshot 2025-04-18 at 10 01 28 AM" src="https://github.com/user-attachments/assets/ee92fc15-8c90-4b61-bb42-9d7cfa075d19" />

3. Virtual Machine Deployment: Created a Windows Server virtual machine within the designated subnet. Specified VM size, operating system image, and administrator credentials.<img width="1438" alt="Screenshot 2025-04-18 at 10 33 55 AM" src="https://github.com/user-attachments/assets/79f976c5-da9c-4152-ad97-a3b9cb1aa4fa" />

4. Initial Network Access: Configured the Network Security Group (NSG) to allow inbound traffic.<img width="1434" alt="Screenshot 2025-04-18 at 10 47 10 AM" src="https://github.com/user-attachments/assets/08237f7e-53c4-43fb-9be0-3c309d8a906f" /><img width="1437" alt="Screenshot 2025-04-18 at 10 44 58 AM" src="https://github.com/user-attachments/assets/b09ef692-1721-4693-a24b-264d9794f3aa" />


5. Remote Connection: Established a remote desktop connection to the Windows VM using its public IP address and the Microsoft Remote Desktop application.
6. Windows Firewall Configuration: Disabled the Windows Firewall for initial setup.
7. Connectivity Validation: Confirmed network connectivity by pinging the VM's public IP address from the local machine by pinging the IP address.
8. Log Analytics Workspace Creation: Created a Log Analytics workspace to store and analyze logs. Specified workspace name, resource group, and location.<img width="1438" alt="Screenshot 2025-04-19 at 4 19 37 PM" src="https://github.com/user-attachments/assets/ffce3ac4-690f-4aef-84d9-f9cff07693f3" />

9. Sentinel Connection: Linked the Log Analytics workspace to a Microsoft Sentinel instance.
10. Security Event Connector Deployment: Deployed the Windows Security Event Connector solution within the Log Analytics workspace.<img width="1432" alt="Screenshot 2025-04-21 at 3 11 31 PM" src="https://github.com/user-attachments/assets/c162e95e-2d64-439e-8d85-3a488251e715" />

11. Azure Monitoring Agent Installation: Installed and configured the Azure Monitoring Agent (AMA) on the Windows VM, ensuring it was connected to the correct Log Analytics workspace.
12. Data Collection Rule Configuration: Enabled the built-in data collection rule for Windows Security Events to forward logs to the Log Analytics workspace.<img width="1437" alt="Screenshot 2025-04-21 at 3 16 22 PM" src="https://github.com/user-attachments/assets/73c3d9c0-85d7-4deb-aa72-1c6fe8cc7484" />

13. Log Analysis and Observation: Queried the Log Analytics workspace using KQL to analyze security events. Observed a burst of failed login attempts.<img width="1432" alt="Screenshot 2025-04-21 at 3 28 37 PM" src="https://github.com/user-attachments/assets/e8f53c8a-14af-46b8-8478-be55551460df" />

14. Sentinel Alert Rule Creation: Created a custom alert rule in Sentinel to trigger an incident based on failed login attempts for the "Administrator" account. Specified alert logic, severity, and incident creation criteria.<img width="1404" alt="Screenshot 2025-04-21 at 3 56 33 PM" src="https://github.com/user-attachments/assets/92bb2dc7-184f-4166-b4cd-92e997bffad7" /><img width="1433" alt="Screenshot 2025-04-21 at 4 01 00 PM" src="https://github.com/user-attachments/assets/817b1504-19f2-4b95-b744-97d5bf83a35b" />




