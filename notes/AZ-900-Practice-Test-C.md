# Azure Practice Quiz — Questions & Answers

---

### Question 1 — *Secure Azure Networking*
**Why should you divide your application into multiple subnets as opposed to having all your web, application and database servers running on the same subnet?**

- There are only a limited number of IP addresses available per subnet, so you need multiple subnets over a certain number.
- Each server type of your application requires its own subnet. It's not possible to mix web servers, database servers and application servers on the same subnet.
- ✅ **Separating your application into multiple subnets allows you to have different NSG security rules for each subnet, which can make it harder for a hacker to get from one compromised server onto another.**

**Explanation:** For security purposes, you should not allow "port 80" web traffic to reach certain servers, and you do that by having separate NSG rules on each subnet.

📄 [More info](https://docs.microsoft.com/en-us/azure/security/fundamentals/network-best-practices)

---

### Question 2 — *Security tools and features*
**Which Azure networking service allows you to securely connect your on-premises network to Azure over the internet?**

- Azure Load Balancer — distributes traffic across servers; does not connect on-premises networks to Azure.
- ✅ **Azure VPN Gateway** — enables secure, encrypted connections between on-premises networks and Azure over the public internet.
- Azure Virtual Network (VNet) — provides isolation/segmentation, not secure internet connections.
- Azure ExpressRoute — private dedicated connection that bypasses the public internet (not "over the internet").

---

### Question 3 — *Benefits of cloud services*
**Which of the following is a key benefit of using cloud services like Microsoft Azure?**

- Fixed costs that do not vary based on usage. *(Incorrect — Azure costs scale with usage.)*
- Limited scalability and flexibility for changing workloads. *(Incorrect — Azure offers strong scalability.)*
- ✅ **Reduced upfront capital expenditure (CapEx) by paying only for what you use.**
- Increased responsibility for managing physical hardware and infrastructure. *(Incorrect — Azure reduces this responsibility.)*

**Explanation:** Operating Expenditure is preferable because you can fully deduct expenses when incurred.

📄 [More info](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/strategy/business-outcomes/fiscal-outcomes)

---

### Question 4 — *Core Azure components*
**What data format are ARM templates created in?**

HTML | ✅ **JSON** | YAML | XML

📄 [More info](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/overview)

---

### Question 5 — *Benefits of cloud services*
**What is the core problem that you need to solve in order to have a high-availability application?**

- You need to ensure your server has a lot of RAM and a lot of CPUs
- You need to ensure the capacity of your server exceeds your highest number of expected concurrent users
- You should have a backup copy of your application on standby, ready to be started up when the main application fails.
- ✅ **You need to avoid single points of failure**

📄 [More info](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/redundancy)

---

### Question 6 — *Core Azure products*
**Which database product offers "sub 5 millisecond" response times as a feature?**

✅ **Cosmos DB** | SQL Server in a VM | Azure SQL Database | SQL Data Warehouse

📄 [More info](https://docs.microsoft.com/en-us/azure/cosmos-db/introduction)

---

### Question 7 — *Monitoring and reporting*
**If you wanted to get an alert every time a new virtual machine is created, where could you create that?**

✅ **Azure Monitor** | Subscription settings | Azure Policy | Azure Dashboard

📄 [More info](https://docs.microsoft.com/en-us/azure/azure-monitor/)

---

### Question 8 — *Core Azure products*
**What operating systems does an Azure Virtual Machine support?**

Windows, Linux and macOS | Windows | macOS | ✅ **Windows and Linux** | Linux

📄 [More info](https://docs.microsoft.com/en-us/azure/virtual-machines/)

---

### Question 9 — *Azure subscriptions*
**What is an Azure Subscription?**

- Each user account is associated with a unique subscription. If you need more than one subscription, you need to create multiple user accounts. *(Incorrect)*
- ✅ **It is the level at which services are billed. All resources created under a subscription are billed to that subscription.**

📄 [More info](https://docs.microsoft.com/en-us/services-hub/health/azure_sponsored_subscription)

---

### Question 10 — *Core Azure solutions*
**What is the name of the collective set of APIs that provide machine learning and artificial intelligence services (voice recognition, image tagging, chat bots) to your own applications?**

Azure Machine Learning Studio | Azure Batch | ✅ **Azure AI services (formerly Cognitive Services)** | Azure AI Language services (formerly LUIS)

📄 [More info](https://learn.microsoft.com/en-us/azure/ai-services/)

---

### Question 11 — *Service lifecycle in Azure*
**True or false: If your feature is in the General Availability phase, then your feature will receive support from all Microsoft support channels.**

✅ **TRUE** | FALSE

**Explanation:** Do not use preview features in production apps.

📄 [More info](https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/)

---

### Question 12 — *Core Azure components*
**What are groups of subscriptions called?**

ARM Groups | Azure Policy | Subscription Groups | ✅ **Management Groups**

**Explanation:** Subscriptions can be nested and placed into management groups to make managing them easier.

📄 [More info](https://docs.microsoft.com/en-us/azure/governance/management-groups/overview)

---

### Question 13 — *Azure subscriptions*
**If you have an Azure free account, with a $200 credit for the first month, what happens when you reach the $200 limit?**

- Your credit card is automatically billed.
- You cannot create any more resources until you add more credits to the account.
- Your account is automatically closed.
- ✅ **All services are stopped and you must decide whether you want to convert to a paid account or not.**

📄 [More info](https://azure.microsoft.com/en-us/free/free-account-faq/)

---

### Question 14 — *Azure management tools*
**Which tool within the Azure Portal will make specific recommendations based on your actual usage for how you can improve your use of Azure?**

Azure Monitor | Azure Service Health | Azure Dashboard | ✅ **Azure Advisor**

📄 [More info](https://docs.microsoft.com/en-us/azure/advisor/)

---

### Question 15 — *Azure governance methodologies*
**What does the letter R in RBAC stand for?**

Review | Rule | ✅ **Role** | Rights

📄 [More info](https://docs.microsoft.com/en-us/azure/role-based-access-control/)

---

### Question 16 — *Core Azure products*
**Which Azure compute service allows you to run containerized applications without managing the underlying infrastructure?**

- Azure App Service — PaaS for web apps/APIs, not primarily for containers without infra management.
- Azure Kubernetes Service (AKS) — managed Kubernetes, but you still manage the cluster's underlying infrastructure.
- ✅ **Azure Container Instances** — serverless container service, no infrastructure to manage.
- Azure Virtual Machines — gives full control over infrastructure; not container-focused.

---

### Question 17 — *Azure Identity services*
**Which of the following scenarios is best addressed by using Microsoft Entra ID?**

- Automating the deployment of virtual machines using Infrastructure as Code (IaC). *(Better suited to ARM templates / IaC tools.)*
- Storing and analyzing large volumes of structured data. *(Not Entra ID's purpose.)*
- ✅ **Providing a centralized identity management solution for hybrid cloud environments.**
- Monitoring the performance of Azure resources in real-time. *(Better suited to Azure Monitor / Application Insights.)*

---

### Question 18 — *Core Azure solutions*
**Which of the following would be an example of an Internet of Things (IoT) device?**

- A mobile application used to watch online video courses
- ✅ **A refrigerator that monitors how much milk you have left and sends you a text message when you are running low**
- A web application used for banking tasks
- A video game installed on Windows clients that keeps user scores in the cloud

📄 [More info](https://docs.microsoft.com/en-us/azure/iot-fundamentals/iot-introduction)

---

### Question 19 — *Benefits of cloud services*
**What two advantages does cloud computing elasticity give to you? (Pick two)**

- Servers have become a commodity and Microsoft doesn't even need to fix servers that fail within Azure.
- ✅ **You can serve users better during peak traffic periods by automatically adding more capacity.**
- You can do more regular backups and you won't lose as much when that backup gets restored.
- ✅ **You can save money.**

📄 [More info](https://azure.microsoft.com/en-us/overview/what-is-elastic-computing/)

---

### Question 20 — *IaaS, PaaS and SaaS*
**Deploying Azure App Services applications consists of what two components? (Pick two)**

- ✅ **Configuration**
- ✅ **Packaged code**
- Database scripts
- Managing operating system updates

📄 [More info](https://docs.microsoft.com/en-us/azure/app-service/)

---

### Question 21 — *Service lifecycle in Azure*
**What does it mean if a service is in Private Preview mode?**

- ✅ **You have to apply to get selected in order to use that service**
- Anyone can use the service but it must not be for production use
- The service is generally available for use, and Microsoft will provide support for it
- Anyone can use the service for any reason

📄 [More info](https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms)

---

### Question 22 — *Azure costs*
**How do you stop your Azure account from incurring costs above a certain level without your knowledge?**

- ✅ **Implement the Azure spending limit in the Account Center**
- Only use Azure Functions which have a significant free limit
- Switch to Azure Reserved Instances with Hybrid Benefit for VMs
- Set up a billing alert to send you an email when it reaches a certain level

📄 [More info](https://docs.microsoft.com/en-us/azure/cost-management-billing/manage/spending-limit)

---

### Question 23 — *IaaS, PaaS and SaaS*
**Which of the following services would NOT be considered Infrastructure as a Service?**

Virtual Network Interface Card (NIC) | Virtual Machine | ✅ **Azure Functions App** | Virtual Network

**Explanation:** Functions are small pieces of code that you give to Azure to run for you, and you have no access to the underlying infrastructure.

📄 [More info](https://docs.microsoft.com/en-us/azure/azure-functions/)

---

### Question 24 — *Azure management tools*
**Which Azure service, when enabled, will automatically block traffic to or from known malicious IP addresses and domains?**

✅ **Azure Firewall** | Load Balancer | Azure Active Directory | Network Security Groups

**Explanation:** Azure Firewall has a threat-intelligence option that automatically blocks traffic to/from bad actors on the internet.

📄 [More info](https://docs.microsoft.com/en-us/azure/firewall/)

---

### Question 25 — *Azure Identity services*
**How does Multi-Factor Authentication make a system more secure?**

- It is another password that a user has to memorize, making it more secure
- It allows the user to log in without a password because they have already previously been validated using a browser cookie
- ✅ **It requires the user to have access to their verified phone in order to log in**
- It doesn't make it more secure

📄 [More info](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-mfa-howitworks)

---

### Question 26 — *Secure Azure Networking*
**What is the goal of a DDoS attack?**

- To crack the password from administrator accounts
- To trick users into giving up personal information
- To extract data from a database
- ✅ **To overwhelm and exhaust application resources**

📄 [More info](https://docs.microsoft.com/en-us/azure/virtual-network/ddos-protection-overview)

---

### Question 27 — *Core Azure products*
**Which two features does Virtual Machine Scale Sets provide as part of the core product? (Pick two)**

- Firewall
- ✅ **Autoscaling of virtual machines**
- Automatic installation of supporting apps and deployment of custom code
- ✅ **Load balancing between virtual machines**
- Content Delivery Network

**Explanation:** VMSS provides autoscale features and has a built-in load balancer. You still need your own way to deploy code to new servers.

📄 [More info](https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/)

---

### Question 28 — *Monitoring and reporting*
**Which feature within Azure alerts you to service issues that happen in Azure itself, not specifically related to your own resources?**

Azure Security Center | Azure Monitor | Azure Portal Dashboard | ✅ **Azure Service Health**

📄 [More info](https://docs.microsoft.com/en-us/azure/service-health/)

---

### Question 29 — *Azure Identity services*
**TRUE OR FALSE: Azure Tenant is a dedicated and trusted instance of Microsoft Entra ID that's automatically created when your organization signs up for a Microsoft cloud service subscription.**

✅ **TRUE** | FALSE

📄 [More info](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-whatis)

---

### Question 30 — *Privacy and compliance*
**What type of documents does the Microsoft Service Trust Portal provide?**

✅ **A list of standards that Microsoft follows, pen test results, security assessments, white papers, FAQs, and other documents that can be used to show Microsoft's compliance efforts**
- Specific recommendations about your usage of Azure and ways you can improve
- A tool that helps you manage your compliance to various standards
- Documentation on the individual Azure services and solutions

📄 [More info](https://servicetrust.microsoft.com/)

---

### Question 31 — *Azure management tools*
**What is the primary purpose of Azure Sovereign Regions?**

- To provide lower-cost Azure services for small and medium-sized businesses. *(Incorrect)*
- To provide free Azure services for educational institutions and non-profits. *(Incorrect)*
- ✅ **To offer Azure services that comply with specific government regulations and data residency requirements.**
- To enable faster performance for global applications by reducing latency. *(Incorrect)*

📄 [More info](https://docs.microsoft.com/en-us/azure/china/overview-checklist)

---

### Question 32 — *Security tools and features*
**What is the recommended way within Azure to store secrets such as private cryptographic keys?**

In an Azure Storage account private blob container | ✅ **Azure Key Vault** | Azure Advanced Threat Protection (ATP) | Within the application code

📄 [More info](https://docs.microsoft.com/en-us/azure/key-vault/)

---

### Question 33 — *Benefits of cloud services*
**How many minutes per month downtime is 99.99% availability?**

40 | 100 | 1 | ✅ **4**

📄 [More info](https://azure.microsoft.com/en-us/support/legal/sla/summary/)

---

### Question 34 — *Core Azure solutions*
**What is the primary benefit of using Azure Virtual Desktop (AVD)?**

- It provides a fully managed database service for relational and non-relational data. *(Incorrect)*
- It offers a serverless computing platform for running event-driven applications. *(Incorrect)*
- It automates the deployment and management of containerized applications. *(Incorrect)*
- ✅ **It enables users to access virtualized desktops and applications from anywhere, on any device.**

---

### Question 35 — *Azure costs*
**How many hours are available free when using the Azure B1S General Purpose Virtual Machines under an Azure free account in the first 12 months?**

500 hrs | Indefinite amount of hrs | ✅ **750 hrs** | 300 hrs

📄 [More info](https://azure.microsoft.com/en-us/free/free-account-faq/)

---

### Question 36 — *Azure management tools*
**Which Azure management tool analyzes your usage of Azure and makes suggestions specifically targeted to help you optimize your usage of Azure regarding cost, security and performance?**

Azure Service Health | ✅ **Azure Advisor** | Azure Mobile App | Azure Firewall

---

### Question 37 — *Security tools and features*
**What does it mean that security is a "shared model" in Azure?**

- You must keep your security keys private and ensure it doesn't get out.
- Azure takes no responsibility for security.
- ✅ **Both users and Azure have responsibilities for security.**
- Azure takes care of security completely.

📄 [More info](https://docs.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility)

---

### Question 38 — *IaaS, PaaS and SaaS*
**Which style of computing is easiest when migrating an existing hosted application from your own data center into the cloud?**

✅ **IaaS** | FaaS | Serverless | PaaS

**Explanation:** Infrastructure as a Service is the easiest to migrate into from an existing hosted app — "lift and shift."

📄 [More info](https://azure.microsoft.com/en-us/overview/what-is-iaas/)

---

### Question 39 — *Azure SLAs*
**What happens if Azure does not meet its own Service Level Agreement guarantee (SLA)?**

- It's not possible. Azure will always meet its SLA.
- The service will be free that month.
- ✅ **You will be financially refunded a small amount of your monthly fee**

**Explanation:** Microsoft offers a refund of 10% or 25% depending on how badly they miss their service guarantee.

📄 [More info](https://azure.microsoft.com/en-us/support/legal/sla/)

---

### Question 40 — *Azure Identity services*
**What software is used to synchronize your on-premises AD with your Azure AD?**

Azure AD Domain Services | LDAP | ✅ **AD Connect** | Azure AD Federation Services

📄 [More info](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-azure-ad-connect)

---

### Question 41 — *Privacy and compliance*
**Where can you go to see what standards Microsoft is in compliance with?**

✅ **Trust Center** | Azure Service Health | Azure Security Center | Azure Privacy Page

📄 [More info](https://www.microsoft.com/en-us/trust-center)

---

### Question 42 — *Core Azure products*
**What advantage does an Application Gateway have over a Load Balancer?**

- Application Gateway can be scaled so that two, three or more instances of the gateway can support your application.
- Application Gateway is more like an enterprise-grade product. You should not use a load balancer in production.
- ✅ **Application Gateway understands the HTTP protocol and can interpret the URL and make decisions based on the URL.**

📄 [More info](https://docs.microsoft.com/en-us/azure/application-gateway/overview)

---

### Question 43 — *Core Azure components*
**What is the significance of the Azure region? Why is it important?**

- Even though you have to choose a region when creating resources, there's generally no consequence of what you select — you can mix regions freely. *(Incorrect)*
- Region is just a folder structure, much like file folders on a computer. *(Incorrect)*
- ✅ **You must select a region when creating most resources, and the region is the area of the world where those resources will be physically located.**
- Once you select a region, you cannot create resources outside of that region. *(Incorrect)*

📄 [More info](https://azure.microsoft.com/en-us/global-infrastructure/geographies/#overview)

---

### Question 44 — *Public, Private and Hybrid cloud*
**With Azure public cloud, anyone with a valid credit card can sign up and get services immediately.**

✅ **TRUE** | FALSE

📄 [More info](https://docs.microsoft.com/en-us/learn/modules/create-an-azure-account/)

---

### Question 45 — *Public, Private and Hybrid cloud*
**Which of the following is an advantage of running your cloud in a private cloud?**

- ✅ **Assurance that your code, data and applications are running on isolated hardware, and on an isolated network.**
- You own the hardware, so you can change private cloud hosting providers easily.
- Private cloud is significantly cheaper than the public cloud.

📄 [More info](https://azure.microsoft.com/en-us/overview/what-are-private-public-hybrid-clouds/)

---

### Question 46 — *Azure governance methodologies*
**What is a policy initiative in Azure?**

✅ **The ability to group policies together**
- Requiring all resources in Azure to use tags
- Assigning permissions to a role in Azure
- A custom designed policy

📄 [More info](https://docs.microsoft.com/en-us/azure/governance/policy/overview#initiative-definition)

---

### Question 47 — *Azure management tools*
**What is a key benefit of using Azure Cloud Shell?**

- ✅ **It provides a pre-configured, browser-based shell for managing Azure resources without requiring local installations.**
- It allows you to run virtual machines directly in the browser. *(Incorrect)*
- It automatically optimizes the cost of your Azure resources. *(Incorrect)*
- It provides a graphical user interface (GUI) for managing Azure services. *(Incorrect — it's command-line based.)*

---

### Question 48 — *Azure SLAs*
**What is the service level agreement for two or more Azure Virtual Machines that have been placed into the same Availability Set in the same region?**

✅ **99.95%** | 99.90% | 100% | 99.99%

📄 [More info](https://azure.microsoft.com/en-us/support/legal/sla/virtual-machines/v1_9/)

---

### Question 49 — *Core Azure components*
**What are resource groups?**

✅ **A folder structure in Azure in which you organize resources like databases, virtual machines, virtual networks, or almost any resource**
- Automatically assigned groups of resources that all have the same type (virtual machine, app service, etc.)
- Within Azure's security model, users are organized into groups, and those groups are granted permissions to resources
- Based on the tag assigned to a resource by the deployment script, it is assigned to a group

📄 [More info](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/manage-resource-groups-portal)

---

### Question 50 — *Azure Identity services*
**Which Azure service can be enabled to enable Multi-Factor Authentication for administrators but not require it for regular users?**

✅ **Privileged Identity Management** | Azure Firewall | Azure AD B2B | Advanced Threat Protection

📄 [More info](https://docs.microsoft.com/en-us/azure/active-directory/privileged-identity-management/pim-configure)
