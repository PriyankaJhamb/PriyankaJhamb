
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

#### Management Infrastructure
- An Azure account is identity in a directory/Azure Active Directory which contains all the information regarding subscriptions by using a management group.

| ```Resources``` logically Grouped into ```Resource Groups``` logically Grouped into ```Subscriptions``` logically Grouped into ```Management Group``` |

Where Resources can be VM, Database etc, subscriptions are a unit of management, billing, and scale. 
- Resource Groups cannot be nested.
- When you apply an action to a resource group, that action will apply to all the resources within the resource group.

![image](https://user-images.githubusercontent.com/74251229/194743189-9925662c-732b-4c8e-b6ef-dd95fbbea2d4.png)
- There are two types of subscription boundaries that you can use:
  - Billing boundary: This subscription type determines how an Azure account is billed for using Azure. You can create multiple subscriptions for different types of billing requirements. Azure generates separate billing reports and invoices for each subscription so that you can organize and manage costs.
  - Access control boundary: Azure applies access-management policies at the subscription level, and you can create separate subscriptions to reflect different organizational structures. An example is that within a business, you have different departments to which you apply distinct Azure subscription policies. This billing model allows you to manage and control access to the resources that users provision with specific subscriptions.

![image](https://user-images.githubusercontent.com/74251229/194743201-78cab19e-9036-4672-b18c-74538bd0ae42.png)
- if you’re dealing with multiple applications, multiple development teams, in multiple geographies, then it will be difficult to organise the n number of subscriptions, so we can make management groups and also nested it when required.
- One can apply governance conditions to the management groups.
- All subscriptions within a management group automatically inherit the conditions applied to the management group, the same way that resource groups inherit settings from subscriptions and resources inherit from resource groups.
- Some examples of how you could use management groups might be:  Create a hierarchy that applies a policy, Provide user access to multiple subscriptions.
- Important facts about management groups:
  - 10,000 management groups can be supported in a single directory.
  - A management group tree can support up to six levels of depth. This limit doesn't include the root level or the subscription level.
  - Each management group and subscription can support only one parent.
![image](https://user-images.githubusercontent.com/74251229/194743219-e5ee79f8-1e1c-487f-ac9a-022c0ebc8233.png)

### Azure Virtual Machines
- like a Virtual Server, it provides infrastructure as a service.
- you can have full control on operating system
- You can configure the VM or you can use prconfigured image of configuration using the option.
- You can also do grouping of VMs to provide the high availability, scalability and redundancy.
- Azure manage Grouping of VMs with features 
  - Scale sets: help us to provide the service of grouping the virtual machines and configure it identically, provide load balancers to use VMs efficiently and also it automatically increase or decrease the number of VMs according to the demand or we can also defined the schedule when it needs to scale.
  - Availablity sets: Availability sets are designed to ensure that VMs stagger updates and have varied power and network connectivity, preventing you from losing all your VMs with a single network or power failure.
    - Update domain: The update domain groups VMs that can be rebooted at the same time. This allows you to apply updates while knowing that only one update domain grouping will be offline at a time. All of the machines in one update domain will be updated. An update group going through the update process is given a 30-minute time to recover before maintenance on the next update domain starts.
    - Fault domain: The fault domain groups your VMs by common power source and network switch. By default, an availability set will split your VMs across up to three fault domains. This helps protect against a physical power or networking failure by having VMs in different fault domains (thus being connected to different power and networking resources).
- Examples of when to use VMs:
  - **During testing and development.** VMs provide a quick and easy way to create different OS and application configurations. Test and development personnel can then easily delete the VMs when they no longer need them.
  - **When running applications in the cloud.**: need to handle fluctuations in demand. 
  - **When extending your datacenter to the cloud:** An organization can extend the capabilities of its own on-premises network by creating a virtual network in Azure and adding VMs to that virtual network.
  - **During disaster recovery:**  If a primary datacenter fails, you can create VMs running on Azure to run your critical applications and then shut them down when the primary datacenter becomes operational again.
  
### Move to the cloud with VMs
- move from a physical server to the cloud (also known as lift and shift). 
- You can create an image of the physical server and host it within a VM with little or no changes. 
- Just like a physical on-premises server, you must maintain the VM: you’re responsible for maintaining the installed OS and software.

### VM Resources
When you provision a VM, you’ll also have the chance to pick the resources that are associated with that VM, including:

- Size (purpose, number of processor cores, and amount of RAM)
- Storage disks (hard disk drives, solid state drives, etc.)
- Networking (virtual network, public IP address, and port configuration)

### Create an Azure Virtual Machine
In this exercise, you create an Azure virtual machine (VM) and install Nginx, a popular web server.

You could use the Azure portal, the Azure CLI, Azure PowerShell, or an Azure Resource Manager (ARM) template.

In this instance, you're going to use the Azure CLI.
 
 
 1. From Cloud Shell, run the following az vm create command to create a Linux VM:
 ```
 az vm create \
  --resource-group learn-a1739492-ec38-44f1-8089-74c46bc325a8 \
  --name my-vm \
  --image UbuntuLTS \
  --admin-username azureuser \
```
2. Run the following az vm extension set command to configure Nginx on your VM:
```
az vm extension set \
  --resource-group learn-a1739492-ec38-44f1-8089-74c46bc325a8 \
  --vm-name my-vm \
  --name customScript \
  --publisher Microsoft.Azure.Extensions \
  --version 2.1 \
  --settings '{"fileUris":["https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh"]}' \
  --protected-settings '{"commandToExecute": "./configure-nginx.sh"}'
```

## Azure Virtual Desktop: 
Azure Virtual Desktop is a desktop and application virtualization service that runs on the cloud. It enables you to use a cloud-hosted version of Windows from any location.




### Reference
- [https://www.pragimtech.com/courses/learn-azure-from-scratch/](https://www.pragimtech.com/courses/learn-azure-from-scratch/)
- [https://www.pragimtech.com/blog/azure/azure-availability-set/](https://www.pragimtech.com/blog/azure/azure-availability-set/)


