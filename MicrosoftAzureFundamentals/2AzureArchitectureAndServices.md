
## Microsoft Azure
Azure provides more than 100 services that enable you to do everything from running your existing applications on virtual machines to exploring new software paradigms, such as intelligent bots and mixed reality.
It is a global cloud provider.

### Practice on Sandbox
- Activate Sandbox
- Give Permissions
- Powershell will appear after authentification.
- Powershell Specific Command: Get-date
- Azure Specific Commands: az version
- **If you’re more familiar with BASH, you can use BASH command instead by shifting to the BASH CLI.**
- Command: bash
- Bash specific Command: 
  - date
  - az upgrade
- You can change back to PowerShell mode by entering pwsh on the BASH command line.
- **Use Azure CLI interactive mode**
- Command: az interactive
![image](https://user-images.githubusercontent.com/74251229/194736893-907c27d1-7776-4b7e-a0fc-172fbf59ccd2.png)
- Once initialized, you can use the arrow keys or tab to help complete your commands. Interactive mode is set up specifically for Azure, so you don't need to enter az to start a command (but you can if you want to or are used to it). 
- Command: exit {to come out of Azure CLI interactive mode. }

### The core architectural components of Azure may be broken down into two main groupings: the physical infrastructure, and the management infrastructure.
### [Tour of Microsoft Data Centers](https://infrastructuremap.microsoft.com/)

#### Physical Infrastructure
- **Datacenter's resources arranged in racks, with dedicated power, cooling, and networking infrastructure.**
- **Datacenters are grouped into Availability Zones.**
- **Availability Zones are grouped into Regions.**
  - An availability zone is set up to be an isolation boundary. If one zone goes down, the other continues working. Availability zones are connected through high-speed, private fiber-optic networks.
  - To store data in more than 1 availability zone, customer needs to pay for duplicacy and tranfering the data among availability zones.
  - not all Azure Regions currently support availability zones.
  - Availability zones are primarily for VMs, managed disks, load balancers, and SQL databases. Azure services that support availability zones fall into three categories:
    - Zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses).
    - Zone-redundant services: The platform replicates automatically across zones (for example, zone-redundant storage, SQL Database).
    - Non-regional services: Services are always available from Azure geographies and are resilient to zone-wide outages as well as region-wide outages.
    
![image](https://user-images.githubusercontent.com/74251229/194738361-89dcf3b9-9d11-47e0-a877-dab5fa00ffbd.png)

- **Even with the additional resiliency that availability zones provide, it’s possible that an event could be so large that it impacts multiple availability zones in a single region. To provide even further resilience, Azure has Region Pairs.**
  - Most Azure regions are paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away.
  - Examples of region pairs in Azure are West US paired with East US and South-East Asia paired with East Asia. Because the pair of regions are directly connected and far enough apart to be isolated from regional disasters, you can use them to provide reliable services and data redundancy.
  - Most regions are paired in two directions, meaning they are the backup for the region that provides a backup for them (West US and East US back each other up). However, some regions, such as West India and Brazil South, are paired in only one direction. In a one-direction pairing, the Primary region does not provide backup for its secondary region.
  - Brazil South is unique because it's paired with a region outside of its geography. Brazil South's secondary region is South Central US. The secondary region of South Central US isn't Brazil South.
  
![image](https://user-images.githubusercontent.com/74251229/194741584-0c2ea227-9223-46ac-bf0e-4cb380070c6d.png)

- **In addition to regular regions, Azure also has sovereign regions. Sovereign regions are instances of Azure that are isolated from the main instance of Azure. You may need to use a sovereign region for compliance or legal purposes.**
  - Azure sovereign regions include:
    - US DoD Central, US Gov Virginia, US Gov Iowa and more: These regions are physical and logical network-isolated instances of Azure for U.S. government agencies and partners. These datacenters are operated by screened U.S. personnel and include additional compliance certifications.
    - China East, China North, and more: These regions are available through a unique partnership between Microsoft and 21Vianet, whereby Microsoft doesn't directly maintain the datacenters.
