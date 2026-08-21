# AZ-900 Practice Exam — Full Question Set

**Score:** 41/50 (82%)

---

### Question 1 — ✅ Correct
**Which is the lowest-cost storage redundancy option?**

- **LRS** ✔️ *(Your answer — Correct)*
  LRS (Locally Redundant Storage) is the lowest-cost storage redundancy option in Azure. It replicates your data three times within a storage scale unit in a datacenter.
- ZRS — Replicates across multiple availability zones within the same region; higher resilience but not lowest-cost.
- GRS — Replicates to a secondary region; higher durability but not lowest-cost.
- GZRS — Combines GRS + ZRS; highest resilience but not lowest-cost.

**Domain:** Describe Azure storage services

---

### Question 2 — ✅ Correct
**What is the primary purpose of single sign-on (SSO)?**

- To add an extra layer of security to user accounts. — Not the primary purpose.
- To enforce strong password policies. — Not the primary purpose.
- To prevent unauthorized access to cloud resources. — Not the primary purpose.
- **To allow users to log in to multiple applications with a single set of credentials.** ✔️ *(Your answer — Correct)*
  Simplifies the user experience, improves productivity, and reduces password fatigue risk.

**Domain:** Describe Azure identity, access, and security

---

### Question 3 — ✅ Correct
**What does cost predictability mean in the context of Azure?**

- **The ability to accurately forecast future costs.** ✔️ *(Your answer — Correct)*
  Helps organizations plan budgets and avoid surprise expenses.
- The ability to reduce costs over time. — Not the focus of predictability.
- The ability to allocate costs to specific resources. — Related to cost tracking, not predictability.
- The ability to avoid unexpected charges. — Related but distinct from forecasting.

**Domain:** Describe the benefits of using cloud services

---

### Question 4 — ✅ Correct
**Which of the following is an example of a PaaS offering from Azure?**

- Azure Virtual Machines — IaaS, not PaaS.
- Microsoft Entra ID — Identity/access management service, not PaaS.
- **Azure App Service** ✔️ *(Your answer — Correct)*
  PaaS offering for building, deploying, and scaling web apps/APIs without managing infrastructure.
- Azure Storage (GPv2) — Storage service, not PaaS.

**Domain:** Describe cloud service types

---

### Question 5 — ✅ Correct
**Which of the following is a key feature of Azure Virtual Machine Scale Sets?**

- **They automatically scale the number of VM instances based on demand or a schedule.** ✔️ *(Your answer — Correct)*
- They provide a GUI for managing VMs. — Managed via ARM templates, PowerShell, or CLI instead.
- Limited to 10 VMs per scale set. — No such limit; can scale to hundreds/thousands.
- Allow manual creation/management of individual VMs. — Contrary to the automated scaling purpose.

**Domain:** Describe Azure compute and networking services

---

### Question 6 — ✅ Correct
**What is the principle of least privilege in the context of Azure RBAC?**

- Granting users the maximum access necessary. — Opposite of least privilege.
- **Granting users the minimum amount of access necessary to perform their job duties.** ✔️ *(Your answer — Correct)*
- Disabling user accounts when not in use. — Good practice, but unrelated to least privilege.
- Assigning "Owner" role to all users. — Directly against least privilege.

**Domain:** Describe Azure identity, access, and security

---

### Question 7 — ❌ Incorrect
**What is the maximum number of web apps a single App Service Plan (Premium v3) can support?**

- 100 — Incorrect; supports more.
- 1 — Incorrect; supports more.
- 10 — Incorrect; supports more.
- **Unlimited** ✔️ *(Correct answer)* | *(Your answer: 100 — Incorrect)*
  A single Premium v3 App Service Plan supports an unlimited number of web apps.

**Domain:** Describe Azure compute and networking services

---

### Question 8 — ❌ Incorrect
**In which storage redundancy option does Azure keep six copies of your files across two regions?**

- LRS — Only replicates within the same region.
- **GRS** ✔️ *(Correct answer)*
  Replicates data to a secondary region, resulting in six copies across two regions.
- ZRS — *(Your answer — Incorrect)* Replicates across zones within a single region only.

**Domain:** Describe Azure storage services

---

### Question 9 — ✅ Correct
**True or false: Azure peering can connect two networks even though they belong to different subscriptions or customer accounts.**

- **TRUE** ✔️ *(Your answer — Correct)*
  Azure peering allows two networks to connect even across different subscriptions or AAD tenants.
- FALSE — Incorrect; peering does support this.

**Domain:** Describe Azure compute and networking services

---

### Question 10 — ❌ Incorrect
**Which connectivity option provides connectivity from on-premises into Azure over a private line, not over the public Internet?**

- Azure Global Peering — Connects Azure networks to Microsoft's backbone, not on-prem to Azure privately.
- Point-to-site VPN — Individual devices connecting over the public Internet.
- Site-to-site VPN — *(Your answer — Incorrect)* Secure, but still travels over the public Internet.
- **Azure ExpressRoute** ✔️ *(Correct answer)*
  Provides a private, dedicated connection that doesn't travel over the public Internet.

**Domain:** Describe Azure compute and networking services

---

### Question 11 — ✅ Correct
**What is the primary purpose of Azure B2B collaboration?**

- **To allow guest users from external organizations to access your organization's resources.** ✔️ *(Your answer — Correct)*
- To enable customers to purchase products/services directly. — Not the purpose.
- To provide identity/access management for internal users. — Not the primary focus.
- To provide identity/access management for cloud-based applications. — Not the primary focus.

**Domain:** Describe Azure identity, access, and security

---

### Question 12 — ❌ Incorrect
**When an entire Azure region fails, where do some Azure services automatically fail over to?**

- Most regions fail over to US East. — Incorrect; based on region pairing, not a fixed region.
- There are no Azure services that fail over. — *(Your answer — Incorrect)* Azure does have automatic failover for some services.
- Another region, usually in another geography. — Partially true but not as precise as the correct answer.
- **Its region pair, which is at least 300 miles away in the same geography.** ✔️ *(Correct answer)*

**Domain:** Describe the core architectural components of Azure

---

### Question 13 — ✅ Correct
**Who is typically responsible for the security and protection of customer data in the cloud?**

- The cloud provider. — Responsible for infrastructure, not customer data.
- Both equally responsible. — Not accurate; data protection is primarily the customer's job.
- Difficult to say who's responsible. — Inaccurate; responsibilities are well-defined.
- **The customer, such as you.** ✔️ *(Your answer — Correct)*

**Domain:** Describe cloud computing

---

### Question 14 — ✅ Correct
**Which of the following is a built-in role in Azure RBAC?** *(select all that apply)*

- **Reader** ✔️ *(Your selection — Correct)* — Read-only access.
- User — Not a built-in RBAC role.
- **Contributor** ✔️ *(Your selection — Correct)* — Manage resources, cannot grant access to others.
- **Owner** ✔️ *(Your selection — Correct)* — Full access, including managing access for others.

**Domain:** Describe Azure identity, access, and security

---

### Question 15 — ✅ Correct
**How does the consumption-based model help businesses manage their IT costs?**

- By increasing long-term commitments. — Opposite of the model's flexibility.
- By limiting resource usage. — Not the purpose.
- By requiring upfront investments. — Opposite of consumption-based pricing.
- **By aligning costs with actual usage.** ✔️ *(Your answer — Correct)*

**Domain:** Describe cloud computing

---

### Question 16 — ✅ Correct
**What is the primary purpose of Microsoft Entra Conditional Access?**

- To provide MFA for all users. — Part of it, but not the sole purpose.
- To enforce strong password policies. — Not the primary purpose.
- To protect against phishing attacks. — Not the primary purpose.
- **To implement granular access controls based on specific conditions.** ✔️ *(Your answer — Correct)*
  Based on factors like user location, device compliance, application sensitivity, etc.

**Domain:** Describe Azure identity, access, and security

---

### Question 17 — ✅ Correct
**Which of the following statements about Azure Management Groups is true?**

- A subscription can belong to multiple Management Groups simultaneously. — False; only one at a time.
- Limited to 10 subscriptions per group. — False; no such limit.
- Management Groups can contain subscriptions from multiple Azure tenants. — False; single tenant only.
- **Management Groups can be used to apply policies and access controls across multiple subscriptions within the same tenant.** ✔️ *(Your answer — Correct)*

**Domain:** Describe the core architectural components of Azure

---

### Question 18 — ✅ Correct
**Which of the following is an example of a serverless computing service?**

- Storage Accounts — Not serverless computing.
- Virtual Machines — Requires infrastructure management; not serverless.
- **Azure Functions** ✔️ *(Your answer — Correct)*
  Runs code without managing infrastructure; auto-scales and charges only for execution.
- App Services — Still requires managing underlying infrastructure/scaling.

**Domain:** Describe cloud computing

---

### Question 19 — ✅ Correct
**Why is it beneficial to organize Azure resources into resource groups?**

- To enhance security. — A side benefit, not the primary purpose.
- To improve performance. — Not the primary purpose.
- **To simplify management and deployment.** ✔️ *(Your answer — Correct)*
- To reduce costs. — A side benefit, not the primary purpose.

**Domain:** Describe the core architectural components of Azure

---

### Question 20 — ✅ Correct
**Who typically owns the IT infrastructure in the cloud computing model?**

- The client, such as you. — Incorrect; clients don't own the infrastructure.
- **The vendor, such as Microsoft Azure or Amazon AWS.** ✔️ *(Your answer — Correct)*

**Domain:** Describe cloud computing

---

### Question 21 — ❌ Incorrect
**How does high availability help businesses avoid financial losses?**

- By increasing downtime. — Opposite effect.
- **By ensuring uninterrupted revenue generation.** ✔️ *(Correct answer)*
- By preventing data loss. — Related but not the primary financial mechanism described.
- By reducing operational costs. — *(Your answer — Incorrect)* Indirect at best; not the primary purpose.

**Domain:** Describe the benefits of using cloud services

---

### Question 22 — ✅ Correct
**How can tags be used to optimize costs in Azure?**

- By identifying resources for migration to lower-cost tiers. — Done via other tools, not tags directly.
- By automatically shutting down underutilized resources. — Done via automation/policies, not tags directly.
- **By categorizing resources based on their cost and usage.** ✔️ *(Your answer — Correct)*
- By automatically applying discounts to tagged resources. — Tags don't apply discounts automatically.

**Domain:** Describe cost management in Azure

---

### Question 23 — ✅ Correct
**Which of the following is an example of an IaaS offering from Azure?**

- Azure SQL Database — DBaaS, not IaaS.
- Azure App Service — PaaS, not IaaS.
- **Azure Virtual Machines** ✔️ *(Your answer — Correct)*
  Full control over OS, applications, and configurations.
- Azure Functions — Serverless/FaaS, not IaaS.

**Domain:** Describe cloud service types

---

### Question 24 — ❌ Incorrect
**Which Azure Storage access tier is optimized for data rarely accessed, stored for at least 180 days, with flexible latency?**

- Hot access — Optimized for frequent access, not cost-effective here.
- **Archive access** ✔️ *(Correct answer)*
  Lowest storage cost, longer access times, minimum 180-day storage.
- Premium storage — For high-performance, low-latency workloads.
- Cool access — *(Your answer — Incorrect)* For infrequent access that still needs quick retrieval.

**Domain:** Describe Azure storage services

---

### Question 25 — ❌ Incorrect
**Software requires Windows Registry access to run. Which is the only option for running this app in the cloud?**

- SaaS — *(Your answer — Incorrect)* No direct access to Registry.
- Serverless — No direct access to Registry.
- **IaaS** ✔️ *(Correct answer)*
  Provides full control over the OS, including Registry access, via VMs.
- PaaS — Abstracts infrastructure, no Registry access.

**Domain:** Describe cloud service types

---

### Question 26 — ✅ Correct
**A viral traffic spike is handled by automatically adding/removing resources. This property is known as __________.**

- Manageability — Related but not the precise term.
- High availability — Related but not the precise term.
- **Scalability** ✔️ *(Your answer — Correct)*
  Ability to handle increased workload by dynamically adding/removing resources.
- Predictability — Not the property being described.

**Domain:** Describe the benefits of using cloud services

---

### Question 27 — ✅ Correct
**How does Azure Policy help manage Azure resources?**

- By providing real-time alerts for security threats. — Handled by Security Center/Sentinel.
- By automatically scaling resources based on demand. — Handled by Autoscale/Scale Sets.
- By optimizing resource utilization and cost. — Handled by Cost Management/Advisor.
- **By defining rules that govern resource configuration and usage.** ✔️ *(Your answer — Correct)*

**Domain:** Describe tools in Azure for governance and compliance

---

### Question 28 — ✅ Correct
**Which of the following can be considered a benefit of using the cloud regarding security?** *(select all that apply)*

- **Adheres to industry-standard compliance frameworks** ✔️ *(Your selection — Correct)*
- **Regular updates and patches** ✔️ *(Your selection — Correct)*
- Ability to disable security measures such as encryption. — False; some measures (like storage encryption) are mandatory and cannot be disabled.
- **Centralized management and monitoring** ✔️ *(Your selection — Correct)*

**Domain:** Describe the benefits of using cloud services

---

### Question 29 — ✅ Correct
**How does a defense-in-depth model improve overall security?**

- By simplifying the security infrastructure. — Opposite; involves multiple layers.
- By reducing the need for security updates. — Not related.
- **By making it more difficult for attackers to breach multiple layers of security.** ✔️ *(Your answer — Correct)*
- By eliminating the need for user training. — Not related; training remains important.

**Domain:** Describe Azure identity, access, and security

---

### Question 30 — ✅ Correct
**What is an Azure resource?**

- A physical device in an Azure datacenter. — Incorrect; resources are logical, not physical.
- A subscription to Azure services. — Incorrect; a subscription is not itself a resource.
- A software component that provides a service. — Not the precise definition.
- **A logical entity that represents a cloud resource.** ✔️ *(Your answer — Correct)*

**Domain:** Describe the core architectural components of Azure

---

### Question 31 — ❌ Incorrect
**Which of the following is a key benefit of using Microsoft Entra Domain Services?**

- It is a replacement for Azure Active Directory. — *(Your answer — Incorrect)* It complements, not replaces, Azure AD.
- **It provides a managed domain service in the cloud without the need to manage on-premises domain controllers.** ✔️ *(Correct answer)*
- It is only suitable for small-scale deployments. — False; scales to large deployments too.
- It simplifies management of on-premises Active Directory. — Not quite accurate; it's about extending, not simplifying on-prem AD.

**Domain:** Describe Azure identity, access, and security

---

### Question 32 — ✅ Correct
**What is the primary benefit of using containers for deploying applications to Azure?**

- Improved network performance. — Not the primary benefit.
- Enhanced security. — A secondary benefit, not primary.
- Increased storage capacity. — Not related to containers' purpose.
- **Improved portability and consistency.** ✔️ *(Your answer — Correct)*
  Encapsulates app + dependencies for consistent behavior across environments.

**Domain:** Describe Azure compute and networking services

---

### Question 33 — ✅ Correct
**Which Azure service can be used to create a highly available application across multiple Availability Zones?**

- **All answers are correct** ✔️ *(Your answer — Correct)*
  A combination of Azure App Service, Azure Storage, and Azure Virtual Machines can be used together for a resilient, highly available architecture.
- Azure Storage — Alone, doesn't cover all services needed.
- Azure App Service — Alone, doesn't cover all services needed.
- Azure Virtual Machines — Alone, doesn't cover all services needed.

**Domain:** Describe the core architectural components of Azure

---

### Question 34 — ✅ Correct
**What is the primary purpose of Availability Zones in Azure?**

- To offer discounts for customers in certain regions. — Not related.
- **To provide redundancy and fault tolerance.** ✔️ *(Your answer — Correct)*
- To provide access to Azure services in specific geographic locations. — Not the primary purpose.
- To ensure data residency compliance. — A side effect, not the primary purpose.

**Domain:** Describe the core architectural components of Azure

---

### Question 35 — ✅ Correct
**What is a fault domain?**

- Where tectonic plates meet below Earth's surface. — Unrelated geological concept.
- A method to resolve human-readable names into IP addresses. — That's DNS, unrelated.
- **A physical grouping of servers within an Azure data center.** ✔️ *(Your answer — Correct)*
  Limits impact of hardware failure/maintenance to a subset of servers.
- A report available through Azure Service Health. — Unrelated.

**Domain:** Describe Azure compute and networking services

---

### Question 36 — ✅ Correct
**Company runs mostly on-prem but scales to Azure VMs when needed. What is this usage called?**

- Autoscaling — A feature used within this setup, not the overall model name.
- **Hybrid Cloud** ✔️ *(Your answer — Correct)*
  Combines on-premises infrastructure with public cloud services.
- Private Cloud — Doesn't apply since public cloud (Azure) is also used.
- Public Cloud — Doesn't apply since on-prem infrastructure is also used.

**Domain:** Describe cloud computing

---

### Question 37 — ❌ Incorrect
**What type of scaling typically involves adding more resources to a pool of existing resources?**

- **Horizontal scaling** ✔️ *(Correct answer)*
  Also known as scale-out; adds more servers/instances to a pool.
- Scaling up — Same idea as vertical scaling; increases capacity of individual resources.
- Vertical scaling — *(Your answer — Incorrect)* Increases capacity of existing resources (scale-up), not adding more to a pool.

**Domain:** Describe the benefits of using cloud services

---

### Question 38 — ✅ Correct
**Which cloud pricing model is often used for applications with predictable workloads and long-term requirements?**

- Serverless computing — Better for sporadic workloads.
- Spot instances — Better for flexible, short-term, interruptible workloads.
- Pay-as-you-go — Better for variable, short-term workloads.
- **Reserved instances** ✔️ *(Your answer — Correct)*
  Commit to fixed capacity for 1-3 years at a discount; ideal for predictable, long-term workloads.

**Domain:** Describe cloud computing

---

### Question 39 — ✅ Correct
**What is the primary purpose of Azure Data Box?**

- To monitor Azure resource usage. — Not related.
- To create and manage Azure virtual machines. — Not related.
- **To transfer large amounts of data to and from Azure.** ✔️ *(Your answer — Correct)*
- To build and deploy web applications in Azure. — Not related.

**Domain:** Describe Azure storage services

---

### Question 40 — ❌ Incorrect
**Can subscriptions be nested?**

- Yes — *(Your answer — Incorrect)*
- **No** ✔️ *(Correct answer)*
  Each subscription is a standalone, independent entity — not nestable.

**Domain:** Describe the core architectural components of Azure

---

### Question 41 — ❌ Incorrect
**Which compute type packages and deploys applications with their dependencies for consistent behavior across environments?**

- Virtual Machine — Offers consistency but heavier/more resource-intensive than containers.
- Serverless — Focused on running code without infrastructure management, not packaging dependencies.
- **Container** ✔️ *(Correct answer)*
  Lightweight, portable, packages app + dependencies for consistent behavior.
- Function — *(Your answer — Incorrect)* Event-driven code execution, not built for packaging dependencies.

**Domain:** Describe Azure compute and networking services

---

### Question 42 — ❌ Incorrect
**What is the maximum amount of data that can be stored in a single Azure Storage account?**

- There is no limit. — Incorrect; there is a limit.
- 5 Terabytes — *(Your answer — Incorrect)* Far below the actual limit.
- **5 Petabytes** ✔️ *(Correct answer)*
- 5 Gigabytes — Incorrect; far below the actual limit.

**Domain:** Describe Azure storage services

---

### Question 43 — ✅ Correct
**Which of the following are required in order to create an Azure Virtual Machine?** *(select all that apply)*

- **A resource group** ✔️ *(Your selection — Correct)*
- **A name for the VM** ✔️ *(Your selection — Correct)*
- **A virtual network** ✔️ *(Your selection — Correct)*
- **A subscription to Azure** ✔️ *(Your selection — Correct)*

**Domain:** Describe Azure compute and networking services

---

### Question 44 — ✅ Correct
**What is a key benefit of using Azure Budgets?**

- Automating resource provisioning. — Not the purpose of Budgets.
- Enforcing security policies. — Not the purpose of Budgets.
- **Setting spending limits and alerts.** ✔️ *(Your answer — Correct)*
- Optimizing virtual machine performance. — Not the purpose of Budgets.

**Domain:** Describe cost management in Azure

---

### Question 45 — ❌ Incorrect
**Queue storage is used for program-to-program communication. Which type of communication is this best suited for?**

- **Asynchronous communication** ✔️ *(Correct answer)*
  Decouples sender and receiver, letting them operate independently.
- Synchronous communication — *(Your answer — Incorrect)* Requires immediate interaction, not queue storage's use case.
- Real-time communication — Not the primary use case for queue storage.
- Broadcast communication (one-to-many) — Queue storage is point-to-point, not broadcast.

**Domain:** Describe Azure storage services

---

### Question 46 — ✅ Correct
**Fill in the blank: _________ is a cloud-based file sharing service that allows you to access your files from anywhere using standard SMB or NFS protocols.**

- **Azure File Storage** ✔️ *(Your answer — Correct)*
- General Purpose V2 — A storage account type, not specifically the file-sharing service itself.
- Azure Blob Storage — For unstructured data; not SMB/NFS file sharing.
- Azure Table Storage — NoSQL structured data store, unrelated to file sharing.

**Domain:** Describe Azure storage services

---

### Question 47 — ✅ Correct
**A large financial institution with strict compliance requirements would be best suited for which cloud model?**

- Community Cloud — Shared among orgs; not enough control for this scenario.
- Hybrid Cloud — Combines public/private but not the best fit for max control/security here.
- **Private Cloud** ✔️ *(Your answer — Correct)*
  Dedicated to a single organization; highest control, security, and customization.
- Public Cloud — Shared, third-party managed; insufficient control for this scenario.

**Domain:** Describe cloud computing

---

### Question 48 — ✅ Correct
**What does redundancy mean in the context of Azure?**

- Monitoring system health. — Related to reliability, not redundancy directly.
- Implementing failover to a secondary data center. — Related to disaster recovery, not the definition of redundancy itself.
- Using a single instance of a resource to avoid failures. — Opposite of redundancy.
- **Having multiple copies of a resource to ensure availability.** ✔️ *(Your answer — Correct)*

**Domain:** Describe the benefits of using cloud services

---

### Question 49 — ❌ Incorrect
**Autoscaling VMs based on need is an example of what type of manageability benefit?**

- Management in the cloud — *(Your answer — Incorrect)* Refers to HOW you manage resources (Portal, CLI, APIs), not this scenario.
- **Management of the cloud** ✔️ *(Correct answer)*
  Refers to managing your cloud resources themselves, e.g. setting up autoscaling rules.

**Domain:** Describe the benefits of using cloud services

---

### Question 50 — ✅ Correct
**Regularly auditing cloud resource usage for compliance with regulations/standards is an example of what practice?**

- Reactive Approach — Opposite; auditing is proactive, not reactive.
- **Governance** ✔️ *(Your answer — Correct)*
  Managing/controlling cloud resources in line with regulatory requirements and corporate standards.
- Reliability — Not directly related to compliance auditing.
- Scalability — Not directly related to compliance auditing.

**Domain:** Describe the benefits of using cloud services

---

## Summary of Missed Questions
| # | Topic | Correct Answer |
|---|-------|----------------|
| 7 | App Service Plan (Premium v3) app limit | Unlimited |
| 8 | 6 copies across 2 regions | GRS |
| 10 | Private on-prem to Azure connection | Azure ExpressRoute |
| 12 | Regional failover destination | Region pair (300+ miles, same geography) |
| 21 | High availability's financial benefit | Uninterrupted revenue generation |
| 24 | Rarely accessed data, 180+ day storage | Archive access tier |
| 25 | App needing Windows Registry access | IaaS |
| 31 | Microsoft Entra Domain Services benefit | Managed cloud domain service, no on-prem DCs needed |
| 37 | Adding resources to a pool | Horizontal scaling |
| 40 | Nested subscriptions | No |
| 41 | Packaging app + dependencies | Container |
| 42 | Max Azure Storage account size | 5 Petabytes |
| 45 | Program-to-program queue communication | Asynchronous communication |
| 49 | Autoscaling VMs manageability type | Management of the cloud |
