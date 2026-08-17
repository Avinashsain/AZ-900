# AZ-900 Exam Prep — Cleaned & Organized Study Guide

Everything from your original notes, deduplicated, cross-checked, and grouped so it's actually fast to review. Same content, no repeated flashcards, no scattered cheat sheets.

---

## How to use this before the exam

1. Read the **Master Cheat Sheet** once, top to bottom (5 min).
2. Skim the **"Commonly Confused Pairs"** section — this is where most wrong answers come from.
3. Go category by category through the flashcards, covering the right column and testing yourself.
4. Re-read **Your Practice Test Mistakes** last, since those are your actual weak spots.

---

## 1. Master Cheat Sheet (last 10 minutes before the exam)

| If the question says… | Choose… |
|---|---|
| Personalized recommendations across cost/security/reliability | **Azure Advisor** |
| Web app is slow / performance bottleneck | **Application Insights** |
| Run queries against collected log data | **Log Analytics** |
| Azure-wide outage notification | **Azure Service Health** |
| One specific resource/VM is unhealthy | **Resource Health** |
| Overall security posture / Secure Score | **Microsoft Defender for Cloud** |
| Enforce naming rules / compliance | **Azure Policy** |
| Bulk upload / resume-able large transfer | **AzCopy** |
| Partner company needs access | **Microsoft Entra B2B** |
| Customer-facing app login | **Microsoft Entra B2C** |
| Remote Windows 10/11 desktops | **Azure Virtual Desktop** |
| Branch office + local file cache | **Azure File Sync** |
| Estimate cost *before* deploying | **Azure Pricing Calculator** |
| Track *current* spend | **Cost Management + Billing** |
| Department-wise billing/chargeback | **Tags + Cost Analysis** |
| Private, dedicated, non-internet connection | **ExpressRoute** |
| Never touches the public internet | **Private Endpoint** |
| Rare access but needs to be instant | **Cool Tier** |
| Rare access, retrieval can be slow (hours) | **Archive Tier** |
| Scripted with cmdlets | **Azure PowerShell** |
| Scripted with commands (cross-platform) | **Azure CLI** |
| Store secrets/certs/keys | **Azure Key Vault** |
| Minimum necessary permissions | **RBAC / Least Privilege** |
| "Verify every request" model | **Zero Trust** |
| Baseline load vs. unpredictable peak load | **Reserved VM (baseline) + Pay-as-you-go (peak)** |
| Datacenter fails, same region | **Availability Zones** |
| Entire region is lost | **Region Pairs** |
| Predictable long-term VM savings | **Reserved Instances** |
| Track compliance with GDPR/ISO 27001 | **Microsoft Purview Compliance Manager** |
| Design principle: eliminate single points of failure | **High Availability** |
| Managed Hadoop / big data analytics | **HDInsight** |
| Max VMs in a Scale Set | **1,000** (600 with a custom image) |

---

## 2. Commonly Confused Pairs (exam traps)

| Wrong answer people pick | Right answer | Why |
|---|---|---|
| Azure Monitor | **Application Insights** | Monitor = infrastructure metrics/logs; App Insights = application performance |
| Azure VM | **Azure Virtual Desktop** | AVD = multi-session, centrally managed, cost-effective for many users |
| Azure Files | **Azure File Sync** | Azure Files = the storage itself; File Sync = caching it locally at branch offices |
| Azure Policy | **Defender for Cloud** | Policy = enforce rules/compliance; Defender = security posture & threat detection |
| Resource Groups | **Tags** | Resource Groups = deployment/lifecycle container; Tags = cost/metadata reporting |
| TCO Calculator | **Pricing Calculator** | TCO Calculator is retired — use Pricing Calculator for cost estimates |
| Cool Tier | **Archive Tier** | Cool = infrequent but *instant* access; Archive = infrequent, *slow* (hours) retrieval |
| ExpressRoute | **Private Endpoint** | ExpressRoute = private network path to Azure; Private Endpoint = private IP for a specific PaaS service |
| Entra B2C | **Entra B2B** | B2B = external partner/business users; B2C = your own app's customers |
| Availability Zones | **Region Pairs** | AZs protect against a single datacenter failing; Region Pairs protect against an entire region going down |
| RBAC alone | **RBAC + Azure Policy** | RBAC controls *who can do what*; Policy still enforces compliance rules on top, regardless of role |
| Reservations for unpredictable workloads | **Spot VMs / Pay-as-you-go** | Reservations only pay off for steady, predictable usage |

---

## 3. Cloud Concepts

| Term | Meaning |
|---|---|
| Public cloud | Owned and operated by a cloud provider (e.g., Microsoft) |
| Private cloud | Owned/used by a single organization |
| Hybrid cloud | Mix of on-prem + cloud |
| CapEx | Upfront capital cost |
| OpEx | Pay-as-you-go operating cost |
| Elasticity | Automatically grows/shrinks with demand |
| Scalability | Ability to increase capacity (manually or automatically) |
| High availability | Minimizes downtime |
| Fault tolerance | System keeps running after a component fails |
| Disaster recovery | Restoring operations after a major outage |
| IaaS | Infrastructure as a Service — VMs, networking, storage |
| PaaS | Platform as a Service — app platform, no OS management |
| SaaS | Software as a Service — ready-made software |
| Shared responsibility model | Microsoft secures the cloud; customer secures their data/access |
| Region | A geographic location with one or more datacenters |
| Availability Zone | Physically separate datacenters within a region |
| Region Pair | Two regions paired for disaster resilience |
| Edge location | Point of presence for faster content delivery |
| Consumption model | Pay only for what you use |
| SLA | Uptime commitment from Microsoft |

---

## 4. Compute Services

| Service | Use case |
|---|---|
| Virtual Machines | IaaS compute, full OS control |
| App Service | Host web apps without managing servers |
| Azure Functions | Serverless, run code only when triggered |
| Container Instances | Run containers quickly, no orchestration |
| Azure Kubernetes Service (AKS) | Managed Kubernetes |
| Azure Virtual Desktop | Multi-session remote Windows desktops |

## 5. Storage Services

| Service | Use case |
|---|---|
| Blob Storage | Unstructured data (images, video) |
| Azure Files | SMB file shares in the cloud |
| Azure File Sync | Syncs Azure Files with a local cache at branch offices |
| Managed Disks | VM disk storage |
| Azure SQL Database | Managed relational (SQL) database |
| Cosmos DB | Globally distributed NoSQL database |
| Data Lake Storage | Large-scale analytics storage |
| Queue Storage | Message queuing |
| Table Storage | NoSQL key-value store |
| Storage Explorer | GUI tool for managing storage accounts |

### Storage access tiers
| Tier | Access pattern |
|---|---|
| Hot | Frequent access |
| Cool | Infrequent, but instant retrieval |
| Archive | Rare access, slow (hours) retrieval, cheapest |

### Redundancy options
| Option | Coverage |
|---|---|
| LRS | One datacenter |
| ZRS | Multiple availability zones, same region |
| GRS | Replicated to a paired region |
| RA-GRS | GRS + read access to the secondary region |

### Storage features
| Feature | Purpose |
|---|---|
| Lifecycle Management | Automatically move data between tiers |
| Immutable Storage | Prevents changes/deletion for a set period |
| Soft Delete | Recover accidentally deleted data |
| Snapshots | Point-in-time copy of a disk/blob |
| Managed Identity | No stored credentials for resource access |
| SAS Token | Time-limited, scoped access to storage |
| AzCopy | Command-line bulk/resumable transfer tool |

---

## 6. Networking

| Service | Purpose |
|---|---|
| Virtual Network (VNet) | Private network in Azure |
| Subnet | Segment of a VNet |
| Network Security Group (NSG) | Allow/deny traffic rules |
| Route Table | Controls traffic path |
| VPN Gateway | Encrypted connection over the public internet |
| ExpressRoute | Private, dedicated connection (no internet) |
| VNet Peering | Connects two VNets |
| Azure Bastion | Secure VM access without a public IP |
| Load Balancer | Distributes Layer 4 (TCP/UDP) traffic |
| Application Gateway | Layer 7 routing + Web Application Firewall |
| Traffic Manager | DNS-based global traffic routing |
| Azure Front Door | Global entry point + routing |
| Azure CDN | Edge caching for faster content delivery |
| NAT Gateway | Outbound internet access for private resources |
| Private DNS | Internal name resolution |
| DNS Zone | Hosts domain records |
| Service Endpoint | Secure access to Azure PaaS over the Azure backbone |
| Private Endpoint | Private IP address for a specific PaaS service (never public internet) |

---

## 7. Identity & Security

| Service | Purpose |
|---|---|
| Microsoft Entra ID | Core identity service |
| Entra B2B | Access for external partner/business users |
| Entra B2C | Identity for your app's customers |
| Conditional Access | Access policies based on location/device/risk |
| Multi-Factor Authentication (MFA) | Extra verification beyond password |
| Single Sign-On (SSO) | One login across multiple apps |
| RBAC | Role-based access permissions |
| Least Privilege | Grant only the minimum access needed |
| Identity Protection | Detects risky sign-ins |
| Zero Trust | "Verify every request" security model |
| Defender for Cloud | Security posture, Secure Score, threat detection |
| Secure Score | Numeric security rating |
| Key Vault | Stores secrets, keys, and certificates |
| Disk Encryption | Encrypts VM disks |
| Network Security Group | Filters network traffic |
| Azure Firewall | Network-level protection |
| Web Application Firewall (WAF) | Protects web apps from SQLi/XSS |
| DDoS Protection | Mitigates denial-of-service attacks |
| Microsoft Sentinel | Cloud-native SIEM/SOAR |
| Private Endpoint | Private access to a PaaS service |

---

## 8. Management & Governance Tools

| Tool | Purpose |
|---|---|
| Azure Portal | Web-based management UI |
| Azure CLI | Cross-platform command-line management |
| Azure PowerShell | Cmdlet-based scripting/automation |
| Cloud Shell | Browser-based terminal |
| ARM Templates | Infrastructure as Code (JSON) |
| Bicep | Simplified syntax for ARM templates |
| Resource Group | Logical container for related resources |
| Subscription | Billing and access boundary |
| Management Group | Organizes/manages multiple subscriptions |
| Tags | Metadata for cost tracking and organization |
| Azure Advisor | Personalized optimization recommendations (cost, security, reliability, performance, operational excellence) |
| Azure Monitor | Collects metrics and logs |
| Log Analytics | Query and analyze log data collected by Azure Monitor |
| Application Insights | Application performance monitoring (APM) |
| Azure Service Health | Notifies of Azure-wide outages |
| Resource Health | Status of an individual resource |
| Activity Log | Record of management operations (who did what) |
| Azure Policy | Enforces organizational rules/compliance |
| Azure Blueprints | Repeatable governance templates |
| Azure Arc | Manages hybrid/multi-cloud resources from Azure |
| Microsoft Purview Compliance Manager | Tracks and scores compliance against standards like GDPR, ISO 27001 |

### How you can deploy ARM templates
Azure Portal • Azure PowerShell • Azure CLI • REST API / SDK — ARM accepts deployments from any of these.

### Scaling limits worth memorizing
- **Virtual Machine Scale Sets:** up to **1,000** VM instances (600 if using a custom image)
- **High availability principle:** design so there is **no single point of failure** — this is the "why," not a specific tool

---

## 9. Analytics & DevOps

| Service | Purpose |
|---|---|
| HDInsight | Managed Apache Hadoop / big-data analytics platform |
| Azure DevOps | Pipelines, boards, repos — CI/CD and project tracking |

---

## 10. Grab-Bag Facts (easy to miss)

- **Storage Service Encryption** encrypts Blob Storage data at rest automatically.
- **Site-to-Site VPN** requires a **VPN device** on the on-premises side.
- Microsoft Azure has one of the **largest global datacenter footprints** of any cloud provider.
- **Compute resources** are billed/consumed as **CPU cycles** (processing power), not just "a VM."
- A service in **Private Preview** requires an **invitation** to access — it isn't open to everyone.
- The **Azure Portal** is the primary **GUI** for managing resources (vs. CLI/PowerShell for scripting).
- Treating Azure as an extension of your on-premises datacenter (not a full migration) describes a **hybrid cloud** setup.
- A **DDoS attack that keeps happening despite DDoS Protection** is usually a **Layer 7 (application-layer)** attack — Azure DDoS Protection Standard focuses on network-layer (L3/L4); pair it with a **WAF** for Layer 7.
- Storing email/collaboration tools you don't manage the infrastructure or platform for (e.g., Microsoft 365) is a **SaaS** example.
- **Cool tier** is cheaper than **Hot tier** for storage, but has a minimum retention period and slightly higher access cost per transaction.

---

## 11. Cost Management

| Tool/Concept | Purpose |
|---|---|
| Pricing Calculator | Estimate costs **before** deployment |
| Cost Management + Billing | Track **current** spending |
| Budgets | Alerts before overspending |
| Reservations | Discount for predictable, long-term workloads |
| Spot VMs | Cheapest option, uses unused capacity, can be evicted |
| Savings Plan | Flexible compute cost savings |
| Tags + Cost Analysis | Department/team chargeback reporting |
| Azure Advisor | Cost optimization recommendations |
| Free services | Some Azure services have a free tier |
| Marketplace | Third-party solutions, sometimes with their own pricing |
| Export Costs | Scheduled cost reports |
| Forecast | Predicted future spend |
| Credits | Promotional balance |

> **Note:** The Total Cost of Ownership (TCO) Calculator has been retired — use the **Pricing Calculator** instead.

---

## 12. Your Practice Test Mistakes (Quick Revision)

### Set 1 — 8 missed questions

| Topic | Correct Answer | One-line reason |
|---|---|---|
| Azure Optimization | Azure Advisor | Analyzes existing resources, gives recommendations |
| Virtual Desktop | Azure Virtual Desktop | Multi-session, centralized, cost-effective vs. 1 VM/user |
| Hybrid Storage | Azure File Sync | Cloud storage + local cache at branch offices |
| Application Monitoring | Application Insights | APM — dependency tracking, anomaly detection |
| Cloud Security | Microsoft Defender for Cloud | Secure Score + continuous assessment + threat detection |
| Cost Estimation | Azure Pricing Calculator | TCO Calculator is retired; use this before deployment |
| Cost Allocation | Resource Tags + Cost Analysis | Enables department-wise chargeback |
| External Identity | Microsoft Entra B2B | Partner manages their own credentials |

### Set 2 — 6 missed questions

| Topic | Correct Answer | One-line reason |
|---|---|---|
| VM Pricing | Reserved VM + Pay-as-you-go | Reserved for baseline load, PAYG for peaks |
| Automation | Azure PowerShell | Cmdlet-based scripting |
| Private Connectivity | Azure ExpressRoute | Private, dedicated, bypasses the internet |
| Customer Identity | Microsoft Entra ID B2C | Customer-facing identity |
| Private Storage Access | Private Endpoint | Traffic never touches the public internet |
| Storage Tier | Cool Tier | Infrequent access but still needs instant retrieval |

### Set 3 — 10 missed questions

| Topic | Correct Answer | One-line reason |
|---|---|---|
| Availability Zones | Separate datacenters in one region | Protects against a single datacenter failing |
| Cost Savings | Reserved Instances | Immediate savings for predictable VM usage |
| Compliance | Purview Compliance Manager | Tracks/scores against GDPR, ISO 27001, etc. |
| ARM Deployment | Portal, PowerShell, CLI, REST API/SDK | ARM accepts deployment from any of these |
| Access | RBAC | Assign roles instead of sharing passwords |
| VM Scale Set | 1,000 VMs | 600 if using a custom image |
| High Availability | No single point of failure | The core design principle behind HA |
| Azure Policy | Enforces compliance regardless of role | RBAC grants access; Policy still restricts non-compliant resources |
| SLA | Varies by service | There's no single blanket SLA for all of Azure |
| Big Data | HDInsight | Managed Apache Hadoop platform |

---

## 13. 33 Rapid-Fire Practice Answers

Quick-fire items from your practice set that aren't already covered above:

| # | Question | Answer |
|---|---|---|
| 15 | Which service model is email/collaboration software you don't manage infrastructure for? | SaaS |
| 16 | Protects against one datacenter failing in a region | ZRS |
| 17 | Best tier for data kept 7 years, rarely accessed | Blob Archive Tier |
| 23 | Device needed for a Site-to-Site VPN | VPN Device (on-premises) |
| 24 | Cloud provider with the largest global datacenter footprint | Microsoft Azure |
| 25 | Azure used as an extension of on-prem infrastructure | Hybrid Cloud |
| 26 | Type of attack that keeps happening despite DDoS Protection | Layer 7 (application-layer) attacks — add a WAF |
| 27 | How Blob Storage data is encrypted at rest | Storage Service Encryption |
| 28 | Fully managed relational database PaaS | Azure SQL Database |
| 30 | Access requirement for a Private Preview feature | Invitation required |
| 31 | Azure DevOps feature for CI/CD | Pipelines |
| 32 | What compute resources are billed as | CPU cycles |
| 33 | Primary graphical tool for managing Azure | Azure Portal |

> Items 1–14 and 18–22, 29 from this set duplicate flashcards already covered in sections 1–9 above (VM pricing, PowerShell, ExpressRoute, Entra B2C, Private Endpoint, Cool Tier, Advisor, AVD, File Sync, App Insights, Defender, Tags, Entra B2B, Service Health, Region Pairs, Conditional Access, OpEx, Management Groups, VMSS limit, storage tier cost).

---

## 14. 30-Minute Final Revision Plan

| Time | Focus |
|---|---|
| 5 min | Advisor vs. Monitor vs. Defender for Cloud |
| 5 min | Pricing Calculator vs. Cost Management |
| 5 min | Azure File Sync vs. Azure Files |
| 5 min | Entra B2B vs. Entra B2C |
| 5 min | Cool Tier vs. Archive Tier vs. Private Endpoint vs. ExpressRoute |
| 5 min | Practice a handful of similar MCQs |

Good luck on the 23rd.