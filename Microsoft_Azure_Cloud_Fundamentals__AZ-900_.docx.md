**Microsoft Azure Cloud Fundamentals**

**AZ-900 Study Notes — Detailed English Edition**

*Complete coverage of all three exam domains, with AWS and GCP comparisons*

**Exam domains:** Domain 1 — Cloud Concepts (25–30%) · Domain 2 — Azure Architecture and Services (35–40%) · Domain 3 — Azure Management and Governance (30–35%)

# **Module 1: Describe Cloud Concepts**

## **What is Cloud Computing?**

### **Definition**

*Cloud computing is the delivery of computing services — servers, storage, databases, networking, software, and analytics — over the internet, so you use a provider’s infrastructure instead of your own local computer or datacenter, and pay only for what you use.*

**Simple example:** Your laptop has only 256 GB of storage. Instead of buying a bigger hard disk, you upload files to Azure Storage. Azure stores everything in Microsoft’s datacenters, replicated for safety, and you access it from anywhere at any time. That is cloud computing.

**Key idea:** The cloud turns computing into a utility, like electricity. You don’t build a power plant to light your house; you plug in and pay for what you consume.

### **Traditional (On-Premises) vs Cloud**

| On-Premises | Cloud |
| :---- | :---- |
| You buy and own servers | You rent Microsoft’s servers |
| Large upfront hardware purchase | Pay-as-you-go pricing |
| You handle maintenance, cooling, power | Azure handles the physical infrastructure |
| Scaling requires buying more hardware (weeks/months) | Scaling takes minutes in the portal |
| Capacity is fixed — often over- or under-provisioned | Capacity matches demand |

**Example — a company needs 100 servers:**

| Step | On-Premises | Azure |
| :---- | :---- | :---- |
| 1 | Purchase servers (weeks of procurement) | Log in to the Azure portal |
| 2 | Install Windows/Linux on each | Create VMs from images |
| 3 | Set up cooling and power | Done in minutes |
| 4 | Configure networking and security | Azure manages the hardware layer |
| 5 | Plan backups and maintenance | Built-in backup and update options |

*On-premises: the company manages everything. Azure: Microsoft manages the hardware; you manage what you build on top.*

### **Why Cloud? Core Business Drivers**

| Benefit | What it means in practice |
| :---- | :---- |
| Fast deployment | Provision resources in minutes instead of weeks; test ideas the same day |
| Lower entry cost | No upfront hardware investment; a startup can begin with almost zero capital |
| High availability | Redundant infrastructure keeps services online through failures |
| Disaster recovery | Replicate to another region; recover quickly from major outages |
| Global reach | Deploy close to users on any continent from a single portal |
| Focus on the business | Engineers build products instead of maintaining hardware |

## **Cloud Service Models (IaaS, PaaS, SaaS)**

The three service models differ in **how much the provider manages versus how much you manage**. Moving from IaaS → PaaS → SaaS, the provider’s responsibility increases and yours decreases.

### **1\. IaaS — Infrastructure as a Service**

The provider gives you the raw building blocks: virtual machines, storage, and networking. You control everything from the operating system upward.

| Azure provides | You manage |
| :---- | :---- |
| Virtual machines (compute) | Operating system and OS patching |
| Storage and disks | Runtime, middleware, applications |
| Virtual networking | Data, access control, in-guest security |
| Physical datacenter, hosts, hypervisor | Backup strategy for your workloads |

**When to use IaaS:** lift-and-shift migrations (move servers as-is), workloads needing full OS control, custom or legacy software, and test environments that mirror on-premises setups.

**Trade-off:** maximum flexibility, but maximum operational responsibility — you patch, you secure the OS, you configure everything inside the VM.

| Azure | AWS | GCP |
| :---- | :---- | :---- |
| Azure Virtual Machines | EC2 | Compute Engine |

*Example: Create an Ubuntu VM → install Apache → deploy a website. Everything inside the VM is your responsibility, including security updates.*

### **2\. PaaS — Platform as a Service**

The provider manages the infrastructure **and** the operating system, runtime, and middleware. You bring only your application code and data.

| Azure manages | You do |
| :---- | :---- |
| Hardware, networking, datacenter | Write and deploy your code |
| Operating system and patching | Configure the application and scaling rules |
| Runtime (e.g., .NET, Python, Node.js) | Manage your data and user access |

**When to use PaaS:** web applications and APIs where the team wants to focus on code, rapid development with built-in scaling, CI/CD integration, and no desire to maintain servers.

**Trade-off:** far less operational work, but less control — you accept the platform’s supported runtimes and configuration surface.

| Azure | AWS | GCP |
| :---- | :---- | :---- |
| Azure App Service | Elastic Beanstalk | App Engine |

*Example: Upload a Python app to App Service. Azure installs the runtime, patches the OS, scales instances, and load-balances traffic — no server management needed.*

### **3\. SaaS — Software as a Service**

The provider manages everything, including the application itself. You simply sign in and use the software, typically on a subscription.

| Microsoft | AWS | Google |
| :---- | :---- | :---- |
| Outlook / Exchange Online | Amazon WorkMail | Gmail |
| Microsoft 365 (Word, Excel) | — (Salesforce is a 3rd-party example) | Google Workspace |
| Microsoft Teams | Amazon Chime | Google Chat / Meet |

**When to use SaaS:** email, collaboration, CRM — standard business software where building or hosting your own adds no value.

**Trade-off:** zero infrastructure work, but the least control — features, release schedule, and data handling are set by the vendor.

### **Quick Comparison**

|  | IaaS | PaaS | SaaS |
| :---- | :---- | :---- | :---- |
| Your control | Maximum (OS upward) | Medium (code and config) | Minimum (settings only) |
| Your effort | Highest | Medium | Lowest |
| Typical user | IT administrators | Developers | End users |
| Memory hook | “Infrastructure — I get a server” | “Platform — I deploy code” | “Software — I just use it” |

### **Serverless Computing**

*Servers still exist, but they are completely abstracted away. You write code or logic; the platform runs it, scales it automatically (including down to zero), and bills you only for actual executions.*

| Aspect | Detail |
| :---- | :---- |
| You provide | Code (Functions) or workflow logic (Logic Apps) |
| Azure manages | Servers, OS, runtime, scaling — everything |
| Billing | Per execution / consumption; idle \= free (“scale to zero”) |
| Azure services | Azure Functions (code-first), Azure Logic Apps (designer-first) |
| AWS equivalents | Lambda, Step Functions |

*Example: A photo upload triggers a Function that generates a thumbnail and exits. There is no charge while the system is idle.*

## **The Shared Responsibility Model**

Security and operations are **shared** between Microsoft and the customer. Where the line sits depends on the service model.

| Service model | Microsoft is responsible for | Customer is responsible for |
| :---- | :---- | :---- |
| On-premises | Nothing | Everything |
| IaaS | Physical datacenter, hosts, network, hypervisor | OS and patching, network controls (NSGs, in-guest firewall), applications, identity, data |
| PaaS | The above \+ OS, runtime, middleware | Applications, application configuration, identity, data |
| SaaS | Almost everything, including the application | Users and accounts, devices, data, access settings |

### **Always the customer’s responsibility — in every model**

1. **Data** — its classification, protection, and appropriate use.

2. **Accounts and identities** — passwords, MFA, who has access.

3. **Devices/endpoints** — the laptops and phones that connect.

### **Always Microsoft’s responsibility — in every model**

Physical datacenter security, physical hosts and hardware, and the physical network — the customer never manages these in any cloud model.

### **Scenario practice**

| Scenario | Responsible party |
| :---- | :---- |
| You create an Azure VM and never patch it | Customer |
| A weak VM password is guessed by an attacker | Customer |
| A disk fails inside an Azure datacenter | Microsoft |
| Datacenter physical security is breached | Microsoft |
| Sensitive data is shared with the wrong user in Microsoft 365 | Customer |

**Exam tip:** *Microsoft secures the cloud; customers secure what they put in the cloud.* As you move IaaS → PaaS → SaaS, Microsoft’s share grows and yours shrinks — but data, identities, and devices are always yours.

## **Benefits of Cloud Computing (Detailed)**

### **High Availability (HA)**

The service stays operational with minimal downtime, even when individual components fail. Achieved through redundancy: multiple VMs behind a load balancer, zone-redundant deployments, health probes that route around failures. Expressed in uptime percentages (see SLA section).

### **Scalability**

The ability to increase or decrease resources to match workload.

| Type | Also called | What happens | Example |
| :---- | :---- | :---- | :---- |
| Vertical scaling | Scale up / scale down | Make one machine bigger or smaller (CPU/RAM) | Resize a VM from 16 GB to 64 GB RAM |
| Horizontal scaling | Scale out / scale in | Add or remove instances | Go from 4 web servers to 40, then back |

**Note:** vertical scaling has a hard ceiling (a single machine can only get so big); horizontal scaling is how cloud applications grow almost without limit. Stateless workloads behind a load balancer scale out best.

### **Elasticity**

Scalability performed **automatically** in response to demand — the system grows during spikes and shrinks afterward without human action, so you never pay long-term for peak capacity. *Scalability is the ability; elasticity is doing it automatically.*

*Example: 100 users in the morning, 10,000 in the evening — autoscale adds VMs for the evening rush and removes them at night. You pay only for what ran.*

### **Reliability**

The ability of a system to recover from failures and continue functioning. Cloud platforms achieve this through decentralized design — multiple datacenters, zones, and regions — so a failure in one place does not take the whole system down.

### **Predictability**

Two kinds, both exam-relevant:

* **Performance predictability** — autoscaling, load balancing, and HA design keep the customer experience consistent under changing load.

* **Cost predictability** — tools like the Pricing Calculator, TCO Calculator, and Cost Management let you forecast and track spend before and after deployment.

### **Security and Governance**

Cloud providers offer certified datacenters, encryption, DDoS protection, and identity management out of the box, plus governance tooling (Azure Policy, RBAC, Blueprints-style templates) that keeps deployments compliant with organizational standards — often stronger than what a single company could build alone.

### **Manageability**

* **Management OF the cloud** — managing your cloud resources: autoscaling rules, template-based deployment, monitoring and alerting, self-healing configuration.

* **Management IN the cloud** — the tools you use to do it: Azure portal, CLI, PowerShell, APIs, mobile app.

## **High Availability vs Fault Tolerance vs Disaster Recovery**

| Concept | Goal | Downtime | Example |
| :---- | :---- | :---- | :---- |
| High Availability | Minimize downtime from component failures | Seconds to minutes | Load balancer \+ multiple VMs |
| Fault Tolerance | Survive component failure with **zero** downtime | None | Redundant components serving live in parallel |
| Disaster Recovery | Restore service after a major outage (region loss, catastrophe) | Measured by RTO | Failover to a replica in a second region |

### **RPO vs RTO (exam favourite)**

| Term | Question it answers | Memory hook |
| :---- | :---- | :---- |
| RPO — Recovery Point Objective | How much **data** loss is acceptable (time since last good copy)? | “Point” \= data point |
| RTO — Recovery Time Objective | How quickly must service be **restored**? | “Time” \= downtime |

*Example: RPO of 1 hour means backups/replication must never be more than 1 hour behind. RTO of 4 hours means the business must be running again within 4 hours of a disaster.*

## **Service Level Agreements (SLAs)**

An SLA is Microsoft’s formal commitment to a level of uptime or performance, with service credits if it is not met.

| SLA % | Downtime per month (approx.) | Downtime per year (approx.) |
| :---- | :---- | :---- |
| 99% | \~7.3 hours | \~3.65 days |
| 99.9% | \~43.8 minutes | \~8.8 hours |
| 99.95% | \~21.9 minutes | \~4.4 hours |
| 99.99% | \~4.4 minutes | \~52.6 minutes |

### **Composite SLAs**

* **Services in series multiply — and the result is LOWER.** App (99.95%) \+ database (99.9%) → 0.9995 × 0.999 ≈ **99.85%**, worse than the weakest link.

* **Redundancy in parallel raises effective availability.** Two independent instances where either can serve means both must fail simultaneously for an outage.

### **Azure VM SLA ladder (memorize)**

| Deployment | SLA |
| :---- | :---- |
| Single VM (Premium SSD or better) | 99.9% |
| 2+ VMs in an Availability Set | 99.95% |
| 2+ VMs across Availability Zones | 99.99% |

## **CapEx vs OpEx and the Consumption Model**

| CapEx (Capital Expenditure) | OpEx (Operational Expenditure) |
| :---- | :---- |
| Large upfront investment in physical assets | Ongoing payment for services as consumed |
| Example: buy servers, storage, routers | Example: monthly Azure VM bill |
| Cost is fixed whether or not capacity is used | Stop the resource → stop paying (compute) |
| Depreciated over years on the books | Expensed as used; scales with the business |

**The consumption-based model** means: no upfront infrastructure purchase, no paying for unused capacity, pay only for what you use, and stop paying when you deprovision. This is why cloud spend is OpEx.

**Watch-outs:** costs are ongoing and can grow unnoticed; egress bandwidth, forgotten resources, and idle VMs are classic bill surprises (covered in Module 3).

## **Cloud Deployment Models**

| Model | Description | Best for / Examples |
| :---- | :---- | :---- |
| Public cloud | Provider-owned, shared (multi-tenant) infrastructure available to anyone over the internet; logical isolation between customers | Most workloads; startups to enterprises — Azure, AWS, GCP |
| Private cloud | Cloud-style infrastructure dedicated to **one** organization; can be in your datacenter or hosted by a third party — “private” means dedicated, not on-site | Banks, defense, strict compliance needs |
| Hybrid cloud | Public \+ private/on-premises connected so data and apps move between them | Keep sensitive data on-prem, run the website in Azure; “cloud bursting” for demand spikes |
| Multi-cloud | Using two or more public providers | Avoiding vendor lock-in, best-of-breed services — Azure \+ AWS |

**Comparing trade-offs:** public cloud has the lowest upfront cost and least control over hardware; private has the highest cost and most control; hybrid balances the two at the price of added complexity.

**Data sovereignty / residency:** laws in many countries require certain data to remain physically within national borders. This drives region selection (Module 2\) and sometimes private/hybrid choices.

# **Module 2: Describe Azure Architecture and Services**

## **Azure Global Infrastructure**

### **The physical hierarchy**

***Geography → Region → Availability Zone → Datacenter***

| Concept | Description | Exam points |
| :---- | :---- | :---- |
| Geography | A discrete market (e.g., India, Europe, United States) usually containing two or more regions; preserves **data residency and compliance** boundaries | Choose for legal/compliance reasons |
| Region | A set of datacenters in one area (Central India, East US, West Europe) connected by low-latency networks | Not every service is available in every region |
| Availability Zone | One or more **physically separate** datacenters within a region, each with independent power, cooling, and networking, linked by private fiber | Protects against **datacenter-level** failure; not all regions have zones (those that do have a minimum of three) |
| Region pair | Two regions in the same geography paired for disaster recovery; platform updates roll out to paired regions **sequentially**, never both at once | Protects against **region-level** failure |
| Sovereign clouds | Physically and logically isolated Azure instances | Azure Government (US), Azure China (operated by 21Vianet) |

### **Zonal vs zone-redundant services**

* **Zonal:** you pin the resource to a specific zone (e.g., a VM in Zone 1).

* **Zone-redundant:** the platform replicates automatically across zones (e.g., ZRS storage, zone-redundant load balancer).

### **How to choose a region**

1. **Latency** — closest to your users.

2. **Service availability** — confirm the services you need exist there.

3. **Compliance/data residency** — legal requirements on where data lives.

4. **Price** — the same VM can cost different amounts in different regions.

## **Organizing Resources: The Management Hierarchy**

***Management Group → Subscription → Resource Group → Resource***

| Level | Purpose | Key rules |
| :---- | :---- | :---- |
| Management group | Governs many subscriptions together; policies and role assignments applied here **inherit downward** | Can be nested into a hierarchy (e.g., Prod / Non-Prod) |
| Subscription | The unit of **billing** and an access-management boundary; has quotas/limits (e.g., cores per region) | Each subscription trusts exactly **one** Microsoft Entra tenant; one tenant can have many subscriptions |
| Resource group | A logical container for related resources sharing a lifecycle | **Deleting the group deletes everything inside.** Resources can’t be in two groups; groups cannot be nested; members may live in **different regions** than the group |
| Resource | The actual service instance — VM, storage account, VNet | Can be **moved** between groups and subscriptions later |

**Exam traps:** the resource group’s “region” only stores its metadata — a group in East US can contain a VM in West Europe. Tags and locks applied to a group affect resources inside (locks inherit; tags do **not** inherit by default).

## **Azure Compute Services (Detailed)**

### **Azure Virtual Machines (IaaS)**

Full OS-level control. You choose the **image** (OS \+ optional pre-installed software), the **size/series** (general purpose, compute-optimized, memory-optimized, GPU), the **disk type**, and the **pricing option**. You are responsible for everything inside the guest OS.

**Price is driven by:** size/series, region, OS licensing, running hours, and pricing model (pay-as-you-go, reserved, spot).

### **Availability options for VMs**

| Option | Protects against | How |
| :---- | :---- | :---- |
| Availability Set | Failures **within one datacenter** | Spreads VMs across **fault domains** (separate racks/power/network) and **update domains** (separate planned-maintenance reboot batches) — SLA 99.95% |
| Availability Zones | **Datacenter** failure | VMs placed in physically separate zones — SLA 99.99% |
| Multi-region | **Region** failure | Replicate/failover to a paired or second region |

*Memory hook: Fault domain \= different rack and power (hardware protection). Update domain \= different reboot batch (maintenance protection).*

### **VM Scale Sets**

Deploy and manage a group of **identical, load-balanced VMs** that scale automatically based on metrics (CPU), a schedule, or manually. The standard answer for “many identical VMs with autoscaling.”

### **Azure App Service (PaaS)**

Host web apps, APIs, and mobile backends without managing servers. Supports .NET, Java, Node.js, Python, PHP on Windows or Linux, and containers. Notable features: built-in autoscale, CI/CD integration, and **deployment slots** — stage a new version in production infrastructure, then **swap** it live with near-zero downtime.

### **Azure Functions vs Logic Apps (both serverless)**

|  | Azure Functions | Azure Logic Apps |
| :---- | :---- | :---- |
| Approach | **Code-first** — developers write functions | **Designer-first** — drag-and-drop workflows |
| Triggered by | HTTP, timers, queue messages, blob uploads, events | 1,000+ connectors (email arrives, file created, tweet posted) |
| Best for | Event-driven code, APIs, background processing | Business process automation and integration |
| Consumption-plan notes | Pay per execution; scales to zero; has execution time limits and cold starts | Pay per action/connector run |

### **Containers: ACI vs AKS**

|  | Azure Container Instances (ACI) | Azure Kubernetes Service (AKS) |
| :---- | :---- | :---- |
| What | Run a container **instantly**, no cluster, per-second billing | Managed **Kubernetes** orchestration |
| Best for | Simple jobs, burst workloads, quick tasks | Microservices at scale: self-healing, rolling updates, service discovery |
| Rule of thumb | One container, fast and simple → ACI | Many containers needing orchestration → AKS |

*Containers vs VMs: containers virtualize the OS and share the host kernel — lightweight, fast-starting, portable. VMs virtualize hardware and each carries a full guest OS.*

### **Other compute services**

| Service | Use case | AWS equivalent |
| :---- | :---- | :---- |
| Azure Virtual Desktop | Stream Windows desktops/apps from the cloud to any device; multi-session Windows lets many users share one VM (cost saving) | Amazon WorkSpaces |
| Azure Dedicated Host | Physical servers reserved for your organization alone — compliance and licensing isolation | EC2 Dedicated Host |
| Spot VMs | Deep discounts on spare capacity; Azure can **evict at any time** — only for interruptible work (batch, rendering, test) | Spot Instances |
| Azure Batch | Large-scale parallel and HPC jobs with managed VM pools | AWS Batch |

## **Azure Networking Services (Detailed)**

### **Virtual Network (VNet) and subnets**

A VNet is your private network in Azure, **scoped to one region** (it can span that region’s zones). You divide it into **subnets** (IP ranges) to segment tiers — web subnet, app subnet, database subnet. Subnets in the same VNet route to each other by default; NSGs control what is actually allowed.

### **Network Security Groups (NSGs)**

Allow/deny rules filtering traffic by source/destination IP, port, and protocol. Attached to **subnets or NICs**.

* Rules are processed by **priority number — lower numbers first; first match wins**.

* Defaults: VNet-internal traffic and load-balancer probes are allowed; unsolicited inbound from the internet is denied.

* Never expose management ports (RDP **3389**, SSH **22**) to the internet — use Bastion instead.

### **NSG vs Azure Firewall**

|  | NSG | Azure Firewall |
| :---- | :---- | :---- |
| Nature | Basic packet filter attached to subnets/NICs | Managed, **stateful** firewall service |
| Features | 5-tuple allow/deny rules | FQDN filtering, threat intelligence, centralized rules across VNets |
| Analogy | A guard with a checklist at each door | A professional security operations gate for the whole estate |

*“Stateful” means return traffic for an allowed outbound connection is automatically permitted.*

### **Connecting networks**

| Service | Connects | Key facts |
| :---- | :---- | :---- |
| VNet peering | VNet ↔ VNet | Private traffic over the **Microsoft backbone** (never the internet); works across regions (“global peering”), subscriptions, and tenants; address spaces must **not overlap** |
| Site-to-site VPN | Entire on-prem network ↔ Azure VNet | Encrypted IPsec tunnel **over the public internet** via a VPN device and VPN Gateway |
| Point-to-site VPN | One client device ↔ Azure VNet | For individual remote workers |
| ExpressRoute | On-prem ↔ Azure | **Private dedicated circuit** via a connectivity provider; traffic never touches the public internet; consistent latency and high bandwidth; commonly paired with a VPN as **failover** |

### **Other networking services**

| Service | Purpose |
| :---- | :---- |
| Azure DNS | Host public DNS zones (point your registrar’s NS records at Azure) and **Private DNS zones** for names inside VNets |
| Azure Bastion | Secure RDP/SSH to VMs **through the portal over TLS** — no public IPs, no exposed ports |
| NAT Gateway | Outbound-only internet access for a subnet without public IPs on VMs |
| DDoS Protection | Infrastructure-level protection is **built in and free** for all of Azure; a paid tier adds tuned mitigation, telemetry, and rapid response |

### **The Load-Balancing Family (very important)**

| Service | Layer | Scope | Use it for |
| :---- | :---- | :---- | :---- |
| Azure Load Balancer | Layer 4 (TCP/UDP) | Regional | Distributing traffic across VMs; internal (tier-to-tier) or public |
| Application Gateway | Layer 7 (HTTP) | Regional | URL-path routing (/images → pool A, /api → pool B), SSL offload, **WAF** |
| Azure Front Door | Layer 7 (HTTP) | **Global** | Edge acceleration, global failover, caching/CDN, **WAF** |
| Traffic Manager | DNS | Global | DNS-based routing (priority, weighted, performance, geographic) — it directs clients but never touches the traffic itself |

**Memory hook:** *LB \= TCP, regional. App Gateway \= HTTP, regional. Front Door \= HTTP, global. Traffic Manager \= DNS only.*

**WAF (Web Application Firewall):** available on Application Gateway and Front Door; protects web apps from attacks like SQL injection and cross-site scripting.

## **Azure Storage Services (Detailed)**

### **Storage accounts**

The container for Azure Storage data services. The account name must be **globally unique** because it forms the public endpoint URL (e.g., name.blob.core.windows.net). Data at rest is **encrypted by default** (Storage Service Encryption). Performance tiers: **Standard** (HDD-backed pricing) and **Premium** (SSD, low latency).

### **The core data services**

| Service | Stores | Typical use | AWS equivalent |
| :---- | :---- | :---- | :---- |
| Blob Storage | Unstructured objects | Images, video, backups, logs, data lakes, static websites | S3 |
| Azure Files | Managed **SMB/NFS file shares** | Mapped network drives; lift-and-shift apps expecting \\\\server\\share; sync with on-prem via **Azure File Sync** | EFS / FSx |
| Queue Storage | Messages | Asynchronous communication that **decouples** application components | SQS |
| Table Storage | NoSQL key/attribute data | Large volumes of structured, non-relational data | DynamoDB (basic) |
| Managed Disks | Block storage | OS and data disks for VMs | EBS |

### **Blob types**

| Type | Optimized for | Example |
| :---- | :---- | :---- |
| Block blobs | General object upload/download | Documents, media files |
| Append blobs | Add-to-the-end writes | Log files |
| Page blobs | Random read/write | VM disks (VHDs) |

### **Blob access tiers**

| Tier | Storage cost | Access cost | Intended for |
| :---- | :---- | :---- | :---- |
| Hot | Highest | Lowest | Frequently accessed data |
| Cool | Lower | Higher | Infrequent access; store ≥ 30 days |
| Cold | Lower still | Higher still | Rare access; store ≥ 90 days |
| Archive | Lowest | Highest \+ **rehydration delay of hours** | Compliance/long-term; store ≥ 180 days; **not readable until rehydrated** |

**Lifecycle management** can automatically move blobs between tiers by age (e.g., to Cool after 30 days, Archive after 180).

### **Managed disk performance ladder**

Standard HDD \< Standard SSD \< Premium SSD \< **Ultra Disk** (highest IOPS/lowest latency, for demanding databases).

### **Storage redundancy — “where are my copies?”**

| Option | Copies | Protects against | Note |
| :---- | :---- | :---- | :---- |
| LRS | 3 in one datacenter | Hardware failure | Cheapest |
| ZRS | 3 across three zones | Datacenter failure | Data **stays in the region** — the answer when residency \+ zone resilience are both required |
| GRS | 3 primary \+ 3 in the paired region | Region failure | Geo-copy is **asynchronous** (a small RPO exists) |
| RA-GRS | GRS \+ read access to secondary | Region failure | You can read from the secondary at all times |
| GZRS / RA-GZRS | ZRS in primary \+ geo-copy | Zone **and** region failure | Highest durability |

### **Moving data to Azure**

| Tool | Use when |
| :---- | :---- |
| Azure Migrate | Central hub to **assess** and migrate on-prem servers, databases, and web apps |
| AzCopy | Command-line bulk copy to/from storage over the network (scriptable) |
| Azure Storage Explorer | Desktop GUI to browse and manage storage |
| Azure Data Box | **Ship data physically** (Disk / standard / Heavy variants) when volume is huge or bandwidth is poor — e.g., 400 TB in two weeks |
| Azure File Sync | Keep on-prem Windows file servers as a fast cache **synchronized** with Azure Files |

**Rule of thumb:** huge data \+ weak bandwidth \+ deadline → Data Box. Regular scripted network transfer → AzCopy.

## **Identity, Access, and Security (Detailed)**

### **Microsoft Entra ID (formerly Azure AD)**

Azure’s cloud-based identity and access management service — it handles **authentication** (proving who you are) and supports **authorization** (what you may do). Unlike on-premises Active Directory (Kerberos, OUs, domain controllers you manage), Entra ID is a managed service using modern protocols (OAuth, SAML, OpenID Connect) and works with apps anywhere, not just in Azure.

| Feature | What it does |
| :---- | :---- |
| Single sign-on (SSO) | Sign in once, access many applications without re-entering credentials |
| Entra Connect | Synchronizes on-premises AD identities to Entra ID — **hybrid identity**, one identity for both worlds |
| Entra Domain Services | Managed domain join, LDAP, Kerberos/NTLM for **legacy apps** — without you running domain controllers |
| External ID — B2B | Invite partner/guest users who sign in with **their own** credentials |
| External ID — B2C | Customer identity for your public-facing apps, including social logins |

### **Strengthening sign-in**

| Feature | Detail |
| :---- | :---- |
| MFA | Requires two or more proofs: something you know (password), have (phone/key), or are (biometric). Mitigates stolen-password attacks |
| Passwordless | Windows Hello, FIDO2 security keys, Microsoft Authenticator — stronger and more convenient than passwords |
| Conditional Access | Policy engine: evaluates **signals** (user/group, location/IP, device state, application, detected risk) and then allows, blocks, or requires MFA. Example: “Finance app from outside the office → require MFA” |
| Entra ID Protection (P2) | Detects risky sign-ins and compromised credentials (e.g., leaked in a breach) and can respond automatically |
| PIM — Privileged Identity Management (P2) | **Just-in-time, time-bound, approval-based** activation of admin roles instead of standing privileges |
| Access reviews | Periodic recertification: “does this user still need this role?” |

**Entra ID licensing:** Free tier \= core identity/SSO. **P1 adds Conditional Access. P2 adds PIM and Identity Protection.**

### **Azure RBAC (Role-Based Access Control)**

Controls **who** can do **what** at **which scope**. An assignment \= security principal (user/group/app) \+ role definition \+ scope (management group, subscription, resource group, or resource). Assignments **inherit downward**; access is **deny-by-default** (no role \= no access).

| Built-in role | Can | Cannot |
| :---- | :---- | :---- |
| Owner | Everything, including granting access | — |
| Contributor | Create/manage all resources | Assign roles to others |
| Reader | View everything | Change anything |
| User Access Administrator | Manage role assignments | Manage resources |

**Exam trap:** Entra **directory roles** (like Global Administrator) and Azure **RBAC roles** are separate systems. A Global Administrator does **not** automatically have RBAC access to Azure resources — they must explicitly elevate access.

### **Protecting secrets and workloads**

| Service | Purpose |
| :---- | :---- |
| Azure Key Vault | Securely store **secrets, encryption keys, and certificates**; apps fetch them at runtime instead of hardcoding |
| Managed identities | Give an app an automatic identity so it can authenticate to Azure services **without any stored credentials** — pairs perfectly with Key Vault |
| Microsoft Defender for Cloud | **Cloud security posture management**: continuously assesses resources, produces a **Secure Score**, recommends fixes, and adds workload protection — covers Azure **plus hybrid and multicloud (AWS/GCP)** |
| Microsoft Sentinel | Cloud-native **SIEM \+ SOAR**: collects security data at scale, detects threats, supports investigation, and automates response with playbooks. Workflow: **collect → detect → investigate → respond** |

### **Security models to memorize**

**Zero Trust — three principles:**

1. **Verify explicitly** — authenticate and authorize every request using all available signals.

2. **Use least-privilege access** — grant only what is needed, just-in-time where possible.

3. **Assume breach** — segment networks, encrypt, and monitor as if an attacker is already inside.

**Defense in depth — layer order (outermost → innermost):**

***Physical security → Identity & access → Perimeter → Network → Compute → Application → Data***

Each layer independently slows an attacker: datacenter guards, MFA and RBAC, DDoS protection, NSGs/firewalls, hardened VMs, secure code and Key Vault, encryption of data.

**Encryption everywhere:** at rest (Storage Service Encryption, disk encryption), in transit (TLS/HTTPS), and in use (confidential computing — protecting data while processed in memory).

# **Module 3: Describe Azure Management and Governance**

## **Cost Management (Detailed)**

### **What drives your Azure bill**

| Factor | Detail |
| :---- | :---- |
| Resource type & size | A D16s VM costs far more than a D2s; Premium SSD more than Standard HDD |
| Consumption | Hours run, GB stored, operations performed |
| Region | The **same** resource is priced differently in different regions |
| Bandwidth | **Ingress (inbound) is free; egress (outbound) is charged** — internet-bound and often cross-region traffic |
| Pricing model | Pay-as-you-go vs reservations vs savings plan vs spot |
| Extras people forget | Unattached disks, idle public IPs, forgotten test resources |

### **Cost tools — before vs after deployment**

| Tool | When | Purpose |
| :---- | :---- | :---- |
| Pricing Calculator | **Before** deployment | Estimate the monthly cost of a proposed architecture |
| TCO Calculator | **Before** migration | Compare current on-premises costs (servers, storage, labor, power) with Azure — the CFO conversation |
| Cost Analysis (Cost Management) | **After** deployment | Explore actual spend by service, region, resource group, or **tag**; trend over time |
| Budgets \+ alerts | Ongoing | Notify when spend crosses thresholds — alerts **inform only**; they don’t stop resources unless you add automation |

### **Ways to reduce cost**

| Option | How it saves |
| :---- | :---- |
| Reservations | Commit to 1 or 3 years of a resource for large discounts — for steady, predictable workloads |
| Savings plan for compute | Commit to an hourly **spend** amount, flexible across compute services and regions |
| Spot VMs | Cheapest compute; can be evicted — batch/interruptible only |
| Azure Hybrid Benefit | Reuse existing on-prem Windows Server / SQL Server licenses (with Software Assurance); **stacks with reservations** |
| Auto-shutdown / deallocate | Stop dev/test VMs off-hours. **Only “Stopped (deallocated)” stops compute billing** — shutting down from inside the OS keeps the hardware reserved and billed. Disks still bill either way |
| Right-sizing | Follow Advisor’s recommendations to shrink or remove underused VMs |
| Tags for chargeback | A CostCenter tag on every resource lets Cost Analysis split the bill by department |

## **Governance and Compliance (Detailed)**

### **Azure Policy — the WHAT**

Enforces organizational rules on resources: allowed regions, allowed VM SKUs, required tags, mandatory encryption. Evaluates **new deployments and existing resources**, showing results on a compliance dashboard.

| Effect | Behavior |
| :---- | :---- |
| Deny | Blocks the non-compliant deployment entirely |
| Audit | Allows it, but flags non-compliance |
| Append / Modify | Adds required properties (e.g., a tag) during creation |
| DeployIfNotExists | Automatically deploys a missing companion resource (e.g., a monitoring agent) — automated remediation |

An **initiative** is a group of related policies assigned as one unit. Assign at the **management group** level to cover many subscriptions at once; **exemptions** can exclude a specific scope without unassigning the policy.

### **Azure Policy vs RBAC (the most-tested distinction)**

*Policy controls **WHAT** can be done with resources. RBAC controls **WHO** can perform actions.*

### **Resource locks**

| Lock | Blocks |
| :---- | :---- |
| CanNotDelete | Deletion (modification still allowed) |
| ReadOnly | Modification **and** deletion |

Locks apply to **everyone, including Owners** — the lock must be removed first (itself an audited action). Locks on a resource group are **inherited** by everything inside. Caution: ReadOnly can break operations that look like reads but require write/list permissions (e.g., listing storage account keys).

### **Tags**

Name:value metadata (Environment: Production, CostCenter: Marketing) used for organization, automation, and cost reporting. Tags are **not inherited** from resource groups by default — use an Azure Policy to enforce or inherit them.

### **Compliance resources**

| Resource | Purpose |
| :---- | :---- |
| Microsoft Purview | Unified **data governance** — discover, classify, and map data (and its lineage) across the estate |
| Service Trust Portal | Microsoft’s audit reports, compliance documentation, and penetration-test results — what you show auditors |
| Microsoft Trust Center | Public information on Microsoft’s security, privacy, and compliance practices and certifications (ISO 27001, SOC, GDPR) |

## **Tools for Managing and Deploying Resources**

| Tool | Type | Notes |
| :---- | :---- | :---- |
| Azure portal | Web GUI | Great for exploring and one-off tasks; manual steps don’t scale or repeat reliably |
| Azure CLI | Command line | Commands start with az (e.g., az vm create); cross-platform, Bash-friendly |
| Azure PowerShell | Cmdlets | Verb-AzNoun format (e.g., New-AzVM); PowerShell 7 runs on any OS |
| Azure Cloud Shell | Browser terminal | Pre-authenticated; offers **both** Bash/CLI and PowerShell; persists files via an Azure Files share |
| Azure mobile app | iOS/Android | Monitor health, view alerts, run Cloud Shell, quick management actions |
| ARM templates | Declarative JSON | Describe the **desired end state**; deployments are **idempotent** (repeat deploys converge to the same state, no duplicates) |
| Bicep | Declarative language | Cleaner syntax that **compiles to ARM JSON** — Microsoft’s recommended IaC |
| Terraform | Third-party IaC | Fully supported for managing Azure |
| Azure Arc | Hybrid/multicloud management | Project **on-premises and AWS/GCP servers** into Azure so Policy, RBAC, tags, and monitoring apply to them like native resources |

**Everything goes through Azure Resource Manager (ARM):** portal, CLI, PowerShell, SDKs, and templates all call the same management layer, which enforces RBAC, policy, locks, and tags consistently.

**Declarative vs imperative:** declarative \= describe the end state (templates/Bicep); imperative \= list the steps (scripts). Declarative IaC in version control gives repeatable, reviewable, drift-correcting environments (dev \= test \= prod).

## **Monitoring Tools (Detailed)**

| Tool | The question it answers |
| :---- | :---- |
| Azure Monitor — Metrics | “What is this VM’s CPU right now?” — numeric time-series, near-real-time charts |
| Azure Monitor — Logs (Log Analytics) | “What’s the pattern in these errors?” — rich records queried with **KQL** in a Log Analytics workspace |
| Activity log | “**Who** deleted the VM on Saturday?” — control-plane operations (create/modify/delete) |
| Application Insights | “Why is the web app slow? Where are exceptions happening?” — request rates, response times, failures, dependencies |
| Alerts \+ action groups | “When CPU \> 90% for 10 minutes, email on-call **and** trigger a Function/webhook/runbook” |
| Azure Advisor | Personalized best-practice recommendations in **five categories: Cost, Security, Reliability, Performance, Operational Excellence** (security items come from Defender for Cloud) |
| Azure Service Health | “Is **Azure itself** having an outage or planned maintenance that affects me?” — supports proactive health alerts |
| Resource Health | “Is **my specific resource** healthy?” |
| Dashboards & Workbooks | Pin metrics, costs, and alerts into shared at-a-glance views; Workbooks add interactive reports over log queries |

## **Azure ↔ AWS ↔ GCP Service Mapping (Consolidated)**

| Azure | AWS | GCP |
| :---- | :---- | :---- |
| Virtual Machines | EC2 | Compute Engine |
| VM Scale Sets | Auto Scaling Groups | Managed Instance Groups |
| App Service | Elastic Beanstalk | App Engine |
| Azure Functions | Lambda | Cloud Functions |
| AKS | EKS | GKE |
| Virtual Network | VPC | VPC |
| Azure DNS | Route 53 | Cloud DNS |
| ExpressRoute | Direct Connect | Cloud Interconnect |
| Blob Storage | S3 | Cloud Storage |
| Azure Files | EFS / FSx | Filestore |
| Managed Disks | EBS | Persistent Disk |
| Entra ID | IAM / Identity Center | Cloud IAM |
| Key Vault | Secrets Manager / KMS | Secret Manager / KMS |
| Azure Monitor | CloudWatch | Cloud Monitoring |
| Activity Log | CloudTrail | Cloud Audit Logs |
| ARM / Bicep | CloudFormation | Deployment Manager |
| Azure Policy | Config Rules / SCPs | Organization Policy |
| Cost Management | Cost Explorer | Cost Management |
| Azure Advisor | Trusted Advisor | Recommender |
| Defender for Cloud | Security Hub | Security Command Center |

# **AZ-900 Exam Tips — Keyword → Answer Cheat Sheet**

| Keyword in the question | The answer is usually |
| :---- | :---- |
| “Physically separate datacenters within a region” | Availability Zones |
| “Two regions paired for disaster recovery” | Region pairs |
| “Private dedicated connection, not over the internet” | ExpressRoute |
| “Secure RDP/SSH without public IPs” | Azure Bastion |
| “Store secrets, keys, certificates” | Key Vault |
| “App authenticates without stored credentials” | Managed identity |
| “Who did what and when” | Activity log |
| “Block resources outside allowed regions” | Azure Policy (Deny) |
| “Prevent accidental deletion” | Resource lock (CanNotDelete) |
| “Estimate cost before deployment” | Pricing Calculator |
| “Compare with on-premises costs” | TCO Calculator |
| “Recommendations in five categories” | Azure Advisor |
| “SIEM / SOAR” | Microsoft Sentinel |
| “Secure Score / security posture” | Defender for Cloud |
| “Manage AWS/on-prem servers from Azure” | Azure Arc |
| “Just-in-time, time-bound admin roles” | PIM |
| “Sign-in rules based on location/device/risk” | Conditional Access |
| “Ship huge data physically” | Azure Data Box |
| “DNS-based global routing” | Traffic Manager |
| “URL-path routing \+ WAF, one region” | Application Gateway |
| “Global HTTP entry point \+ WAF \+ caching” | Azure Front Door |
| “Data must stay in-region and survive zone failure” | ZRS |
| “Rarely accessed, hours to retrieve, cheapest” | Archive tier |
| “Decouple application components with messages” | Queue Storage |
| “Mapped network drive / SMB share” | Azure Files |
| “No-code workflow with connectors” | Logic Apps |
| “Event-driven code, pay per execution” | Azure Functions |
| “One container quickly, no cluster” | Container Instances |
| “Orchestrate many containers” | AKS |

## **Memory Tricks (English Edition)**

| Term | Trick |
| :---- | :---- |
| IaaS / PaaS / SaaS | “I get a server” / “I deploy code” / “I just use it” |
| Scalability vs Elasticity | Scalability \= the ability to resize; Elasticity \= resizing happens **automatically** |
| CapEx vs OpEx | One big payment up front vs monthly pay-as-you-go |
| Fault domain vs Update domain | Different **rack/power** vs different **reboot batch** |
| RPO vs RTO | “Point” \= data point lost; “Time” \= downtime allowed |
| Availability Zone | Separate buildings in the same city (region) |
| Region pair | The disaster-recovery partner city |
| NSG | A doorman with a numbered checklist — lowest number checked first |
| Bastion | The VIP entrance — get in without a public address |
| ExpressRoute | A private highway — your traffic never joins internet traffic |
| ZRS | Copies across zones, but never leaves the region |
| Archive tier | A warehouse — cheap to store, slow to retrieve |
| Policy vs RBAC | Policy \= **what** is allowed; RBAC \= **who** is allowed |
| ReadOnly lock | “Look, don’t touch” — blocks changes and deletion |
| PIM | Admin powers on a timer |
| Advisor | A free consultant with five kinds of advice (Cost, Security, Reliability, Performance, Operational Excellence) |
| Activity log | The CCTV recording of who did what |
| Bicep | ARM JSON’s friendlier sibling |
| Azure Arc | Azure’s arm reaching into AWS and your datacenter |

*If you already know AWS, Terraform, Docker, and Kubernetes, treat Azure as the same core concepts with different service names — the consolidated mapping table above is your fastest on-ramp, and AZ-900 will feel very familiar.*