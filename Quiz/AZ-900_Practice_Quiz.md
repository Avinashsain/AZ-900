# AZ-900 Practice Quiz — Questions & Explanations

---

### Question 1
A company is deploying a business-critical application in Azure and needs to protect against datacenter-level failures within a single Azure region. The application requires 99.99% availability SLA. Which Azure feature should the company use to distribute their virtual machines across physically separate locations within the region?

- Deploy virtual machines across multiple resource groups
- **✅ Deploy virtual machines across availability zones**
- Deploy virtual machines in a single datacenter with multiple backup copies
- Deploy virtual machines across multiple Azure regions

**Explanation:** Availability zones are physically separate datacenters within an Azure region, each with independent power, cooling, and networking. Distributing VMs across availability zones protects against datacenter-level failures while keeping resources within the same region, enabling the 99.99% SLA for VMs deployed across two or more zones. Resource groups are only logical containers and provide no physical separation; multi-region deployment addresses region-level (not datacenter-level) failures and is more than necessary here.

---

### Question 2
Contoso Ltd. runs several business applications on physical servers in their on-premises datacenter. The company wants to modernize by migrating some applications to Azure while keeping others on-premises due to regulatory requirements, with seamless authentication across both environments. Which cloud deployment model does this describe?

- **✅ Hybrid cloud**
- Private cloud
- Public cloud
- Community cloud

**Explanation:** A hybrid cloud combines on-premises infrastructure with public cloud services, allowing data and applications to be shared between them. Contoso's mix of on-premises and Azure workloads with integrated authentication (e.g., via Microsoft Entra Connect) is a textbook hybrid cloud scenario.

---

### Question 3
The IT manager wants to be notified when Azure plans maintenance that might affect virtual machines, and wants to review root cause analysis when service interruptions occur. Which Azure service should you recommend?

- Azure Advisor
- Azure Monitor
- Microsoft Defender for Cloud
- **✅ Azure Service Health**

**Explanation:** Azure Service Health provides personalized alerts and guidance covering Service Issues (current problems), Planned Maintenance (upcoming events), and Health Advisories, along with detailed root cause analysis (RCA) reports after incidents resolve. Advisor gives optimization recommendations, Monitor tracks your own telemetry, and Defender for Cloud focuses on security — none provide platform maintenance/incident RCA reporting.

---

### Question 4
The company wants personalized recommendations to reduce costs, improve security, and optimize performance across all Azure resources based on actual usage and configuration. Which service should you use?

- Microsoft Defender for Cloud
- Azure Service Health
- Azure Monitor
- **✅ Azure Advisor**

**Explanation:** Azure Advisor is a free, personalized cloud consultant that analyzes resource configuration and usage telemetry to provide actionable recommendations across five pillars: Cost, Security, Reliability, Operational Excellence, and Performance.

---

### Question 5
A retail company's e-commerce application must remain available even if an Azure datacenter experiences an outage. Which Azure reliability benefit directly addresses this?

- **✅ Azure's ability to deploy resources across multiple availability zones within a region**
- Azure's support for automatic horizontal scaling to handle increased traffic loads
- Azure's compliance certifications that meet industry regulatory standards
- Azure's pay-as-you-go pricing model that reduces upfront infrastructure costs

**Explanation:** Availability zones are physically separate datacenters within a region, each with independent power, cooling, and networking — distributing resources across them ensures continued operation if one datacenter fails. Scaling addresses load, not failure; compliance and pricing relate to governance and cost, not resilience.

---

### Question 6
The IT director wants to understand how Azure's built-in security features reduce the company's security management burden compared to on-premises. Which benefit best addresses this?

- Azure requires customers to install and maintain their own security software on all virtual machines to ensure compliance.
- Azure eliminates all security responsibilities from the customer organization by handling all security aspects of the cloud environment.
- **✅ Azure provides security tools and features that are managed and updated by Microsoft, reducing the organization's responsibility for maintaining security infrastructure.**
- Azure provides security only for Microsoft-managed services and requires third-party solutions for customer-deployed resources.

**Explanation:** Under Azure's shared responsibility model, Microsoft manages security of the underlying cloud infrastructure (physical datacenters, networks, hosts) and provides built-in tools like Microsoft Defender for Cloud with continuous updates — significantly reducing the customer's infrastructure security burden compared to on-premises environments.

---

### Question 7
A company needs to store large amounts of unstructured data (images, videos, logs) that's accessed frequently for the first month, then rarely. They want to minimize storage costs while keeping data available. Which solution should they implement?

- Azure Table Storage with partitioning by upload date
- Azure Queue Storage with automatic archiving enabled
- **✅ Azure Blob Storage with a lifecycle management policy to move data to the Cool access tier after 30 days**
- Azure Files with Premium performance tier for the first month, then switch to Standard tier

**Explanation:** Azure Blob Storage is purpose-built for unstructured data at scale. Lifecycle management policies automatically transition blobs between Hot, Cool, and Archive tiers based on age/access patterns, matching this exact use case and optimizing cost.

---

### Question 8
You need User1 to be able to start and stop VMs in resource group RG-Production, but not delete them or modify configurations. What should you do?

- Assign User1 the Reader role on RG-Production.
- Assign User1 the Contributor role on RG-Production.
- **✅ Create and assign User1 a custom Azure RBAC role scoped to RG-Production that allows only the required VM start and stop actions**
- Assign User1 the Virtual Machine Contributor role on RG-Production.

**Explanation:** A custom RBAC role lets you grant only the exact permissions needed (start/stop) while excluding delete/modify actions, following least privilege. Reader can't perform management actions like start/stop; Contributor and Virtual Machine Contributor both grant far more permission (including delete and modify) than required.

---

### Question 9
A company needs to deploy a web application with multiple microservices that must scale independently, handling unpredictable traffic, while minimizing infrastructure management and supporting containerized deployment with dependencies. Which compute option best fits?

- Azure App Service with a single web app deployment
- Azure Virtual Machines with manual scaling configuration
- **✅ Azure Kubernetes Service (AKS) with auto-scaling enabled**
- Azure Container Instances with individual container deployment

**Explanation:** AKS is built for orchestrating containerized microservices, offering automatic scaling, self-healing, and service discovery as a managed service — allowing each microservice to scale independently with minimal overhead. App Service suits monolithic apps; VMs require heavy manual management; ACI lacks orchestration for interdependent services.

---

### Question 10
500 remote employees need Windows 11 desktops and Microsoft 365 apps, centrally managed, with minimal hardware requirements on employee devices. Which solution should the company implement?

- Azure Virtual Machines running Windows 11 with RDP access for each user
- Azure App Service with web-based application hosting
- **✅ Azure Virtual Desktop**
- Microsoft 365 Business Premium with local desktop installations

**Explanation:** Azure Virtual Desktop is purpose-built for delivering virtualized Windows desktops and apps with centralized management, security, and minimal client-side hardware needs, supporting Windows 11 multi-session and Microsoft 365 integration.

---

### Question 11
Users accessing cloud apps from outside the corporate network must perform MFA, while users on the corporate network can sign in with just username/password. Which feature should you implement?

- **✅ Microsoft Entra Conditional Access**
- Microsoft Entra Multi-Factor Authentication
- Microsoft Entra Privileged Identity Management
- Microsoft Entra ID Protection

**Explanation:** Conditional Access lets administrators create policies that apply controls (like requiring MFA) based on conditions such as network location, device state, or risk level — exactly matching this location-based requirement. MFA alone provides the mechanism but not the conditional logic; PIM manages privileged role access; ID Protection focuses on risk detection.

---

### Question 12
Currently the company pays fixed monthly costs regardless of usage. How does Azure's consumption-based model change their cost structure?

- The company will pay a fixed monthly subscription fee for Azure services, similar to their current datacenter costs.
- **✅ The company will pay only for the Azure resources they actually use, with costs varying based on consumption.**
- The company will pay the same total costs as their on-premises datacenter, but distributed across multiple Azure subscriptions.
- The company will pay upfront capital expenses for Azure infrastructure before they can deploy any resources.

**Explanation:** The consumption-based model shifts costs from fixed capital expenses (CapEx) to variable operational expenses (OpEx) that scale with actual usage, eliminating waste from paying for unused capacity.

---

### Question 13
A small application processes HTTP requests for a few seconds per request with sporadic traffic. The team wants minimal infrastructure management and to pay only for actual compute time. Which service should they recommend?

- Azure Container Instances
- **✅ Azure Functions**
- Azure Virtual Machines
- Azure App Service

**Explanation:** Azure Functions is serverless, automatically scales with demand, and charges only for actual execution time (gigabyte-seconds) — ideal for event-driven, sporadic workloads. ACI charges for allocated container time regardless of execution; VMs and App Service typically run (and charge) continuously.

---

### Question 14
Identical dev, test, and production environments (same VMs, storage accounts, virtual networks) must be deployed consistently with minimal manual configuration errors. Which feature should you recommend?

- Resource groups
- Azure Policy
- Azure Portal dashboard
- **✅ Azure Resource Manager (ARM) templates**

**Explanation:** ARM templates define infrastructure as code (JSON), enabling consistent, repeatable deployment of identical environments while minimizing human error. Resource groups just organize resources; Azure Policy enforces standards/compliance but doesn't deploy infrastructure; dashboards are for visualization only.

---

### Question 15
Management requires that all VMs must have specific tags (Department, CostCenter, Owner) applied before they can be created, across multiple subscriptions. Which governance feature should you implement?

- Resource locks
- Role-based access control (RBAC)
- Management groups
- **✅ Azure Policy**

**Explanation:** Azure Policy enforces rules and effects over resources, including requiring specific tags before deployment, and can deny non-compliant resource creation. Locks prevent deletion/modification of existing resources; RBAC manages permissions, not configuration requirements; management groups organize subscriptions but don't directly enforce tagging (Azure Policy does, even when applied at that scope).

---

### Question 16
Resources in production resource group RG-Prod must be protected from accidental deletion, while administrators must still be able to modify configurations. What should you implement?

- Apply a Read-only lock on the RG-Prod resource group
- Remove Contributor permissions and assign Reader permissions to all administrators
- **✅ Apply a Delete lock on the RG-Prod resource group**
- Enable Microsoft Defender for Cloud on the RG-Prod resource group

**Explanation:** A Delete lock prevents deletion while still allowing read and modify operations — meeting both requirements. A Read-only lock would block modifications too; removing Contributor access would block modifications entirely; Defender for Cloud addresses security posture, not deletion protection.

---

### Question 17
Branch offices want centralized file storage in Azure Files while ensuring fast local file access even with slow internet connections. Which service should the company implement?

- Azure Blob Storage with Content Delivery Network (CDN)
- Azure NetApp Files
- **✅ Azure File Sync**
- Azure Files with geo-replication

**Explanation:** Azure File Sync centralizes storage in Azure Files while caching frequently accessed files locally on Windows Servers at each branch, with bidirectional synchronization — solving both centralization and local performance needs. Blob+CDN is for web content delivery, not SMB file shares; NetApp Files doesn't cache locally; geo-replication addresses redundancy, not local latency.

---

### Question 18
A business-critical application must survive an entire Azure datacenter failure but not a regional disaster, while minimizing cost. Which storage redundancy option should you recommend?

- Geo-redundant storage (GRS)
- **✅ Zone-redundant storage (ZRS)**
- Geo-zone-redundant storage (GZRS)
- Locally redundant storage (LRS)

**Explanation:** ZRS synchronously replicates data across three availability zones within a region, surviving a datacenter failure without the added cost of geo-replication to another region. LRS only protects against drive/rack failure (not a full datacenter); GRS and GZRS add unnecessary, costlier regional protection.

---

### Question 19
A mobile app needs to let customers create accounts and sign in with social media credentials (Facebook, Google, email) without corporate credentials. Which service should the company implement?

- Microsoft Entra ID B2B (Business-to-Business)
- **✅ Microsoft Entra ID B2C (Business-to-Consumer)**
- Microsoft Entra Domain Services
- Microsoft Entra ID (standard tenant)

**Explanation:** Microsoft Entra ID B2C is purpose-built for consumer-facing apps, supporting sign-up/sign-in via social, enterprise, or local identities without requiring corporate credentials. B2B is for partner/business collaboration; Domain Services provides legacy domain services; standard Entra ID targets organizational/employee users.

---

### Question 20
A development team wants to deploy web application code directly, without managing VMs, OS, or hardware. Which service model best meets this?

- **✅ Platform as a Service (PaaS) using Azure App Service**
- Software as a Service (SaaS) using Microsoft 365
- Infrastructure as a Service (IaaS) using Azure Virtual Machine Scale Sets
- Infrastructure as a Service (IaaS) using Azure Virtual Machines

**Explanation:** Azure App Service (PaaS) lets developers deploy code directly while the platform manages infrastructure, OS, scaling, and patching. SaaS (Microsoft 365) offers no custom code deployment; both IaaS options (VMs, Scale Sets) require the team to manage OS/infrastructure.

---

### Question 21
A company has resources on-premises, in AWS, and in Azure, and wants unified management, policy application, and visibility via a single control plane. Which service should the company implement?

- **✅ Azure Arc**
- Azure Monitor
- Azure Resource Manager
- Microsoft Defender for Cloud

**Explanation:** Azure Arc extends Azure's management capabilities — including policies and tooling — to resources outside Azure, including on-premises servers and other clouds like AWS, by projecting them into Azure Resource Manager. Monitor collects telemetry but doesn't provide a governance control plane; ARM natively manages only Azure resources; Defender for Cloud focuses on security, not general management.

---

### Question 22
The IT manager wants automatic email notification whenever CPU usage on any VM exceeds 85% for more than 5 minutes. Which Azure Monitor capability should you configure?

- Log Analytics workspace query
- **✅ Azure Monitor alert rule**
- Application Insights availability test
- Azure Monitor metrics chart

**Explanation:** Alert rules define conditions (like a CPU threshold over time) and trigger action groups (e.g., email notifications) when met. Log Analytics is for querying data; Application Insights availability tests check endpoint responsiveness; metrics charts are visualization tools without automated notification.

---

### Question 23
15 identical VMs must be deployed across three Azure regions with configuration consistency and simplified deployment. Which ARM capability is most appropriate?

- Use Azure Resource Manager locks to prevent changes to the virtual machines after deployment
- **✅ Use Azure Resource Manager templates to define the infrastructure and deploy it consistently across all regions**
- Use Azure Resource Manager resource groups to organize the virtual machines by region
- Use Azure Resource Manager role-based access control (RBAC) to manage permissions for the virtual machines

**Explanation:** ARM templates (infrastructure as code) let you define and repeatedly deploy identical, consistent configurations across regions, reducing errors through automation. Locks protect existing resources post-deployment; resource groups only organize; RBAC manages access, not deployment consistency.

---

### Question 24
The security team needs continuous security posture assessment, recommendations, and threat alerts across VMs, storage accounts, and SQL databases. Which service should they implement?

- Azure Policy
- Microsoft Entra ID Protection
- **✅ Microsoft Defender for Cloud**
- Azure Monitor

**Explanation:** Microsoft Defender for Cloud continuously assesses security posture (via secure score), provides actionable recommendations, and detects threats across hybrid cloud workloads — covering all stated requirements. Azure Policy handles compliance/governance, not threat detection; ID Protection covers identity risk only; Azure Monitor focuses on operational telemetry, not security-specific analysis.

---

### Question 25
The compliance team needs to discover sensitive personal information, classify data by regulatory requirements, and track access across Azure SQL Database, Storage accounts, and Data Lake Storage. Which service should you recommend?

- Microsoft Entra ID
- **✅ Microsoft Purview**
- Azure Policy
- Microsoft Defender for Cloud

**Explanation:** Microsoft Purview is a unified data governance service providing data discovery, classification, and lineage tracking across an organization's data estate, directly meeting these compliance requirements. Entra ID manages identity, not data governance; Azure Policy enforces resource configuration; Defender for Cloud focuses on security posture, not data classification.

---

### Question 26
The manager wants to quickly find and deploy an Azure VM using a graphical interface from any web browser, without command-line tools or extra software. Which tool should you demonstrate?

- Azure PowerShell
- Azure Mobile App
- Azure CLI
- **✅ Azure Portal**

**Explanation:** The Azure Portal is a web-based GUI accessible from any browser with no installation required, offering step-by-step wizards for deploying resources like VMs. PowerShell and CLI are command/script-based; the Mobile App has limited functionality for full deployment workflows.

---

### Question 27
The team currently deploys resources manually via the portal. Leadership wants improved consistency, fewer errors, and version-controlled infrastructure. Which approach should the team implement?

- Create detailed documentation with step-by-step screenshots of the portal deployment process
- Assign multiple administrators to review each manual deployment before execution
- Schedule regular backups of all Azure resources using Azure Backup
- **✅ Use Azure Resource Manager (ARM) templates to define and deploy infrastructure**

**Explanation:** ARM templates implement Infrastructure as Code (IaC), letting infrastructure be defined in version-controllable JSON files and deployed consistently and repeatably — directly solving consistency, error reduction, and version control needs. Documentation and extra reviewers don't eliminate manual error-prone processes; Azure Backup addresses recovery, not deployment consistency.

---

### Question 28
A development environment is used only 9 AM–5 PM, Monday–Friday; production must run continuously. Which pricing model gives the greatest cost savings for the development environment?

- Azure Hybrid Benefit to use existing on-premises licenses for the development virtual machines
- Reserved Instances with a one-year commitment for the development virtual machines
- **✅ Pay-as-you-go pricing with automated shutdown and startup schedules for the development virtual machines**
- Reserved Instances with a three-year commitment for the development virtual machines

**Explanation:** Pay-as-you-go with automated shutdown/startup schedules means paying only for the ~40 hours/week actually used (about 24% of total hours), eliminating charges for the rest of the week. Reserved Instances require paying for continuous 24/7 availability, wasting money on an intermittent workload; Hybrid Benefit only reduces licensing costs, not compute costs for idle time.

---

### Question 29
A company pays fixed costs for hardware, cooling, and maintenance regardless of usage, with servers often idle during off-peak hours. Which cloud characteristic most directly addresses paying for unused capacity?

- Geo-distribution
- **✅ Pay-as-you-go pricing**
- Disaster recovery
- High availability

**Explanation:** Pay-as-you-go (consumption-based) pricing lets organizations pay only for resources actually consumed, directly addressing the problem of fixed costs for idle infrastructure. Geo-distribution, disaster recovery, and high availability address performance/resilience concerns, not idle-capacity cost.

---

### Question 30
A web application must be accessible to users worldwide over the internet without a VPN or private network configuration. Which cloud deployment model best describes this?

- Community cloud
- Hybrid cloud
- Private cloud
- **✅ Public cloud**

**Explanation:** Public cloud resources are owned/operated by a third-party provider and delivered over the public internet, making them globally accessible via standard internet protocols without VPN. Private cloud typically requires special network access (VPN/dedicated connection); hybrid emphasizes integration of private and public components; community cloud is shared among organizations with common concerns, not a general public-access model.

---

### Question 31
A US government agency needs Azure services with physical/logical isolation of data within the US, screened US personnel, and FedRAMP High compliance. Which deployment option should the agency select?

- Deploy resources in Azure China regions operated by 21Vianet
- Deploy resources in Azure public cloud regions located in the United States (such as East US or West US)
- **✅ Deploy resources in Azure Government**
- Deploy resources using Azure Arc on the agency's on-premises infrastructure

**Explanation:** Azure Government is a sovereign cloud built specifically for US government agencies, offering physical/logical isolation from the public cloud, screened US personnel, dedicated US datacenters, and built-in FedRAMP High compliance. Azure China serves Chinese regulatory needs (wrong jurisdiction); public US regions lack the specialized isolation/personnel/compliance framework; Azure Arc extends management to on-premises infrastructure but doesn't itself provide sovereign cloud compliance.

---

### Question 32
A mobile app processes image uploads with unpredictable spikes, and the company wants to pay only for compute resources when images are actually being processed. Which compute solution best meets this?

- Azure Container Instances running continuously
- Azure Virtual Machines with auto-scaling enabled
- **✅ Azure Functions with a consumption plan**
- Azure App Service with an Always On feature

**Explanation:** Azure Functions with a consumption plan automatically scales with demand and charges only for actual execution time and resources consumed — no charges when idle. Continuously running ACI and Always-On App Service both incur charges regardless of activity; VMs with auto-scaling still require a minimum running instance count and incur cost during low usage.

---

### Question 33
The IT director wants to compare current on-premises costs (50 physical servers) with equivalent Azure services over a 5-year period. Which tool should be used?

- Azure Advisor
- Total Cost of Ownership (TCO) Calculator *(Note: retired as of end of August 2025)*
- Azure Cost Management and Billing
- **✅ Azure Pricing Calculator**

**Explanation:** The Azure Pricing Calculator lets organizations plan and forecast cloud expenses, evaluate configurations and pricing models, and make informed service/deployment decisions — useful both for discovery-phase planning and post-purchase optimization. Advisor optimizes existing Azure deployments; Cost Management tracks actual spend on already-deployed resources; the TCO Calculator (which specifically compared on-prem vs. Azure costs) has been retired.

---

### Question 34
The IT manager needs to estimate monthly costs for 5 VMs, 2 Azure SQL databases, and 10 TB of Blob Storage across two regions, before deploying anything. Which tool should be used?

- **✅ Azure Pricing Calculator**
- Total Cost of Ownership (TCO) Calculator
- Azure Advisor
- Azure Cost Management and Billing

**Explanation:** The Azure Pricing Calculator is designed specifically to estimate costs for Azure services before deployment, letting users configure services (region, tier, quantity) to get detailed monthly cost estimates. The TCO Calculator compares on-prem vs. cloud costs generally, rather than granular service pricing; Advisor and Cost Management both work only with resources already deployed.

---

### Question 35
An on-premises application server (8 vCPUs, 32 GB RAM, Windows Server 2022) needs full OS control, custom software installation, and support for these specs. What should you recommend?

- Azure Container Instances
- **✅ Azure Virtual Machines**
- Azure App Service
- Azure Functions

**Explanation:** Azure Virtual Machines (IaaS) provide full control over the OS, support custom software installation, and let you select VM sizes matching specific vCPU/memory requirements — meeting every stated need. ACI's shared-kernel container model doesn't offer full OS control; App Service and Functions (PaaS/serverless) don't allow direct OS-level control or custom software installation.

---

### Question 36
The CFO needs monthly cost reports broken down by department (Marketing, Finance, IT) across Azure resources. What is the most effective way to accomplish this?

- Use Microsoft Defender for Cloud to track and report on departmental resource costs.
- Create separate Azure subscriptions for each department and generate cost reports per subscription.
- **✅ Apply tags with department names to resources and use cost analysis to filter and group spending by tag values.**
- Create separate resource groups for each department and manually calculate costs per resource group.

**Explanation:** Tags are name-value pairs designed for organizational purposes like cost tracking, and Azure Cost Management natively supports filtering/grouping by tag — the most efficient, scalable solution without restructuring the environment. Separate subscriptions add unnecessary administrative overhead; resource groups alone don't natively support flexible cost breakdowns the way tags do; Defender for Cloud is a security tool, not a cost management tool.

---

### Question 37
In an IaaS deployment using Azure VMs, which security task remains the company's responsibility?

- **✅ Security patches and updates for the operating system running on the virtual machines**
- Security of the Azure hypervisor layer
- Physical network infrastructure connecting the Azure datacenter
- Physical security of the datacenter hosting the virtual machines

**Explanation:** Under the shared responsibility model for IaaS, the customer manages the guest OS and everything above it — including OS patches, applications, and data — while Microsoft manages the hypervisor, physical network, and datacenter physical security across all service models.

---

### Question 38
VMs across multiple subscriptions must be created only in specific regions (East US and West Europe) for data residency compliance. What should you use to enforce this?

- Role-based access control (RBAC)
- Microsoft Defender for Cloud
- Resource locks
- **✅ Azure Policy**

**Explanation:** Azure Policy enforces organizational standards and can restrict which regions resources may be deployed to, denying non-compliant deployments across multiple subscriptions. RBAC controls permissions, not deployment location; Defender for Cloud focuses on security posture; resource locks protect existing resources but don't restrict where new ones can be created.

---

### Question 39
The finance department needs to forecast annual cloud spending, predicting monthly costs within a 5% variance. Which Azure benefit best addresses this?

- Performance predictability
- **✅ Cost predictability**
- High availability
- Disaster recovery

**Explanation:** Cost predictability lets organizations forecast and control cloud spending using tools like Azure Cost Management, pricing calculators, and cost alerts, directly supporting accurate budget forecasting. Performance predictability relates to consistent application performance, not spending; high availability and disaster recovery relate to uptime and resilience, not financial forecasting.

---

### Question 40
The IT director wants an authentication method that eliminates the need for users to remember/enter passwords while still providing strong authentication. Which method should you recommend?

- Security questions and answers
- **✅ Windows Hello for Business**
- Username and complex password with regular password rotation
- Multi-factor authentication using SMS text messages

**Explanation:** Windows Hello for Business is a passwordless authentication method using biometrics (facial recognition, fingerprint) or a device-bound PIN, eliminating passwords while providing strong, phishing-resistant authentication. Security questions and password-based MFA (SMS) still rely on a password/knowledge-based factor; complex password rotation is itself a traditional password method.

---

### Question 41
Before migrating 50 on-premises servers, databases, and web apps, the IT manager wants server dependency discovery, Azure cost estimates, and right-sizing recommendations. Which service should they use?

- **✅ Azure Migrate**
- Microsoft Defender for Cloud
- Azure Monitor
- Azure Advisor

**Explanation:** Azure Migrate is the centralized hub for assessing and migrating on-premises servers, databases, and applications — offering discovery, dependency mapping, cost estimates, and right-sizing recommendations. Defender for Cloud handles security; Azure Monitor tracks already-deployed resources; Advisor optimizes existing Azure deployments, not pre-migration on-premises assessment.

---

### Question 42
A manufacturing company must keep proprietary production control systems on-premises (regulatory/latency needs) while migrating other workloads to Azure, with consistent management tools and seamless connectivity across both. Which cloud model should the company implement?

- Private cloud
- Public cloud
- **✅ Hybrid cloud**
- Community cloud

**Explanation:** Hybrid cloud combines on-premises infrastructure with public cloud services, letting the company keep sensitive production systems on-premises while leveraging Azure for other workloads, with tools like Azure Arc/Azure Stack enabling unified management and connectivity. Private cloud lacks public cloud integration; public cloud excludes on-premises retention; community cloud addresses shared infrastructure across organizations, not this scenario.

---

### Question 43
Two virtual networks in different regions (East US and West Europe) need direct communication between VMs using private IP addresses. Which solution should you implement?

- Deploy Azure DNS to enable name resolution between the two virtual networks
- Configure Azure VPN Gateway to establish a site-to-site VPN connection between the two virtual networks
- **✅ Configure virtual network peering between VNet-Production and VNet-Development**
- Create a shared subnet that spans both virtual networks

**Explanation:** Virtual network peering connects Azure virtual networks (even across regions, via global VNet peering) with low-latency, high-bandwidth private IP connectivity over Microsoft's backbone — the recommended native solution. DNS only resolves names, not connectivity; VPN Gateway works but is more complex/costly with lower bandwidth than peering; subnets cannot span multiple virtual networks.

---

### Question 44
Users report slow page load times in an App Service web app, but the team can't identify which components cause it. Which monitoring solution automatically detects anomalies, tracks user behavior, and identifies problematic dependencies?

- Azure Monitor Logs
- Microsoft Defender for Cloud
- Azure Service Health
- **✅ Application Insights**

**Explanation:** Application Insights (a feature of Azure Monitor) provides application performance management (APM): automatic anomaly detection, dependency tracking, and user behavior analytics — directly identifying bottlenecks like slow dependencies and failed requests. Monitor Logs handles log queries generally; Defender for Cloud addresses security; Service Health covers Azure platform status, not app-level performance.

---

### Question 45
Users from a partner company need access to a specific application without creating separate accounts in your directory; the partner manages their own users' credentials. Which feature should you use?

- **✅ Microsoft Entra B2B collaboration**
- Microsoft Entra B2C
- Microsoft Entra Conditional Access
- Microsoft Entra Domain Services

**Explanation:** Microsoft Entra B2B lets you invite external users as guests, letting the partner organization retain control of their identities while you control resource access — no duplicate accounts needed. B2C targets consumer-facing apps, not partner collaboration; Conditional Access enforces policies but doesn't itself enable external guest access; Domain Services provides legacy domain services, unrelated to this need.

---

### Question 46
The security team wants to implement defense-in-depth for a web app using VMs, Azure SQL Database, and sensitive customer data. Which approach best demonstrates this?

- Configure role-based access control (RBAC) for all resources and implement Microsoft Entra ID authentication for application users.
- **✅ Implement multiple layers of security including network security groups, encryption at rest for the database, multi-factor authentication with Microsoft Entra ID, and Microsoft Defender for Cloud monitoring.**
- Implement only network security groups (NSGs) with strict rules to control all traffic to and from the virtual machines and database.
- Focus security efforts exclusively on the perimeter by implementing a firewall and ensuring all virtual machines are updated with the latest security patches.

**Explanation:** True defense-in-depth combines controls across multiple layers — network (NSGs), data (encryption at rest), identity (MFA with Entra ID), and monitoring (Defender for Cloud) — so that if one layer fails, others still protect the system. Options relying on RBAC/authentication alone, NSGs alone, or perimeter-only defenses represent single-layer approaches that violate the defense-in-depth principle.

---

### Question 47
A business-critical application must remain available even if an entire Azure region becomes unavailable due to disaster. Which feature provides automatic platform-service replication to a secondary location?

- Availability Zones within a single region
- **✅ Azure region pairs**
- Resource groups spanning multiple regions
- Availability Sets in multiple regions

**Explanation:** Azure region pairs are two regions within the same geography (typically 300+ miles apart) paired for disaster recovery; Azure sequences updates and automatically replicates certain platform services (e.g., geo-redundant storage) between them for cross-region resilience. Availability Zones and Availability Sets only provide protection within a single region/datacenter; resource groups are logical containers with no replication capability.

---

### Question 48
500 employees need single sign-on access to both Microsoft 365 and custom Azure applications. Which service should you recommend?

- Azure Active Directory Domain Services (Azure AD DS)
- **✅ Microsoft Entra ID**
- Windows Server Active Directory running on Azure Virtual Machines
- Azure Key Vault

**Explanation:** Microsoft Entra ID is Microsoft's cloud-based identity and access management service, providing SSO across Microsoft 365 and Azure applications as the centralized cloud/hybrid identity provider. Azure AD DS targets legacy lift-and-shift domain services; Windows Server AD on VMs adds unnecessary management overhead without native cloud SSO; Key Vault manages secrets/keys, not identity/authentication.

---

### Question 49
An e-commerce app serves ~1,000 users normally but spikes to 50,000 concurrent users during sales events. The company wants to handle spikes while minimizing costs during normal periods. Which capability best addresses this?

- **✅ Horizontal scaling (scaling out)**
- High availability
- Vertical scaling (scaling up)
- Geo-distribution

**Explanation:** Horizontal scaling (scale out/in) adds instances during high demand and removes them when demand drops, letting the app handle 50,000-user spikes while minimizing cost during normal 1,000-user periods. High availability addresses uptime/redundancy, not demand fluctuation; vertical scaling has practical limits and often requires downtime, making it less cost-effective for such wide swings; geo-distribution addresses latency/DR across locations, not elastic capacity.

---

### Question 50
A development team wants to deploy a new web app while focusing only on code — no infrastructure, OS, or web server management — with automatic scaling and built-in load balancing. Which service should the company use?

- **✅ Azure App Service**
- Azure Functions
- Azure Container Instances
- Azure Virtual Machines

**Explanation:** Azure App Service is a fully managed PaaS that lets developers deploy web apps without managing infrastructure, OS, or web servers, while providing built-in automatic scaling and load balancing. Azure Functions targets short-running, event-driven code rather than full continuous web apps; Container Instances requires containerization and lacks the same built-in web hosting/scaling features; Virtual Machines require full OS and infrastructure management.

---

## Quick-Reference Answer Key

| # | Answer | # | Answer | # | Answer | # | Answer | # | Answer |
|---|--------|---|--------|---|--------|---|--------|---|--------|
| 1 | Availability zones | 11 | Conditional Access | 21 | Azure Arc | 31 | Azure Government | 41 | Azure Migrate |
| 2 | Hybrid cloud | 12 | Pay only for usage | 22 | Alert rule | 32 | Functions (consumption) | 42 | Hybrid cloud |
| 3 | Service Health | 13 | Azure Functions | 23 | ARM templates | 33 | Pricing Calculator | 43 | VNet peering |
| 4 | Azure Advisor | 14 | ARM templates | 24 | Defender for Cloud | 34 | Pricing Calculator | 44 | Application Insights |
| 5 | Availability zones | 15 | Azure Policy | 25 | Microsoft Purview | 35 | Virtual Machines | 45 | Entra B2B |
| 6 | Microsoft-managed tools | 16 | Delete lock | 26 | Azure Portal | 36 | Tags + cost analysis | 46 | Multi-layer defense |
| 7 | Blob Storage + lifecycle | 17 | Azure File Sync | 27 | ARM templates | 37 | OS patches | 47 | Region pairs |
| 8 | Custom RBAC role | 18 | ZRS | 28 | PAYG + auto shutdown | 38 | Azure Policy | 48 | Microsoft Entra ID |
| 9 | AKS | 19 | Entra ID B2C | 29 | Pay-as-you-go | 39 | Cost predictability | 49 | Horizontal scaling |
| 10 | Azure Virtual Desktop | 20 | PaaS / App Service | 30 | Public cloud | 40 | Windows Hello for Business | 50 | Azure App Service |
