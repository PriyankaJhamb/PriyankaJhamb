
## Microsoft Azure Fundamentals
- Microsoft Azure is a cloud computing platform. 
- It is a consumption-based model. (works on operational expenditure rather than on capital expenditure).
#### This consumption-based model has many benefits, including:
1. No upfront(paid in advance) costs.
2. No need to purchase and manage costly infrastructure that users might not use to its fullest potential.
3. The ability to pay for more resources when they're needed.
4. The ability to stop paying for resources that are no longer needed.

#### Temporary Azure portal environment called the sandbox.

#### The main two services are provided by the cloud service provider:)
1. Compute Power
2. Storage
3. Application
4. Platform
5. Messaging

### Ideally without the use of cloud computing, all responsibilities need to be complete by the company which includes managing physical softwares, physical storage, power, cooling, security and network connectivity.
### Shared Responsibility Model between Customer and the cloud service provider.
![image](https://user-images.githubusercontent.com/74251229/193389481-9d00fe1b-b855-4eb2-b3e4-3eb6812f8122.png)

### Types of Cloud Deployment Models
#### 1. Public Cloud:
- open to all to store and access information via internet,
- pay as per use(for the services),
- managed by the third parties(cloud service provider)

##### Fundamental Characteristic of public cloud is Multitenancy.(Multi-tenancy is an architecture in which a single instance of a software application serves multiple customers.)
Examples: Google App Engine, Dropbox etc.
![image](https://user-images.githubusercontent.com/74251229/193392848-79592080-7836-4a85-b421-a99268433c43.png)

##### Advantages:
1. Cost effective (pay as per scale)
2. High scalability 
3. Feasibility: Location independent because its services are delivered through the internet.
4. Time efficient: Maintained by cloud service provider.

##### Disadvantages
1. Less secure because resources are shared publically.
2. Less customizable as compared to private cloud.
3. Less Data Privacy.
4. Less reliability.
#### 2. Private Cloud (Internal/ Corporate Cloud)
- services accessible within a  organisation i.e it belongs to a specific organisation.
- can be managed by organisation, 3rd party also.

![image](https://user-images.githubusercontent.com/74251229/193393184-9bdff749-4c0c-425c-824b-692f6eb8449a.png)

##### Advantages:
1. Less feasibility: It is accessible within an organisation, so the area of operations is limited.
3. High security
3. Data Privacy
4. More customizable.
5. Improved reliability.

##### Disadvantages:
1. High Cost
2. Limited Scalability
3. Time used more.

#### 3. Hybrid Cloud
- features of public and private cloud
- critical activities performed by private cloud and non critical activites by public cloud.

##### Advantages:
1. Low cost as compare to private coud/
2. Scalability
3. Flexibility
4. Security

##### Disadvantages:
1. Managing is difficult/complex because there are more than 1 type of deployment model.
2. Maintainence: dependency on infrastructure 

#### 4. Community Cloud
- allows services to be accessible by a group of several organisations to share the information between the organisation & a specific community.
- owned, managed & operated by 1 or more organisations in the community or 3rd party.

![image](https://user-images.githubusercontent.com/74251229/193393245-c401d2b4-14e3-4277-99b1-7540693518e6.png)

##### Advantages:
1. Cost reduction/ Cost effective: It is cheaper than private cloud. Mutlitple companies share the bill, which lowers the cost.
2. sharing among the companies (like resources).
3. More secure than public cloud but less than private cloud.
##### Disadvantages:
1. consistent maintainence cost
2. Increased cost as compare to public loud.

### Multi-Cloud

- In which 2 or more cloud environments are involved. 
- It may possible that you are using one service and you want to migrate to other service provider.

### Azure Arc
- set of technologies that help to manage any type of cloud environment(it can be public, private or hybrid).

### Azure VMware Solution
It helps to run VMware workloads, that is previously in private cloud environment, in Azure.


### Benefits of Cloud
1. Scalability (ability to handle demand):
- Vertical Scaling: power/capabilities of resources can be scaled up (either automatically or manually) or scaled down as per requirement. e.g adding more CPU/RAM to the virtual machine or lowering the CPU/RAM specifications. 
- Horizontal Scaling: number of resources/ virtual machines/ containers can be scaled out (increase) or scaled in (decrease). 

2. Availability (High Uptime):
- available (Uptime)
- Not availbale (Downtime)


It is not possible to have 100 percent uptime because when we experienced a steep jump in demand, we need to use back up servers but we need to integrate which takes time atleast 1 minute. but we can have 99.9 percent.

For each service, there is a service level agreement which can be different for each service provided by a cloud service provider.


3. Reliability (ability to recover from failurs and continue to function):
Using decentralised design, the cloud naturaly supports a reliable and resilent infrastructure. With the global scale, event if one region has a catastrophic event other regions are still up and running.

4. Predictability (forecasting the performance and cost):
- Performance predictability focus on predicting the resources needed to deliver a positive experience to the customers. Autoscaling, load balancing and high availablity supports performance predictability. If you suddenly need more resources, autoscaling can deploy additional resources to meet the demand, and then scale back when the demand drops. Or if the traffic is heavily focused on one area, load balancing will help redirect some of the overload to less stressed areas.
- Cost predictability is focused on predicting the cost of the cloud spend. With the cloud, one can monitor, analyse trends and patterns of usage, predict future cost and adjust resources as needed. Also some tools can be used to get an estimate of potential cloud spend e.g pricing calculator and total cost of ownership (TCO).

5. Security: 
- Cloud providers are typically well suited to handle things like distributed denial of service attacks etc.
- It depends upon the security need that matches with the cloud solution. If a person wants more control on security, he can go with the infrastructure as a service and if he wants patches and maintenance taken care of automatically, platform as a service may be the best cloud strategies for him.

6. Governance: 
Cloud service providers provides the software updates to meet corporate standards and government regulatory requirements time to time. Cloud-based auditing helps flag any resource that's out of compliance with your corporate standards and provides mitigation strategies.

7. Manageability:
Two types of manageability for cloud computing are:
  1. Management of the cloud (managing cloud resources)
  - Automatically scale resource deployment based on need.
  - Deploy resources based on a preconfigured template, removing the need for manual configuration.
  - Monitor the health of resources and automatically replace failing resources.
  - Receive automatic alerts based on configured metrics, so you’re aware of performance in real time.
  2. Management in the cloud (managing the cloud environment) 
  - through a web portal.
  - using a command line interface
  - using APIs.
  - using powershell



