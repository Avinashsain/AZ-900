# AZ-900 Practice Test D — Results (Attempt 1)

---

### Question 1 — *Describe cloud computing*
**Fill in the blank: Cloud computing is a model of delivering IT services such as computing, networking and storage over the Internet on a _____________ basis.**

long-term contract | case-by-case | ✅ **pay-as-you-go** | pay up-front as a capital expense

**Explanation:** Pay-as-you-go allows users to pay for the resources they consume on a flexible, as-needed basis, without long-term commitments or upfront expenses.

---

### Question 2 — *Describe cloud computing*
**What is the primary difference between pay-as-you-go and reserved instance pricing models in the cloud?**

- Reserved instances offer higher performance than pay-as-you-go instances. *(Incorrect — not about performance.)*
- Pay-as-you-go requires upfront payment, while reserved instances are billed hourly. *(Incorrect — reversed.)*
- Pay-as-you-go is only available for public cloud models, while reserved instances are for private cloud models. *(Incorrect.)*
- ✅ **Reserved instances offer discounted rates for long-term commitments, while pay-as-you-go is billed based on usage.**

---

### Question 3 — *Describe cloud computing*
**According to the shared responsibility model, who is responsible for keeping the guest operating system (Windows or Linux) updated on an Azure Virtual Machine?**

- It's automatically taken care of, and no one needs to do anything. *(Incorrect.)*
- The cloud provider, in this case Microsoft Azure. *(Incorrect — Azure manages underlying infrastructure, not the guest OS.)*
- ✅ **The customer, such as you**

---

### Question 4 — *Describe Azure compute and networking services*
**What is the benefit of using Azure Virtual Desktop compared to traditional on-premises desktop virtualization solutions?**

Lower costs | ✅ **All answers are correct** | Increased security | Improved scalability

**Explanation:** Azure Virtual Desktop provides a combination of lower costs, increased security, and improved scalability compared to traditional on-premises solutions.

---

### Question 5 — *Describe cloud service types* (❌ Incorrect)
**Which of the following is NOT a characteristic of Infrastructure as a Service (IaaS)?**

- Hardware virtualization *(this IS a characteristic of IaaS)*
- ✅ **Managed operating system** *(correct answer — in IaaS, the customer manages the OS, not the provider)*
- Pay-as-you-go pricing *(this IS a characteristic of IaaS)*
- On-demand provisioning *(this IS a characteristic of IaaS)*

> Your answer: Pay-as-you-go pricing (incorrect)

---

### Question 6 — *Describe Azure identity, access, and security*
**What is the primary purpose of Azure RBAC?**

- To manage network security groups. *(Incorrect.)*
- ✅ **To grant users the appropriate level of access to Azure resources.**
- To protect against unauthorized access to Azure subscriptions. *(Partially true, but not the primary purpose.)*
- To enforce multi-factor authentication. *(Incorrect.)*

---

### Question 7 — *Describe the core architectural components of Azure* (❌ Incorrect)
**Fill in the blank: A _________ is a geographical area on the planet that contains at least one, but potentially multiple datacenters that are nearby and networked together with a low-latency network.**

- data center *(Incorrect — too narrow.)*
- availability zone *(Incorrect — a unique physical location within a region.)*
- edge network *(Incorrect.)*
- ✅ **region** *(correct answer)*

> Your answer: availability zone (incorrect)

---

### Question 8 — *Describe the benefits of using cloud services*
**Fill in the blank: __________ refers to the policies, processes, and controls that organizations implement to ensure that their cloud computing initiatives align with their overall business objectives and risk management strategies.**

✅ **Governance** | Manageability | Reliability | Security

---

### Question 9 — *Describe cloud computing*
**What is a key benefit of the consumption-based model in cloud computing?**

Long-term contracts | Upfront hardware purchases | ✅ **Pay-as-you-go pricing** | Fixed monthly costs

---

### Question 10 — *Describe the core architectural components of Azure*
**Which of the following is a benefit of using sovereign regions in Azure?**

✅ **Reduced compliance risks** | Increased performance | Greater flexibility | Lower costs

**Explanation:** Sovereign regions are designed to meet specific regulatory and compliance requirements of certain industries or regions.

---

### Question 11 — *Describe Azure storage services*
**Which Azure Storage access tier is optimized (including for cost) for data accessed infrequently and must be stored for at least 30 days?**

Premium storage | Hot access tier | ✅ **Cool access tier** | Archive access tier

---

### Question 12 — *Describe Azure storage services*
**Which storage option should you choose if you need the absolute highest performance (regardless of the cost) for intense workloads like SAP HANA or transaction-heavy applications?**

✅ **Ultra Disks** | Premium SSDs | Standard HDDs | Standard SSDs

---

### Question 13 — *Describe the core architectural components of Azure* (❌ Incorrect)
**What entities can management groups contain?** *(multi-select)*

- ✅ Subscriptions *(your selection — correct)*
- ❌ Resources *(your selection — incorrect; resources live in resource groups/subscriptions, not directly in management groups)*
- ✅ **Management groups** *(correct answer you missed — management groups can be nested inside each other)*
- Resource groups *(incorrect — not directly contained within management groups)*

**Explanation:** Management groups can contain subscriptions and other (nested) management groups, forming a governance hierarchy. They do **not** directly contain resources or resource groups.

---

### Question 14 — *Describe Azure identity, access, and security*
**What is the primary purpose of Microsoft Entra ID?**

- To provide on-premises domain services in the cloud. *(Incorrect.)*
- To secure network traffic and protect against cyber threats. *(Incorrect.)*
- ✅ **To manage user identities and access to applications and resources.**
- To store and manage large amounts of data. *(Incorrect.)*

---

### Question 15 — *Describe the benefits of using cloud services*
**What is the primary benefit of high availability in cloud computing?**

Reduces scalability | Increases cost | ✅ **Minimizes downtime and ensures continuous service** | Requires manual intervention

---

### Question 16 — *Describe Azure identity, access, and security*
**Which of the following is a key principle of the Zero Trust security model?**

- Rely solely on network firewalls to secure resources. *(Incorrect.)*
- Trust all users and devices by default once they are inside the network perimeter. *(Incorrect — opposite of Zero Trust.)*
- Allow unrestricted access to resources for all authenticated users. *(Incorrect.)*
- ✅ **Verify explicitly and enforce least-privilege access for all users and devices.**

---

### Question 17 — *Describe Azure identity, access, and security*
**What is the primary benefit of using Microsoft Entra Conditional Access?**

- Reduced reliance on passwords. *(Incorrect — not the primary benefit.)*
- Simplified user authentication. *(Incorrect.)*
- ✅ **Enhanced security by limiting access to authorized users and devices.**
- Improved user experience. *(Incorrect.)*

---

### Question 18 — *Describe the core architectural components of Azure*
**What is the minimum number of Availability Zones required to create a highly available application in Azure?**

3 | 1 | 4 | ✅ **2**

---

### Question 19 — *Describe the benefits of using cloud services*
**What type of scaling typically involves moving from a smaller machine to a larger (more powerful) machine?**

✅ **Vertical scaling** | Scaling out | Horizontal scaling

**Explanation:** Vertical scaling ("scaling up") increases the capacity of a single machine (more CPU, memory, storage). Horizontal scaling/"scaling out" adds more machines instead.

---

### Question 20 — *Describe Azure compute and networking services*
**What is the primary purpose of an availability set in Azure?**

- To ensure data redundancy and durability. *(Incorrect — not the primary purpose.)*
- To group virtual machines for easier management. *(Incorrect — not the primary purpose.)*
- To provide load balancing for web applications. *(Incorrect.)*
- ✅ **To protect against single points of failure.**

---

### Question 21 — *Describe the benefits of using cloud services*
**Which of the following best describes the benefit of elasticity in cloud services like Microsoft Azure?**

- ✅ **The ability to automatically scale resources up or down based on demand.**
- The guarantee of 100% uptime for all services. *(Incorrect.)*
- The elimination of all operational costs for managing resources. *(Incorrect.)*
- The requirement to pre-purchase resources for future use. *(Incorrect.)*

---

### Question 22 — *Describe cloud computing*
**What is the key characteristic of serverless computing that distinguishes it from traditional infrastructure?**

Fixed pricing structure | Requires manual server management | ✅ **Automatic scaling based on demand** | Limited scalability options

---

### Question 23 — *Describe the core architectural components of Azure*
**Which of the following statements about Azure resource groups is true?**

- ✅ **A resource group can contain resources from multiple Azure regions.**
- Deleting a resource group will not delete the resources contained within it. *(Incorrect — deleting a resource group deletes its resources too.)*
- A resource group can contain resources from multiple Azure subscriptions. *(Incorrect — a resource group is tied to a single subscription.)*
- A resource group can only contain one type of resource. *(Incorrect — it can hold a mix of resource types.)*

---

### Question 24 — *Describe the benefits of using cloud services*
**What is the primary advantage of using Azure's built-in security features compared to managing security on-premises?**

Decreased flexibility | Increased complexity | ✅ **Reduced expertise required** | Lower costs

---

### Question 25 — *Describe cost management in Azure*
**How does data transfer between Azure regions impact costs?**

✅ **It's charged based on the amount of data transferred and the distance** | It's charged based on the destination region only | It's charged based on the source region only | It's always free, regardless of the distance

---

### Question 26 — *Describe the benefits of using cloud services*
**Which of the following is NOT a core component of Azure's reliability strategy?**

Availability | ✅ **Performance** *(correct answer — not a core reliability component)* | Fault tolerance | Redundancy

---

### Question 27 — *Describe Azure storage services*
**Which tool lets you centralize your file shares in Azure Files and keep the flexibility, performance, and compatibility of a Windows file server?**

AzCopy | ✅ **Azure File Sync** | Azure Storage Explorer

---

### Question 28 — *Describe Azure storage services* (❌ Incorrect)
**In which storage redundancy option does Azure give you a secondary endpoint for read-only access?**

ZRS *(Incorrect — no secondary read endpoint.)* | ✅ **RA-GRS** *(correct answer — provides read-access to a secondary region)* | LRS *(Incorrect.)* | GRS *(Incorrect — replicates to secondary region but doesn't grant read access to it.)*

> Your answer: LRS (incorrect)

---

### Question 29 — *Describe the core architectural components of Azure*
**What is the primary purpose of an Azure resource group?**

- To provide a logical container for Azure subscriptions. *(Incorrect.)*
- ✅ **To group related Azure resources together for management and deployment.**
- To manage user accounts and access control. *(Incorrect.)*
- To act as a central hub or dashboard for all Azure services. *(Incorrect.)*

---

### Question 30 — *Describe cloud computing*
**A small startup with limited IT resources and a need for flexible scalability would be best suited for which cloud model?**

Hybrid Cloud | Community Cloud | ✅ **Public Cloud** | Private Cloud

---

### Question 31 — *Describe cloud service types*
**What is the primary benefit of using PaaS compared to IaaS?**

Increased control over the infrastructure | Greater flexibility | ✅ **Reduced development time** | Lower costs

---

### Question 32 — *Describe Azure compute and networking services*
**What is the primary purpose of a virtual machine scale set in Azure?**

✅ **To automatically scale virtual machines based on demand** | To provide load balancing for web applications | To group virtual machines for easier management | To ensure data redundancy and durability

---

### Question 33 — *Describe Azure compute and networking services*
**Which Azure App Service hosting option would you choose if you wanted isolated hardware and network, ensuring they are not used by any other Azure customers?**

✅ **App Service Environment** | Bare Metal Hosting | Virtual Machine | App Service Plan

---

### Question 34 — *Describe Azure compute and networking services*
**Which Azure service can be used to deploy and scale serverless containerized applications?**

Azure Functions | ✅ **Azure Container Instances** | Azure App Service | Azure Kubernetes Service (AKS)

---

### Question 35 — *Describe cloud computing*
**Which of the following qualities is unique to Private Cloud?**

- Anyone can sign up using a credit card. *(Incorrect — that's Public Cloud.)*
- ✅ **A cloud infrastructure dedicated to a single organization, managed either by the organization itself or by a third-party provider.**
- An application that uses a network security group, firewall, DDoS protection, and other network security methods. *(Incorrect — not unique to Private Cloud.)*
- The virtual network is not accessible from the public Internet. *(Incorrect — describes an isolated VNet, not Private Cloud specifically.)*

---

### Question 36 — *Describe Azure identity, access, and security*
**Which of the following is a passwordless authentication method supported by Azure?**

✅ **Biometric authentication and security keys** | Only biometric authentication (e.g., fingerprint, facial recognition) | Four-digit PIN | Only security keys

---

### Question 37 — *Describe Azure storage services*
**Which feature of Azure Storage makes it durable?**

✅ **Redundancy** | Security | Accessibility | Scalability

---

### Question 38 — *Describe the benefits of using cloud services* (❌ Incorrect)
**Which of the following is NOT a key aspect of predictability in Azure?**

Cost optimization *(this IS a key aspect)* | ✅ **Fault tolerance** *(correct answer — this relates to reliability, not predictability)* | Consistent performance *(this IS a key aspect)* | Scalability *(this IS a key aspect)*

> Your answer: Consistent performance (incorrect)

---

### Question 39 — *Describe Azure identity, access, and security*
**Which of the following is a key difference between Azure B2B and Azure B2C?**

- B2B is for cloud-based applications, while B2C is for on-premises applications. *(Incorrect.)*
- B2B is for internal users, while B2C is for external users. *(Incorrect.)*
- There is no significant difference between the two services. *(Incorrect.)*
- ✅ **B2B is for business-to-business collaboration, while B2C is for business-to-customer interactions.**

---

### Question 40 — *Describe cost management in Azure*
**What is the primary purpose of tags in Azure?**

To monitor resource performance | To automate resource provisioning | ✅ **To categorize and organize resources for better management** | To assign security permissions to resources

---

### Question 41 — *Describe the core architectural components of Azure*
**Why are Azure datacenters located in various regions around the world?**

To reduce latency for users | To comply with local regulations | To ensure redundancy and high availability | ✅ **All answers are correct**

---

### Question 42 — *Describe Azure storage services*
**Fill in the blank: __________ stores data offline and offers the lowest storage costs.**

Cold access | Hot access | Cool access | ✅ **Archive storage**

---

### Question 43 — *Describe cloud service types*
**Which of the following is the most likely scenario in which to choose Infrastructure as a Service (IaaS) options in cloud computing?**

Someone looking to run an app for free in the cloud | Someone looking to reduce administrative overhead | Brand new development | ✅ **Lift-and-shift migration**

---

### Question 44 — *Describe tools in Azure for governance and compliance* (❌ Incorrect)
**Which of the following is NOT a core capability of Microsoft Purview?**

Data loss prevention *(this IS a core capability)* | ✅ **Data migration and integration** *(correct answer — handled by Azure Data Factory/Data Share, not Purview)* | Data discovery and classification *(this IS a core capability)* | Data sensitivity labeling *(this IS a core capability)*

> Your answer: Data loss prevention (incorrect)

---

### Question 45 — *Describe Azure compute and networking services* (❌ Incorrect)
**Which of the following benefits are provided by Azure ExpressRoute compared to a regular Site-to-Site VPN?** *(multi-select)*

- ❌ Access to private Virtual Networks that do not have devices with a public IP address *(your selection — incorrect; both ExpressRoute and VPN can provide this depending on settings)*
- Less expensive connection to Azure *(incorrect — ExpressRoute is typically more expensive)*
- ✅ **Data travels over a private network, not a public one** *(your selection — correct)*
- ✅ **Faster connection to Azure** *(your selection — correct)*

---

### Question 46 — *Describe Azure compute and networking services*
**Which compute type offers the greatest flexibility and control over the underlying hardware, allowing you to customize the environment to your specific needs?**

Function | Serverless | ✅ **Virtual Machine** | Container

---

### Question 47 — *Describe Azure compute and networking services* (❌ Incorrect)
**You have a virtual machine that you need to have a public endpoint - accessible from the Internet. Which of the following resources do you need to have in order to achieve your goal?**

Azure Firewall *(Incorrect — not required for this.)* | IIS web server *(Incorrect — not required for network accessibility.)* | VPN Gateway *(Incorrect — used for private connections, not public exposure.)* | ✅ **Public IP Address** *(correct answer)*

> Your answer: VPN Gateway (incorrect)

---

### Question 48 — *Describe Azure compute and networking services*
**Fill in the blank: __________ is a mechanism that allows you to connect two virtual networks within Azure.**

Azure Application Gateway | Azure ExpressRoute | ✅ **Azure peering** | Azure Load Balancer

---

### Question 49 — *Describe Azure storage services*
**What is AzCopy primarily used for in Azure?**

Managing user identities and access permissions | Monitoring the performance of Azure resources | Automating the deployment of virtual machines | ✅ **Copying data to and from Azure Storage efficiently.**

---

### Question 50 — *Describe the benefits of using cloud services*
**Which of the following best describes scalability in the cloud?**

The ability to maintain security across regions | ✅ **The ability to increase or decrease resources based on demand** | The ability to reduce costs by limiting storage | The ability to run applications without an internet connection

---

## Summary of Missed Questions
| # | Topic | Correct Answer |
|---|-------|-----------------|
| 5 | IaaS characteristics | Managed operating system (is NOT a characteristic) |
| 7 | Region definition | Region |
| 13 | Management group contents | Subscriptions + Management groups |
| 28 | Storage redundancy w/ read endpoint | RA-GRS |
| 38 | Predictability aspects | Fault tolerance (is NOT a key aspect of predictability) |
| 44 | Microsoft Purview capabilities | Data migration and integration (is NOT a core capability) |
| 45 | ExpressRoute benefits | Private network + Faster connection (partial credit — missed one option) |
| 47 | Public endpoint requirement | Public IP Address |
