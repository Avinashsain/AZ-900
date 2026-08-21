# AZ-900 Practice Exam Review

**Score:** 41/50 correct (82%)

## Missed Questions

### Q7 — App Service Plan (Premium v3) app limit
A single Premium v3 App Service Plan supports an **unlimited** number of web apps, not a fixed number like 10 or 100.

### Q8 — 6 copies of data across 2 regions
This is **GRS** (Geo-Redundant Storage): 3 copies in the primary region, 3 in the secondary region.

### Q10 — Private connection from on-prem to Azure
**Azure ExpressRoute** provides a private connection that never touches the public internet. Site-to-site VPN is encrypted but still travels over the public internet.

### Q12 — Regional failover
Azure services fail over to their **region pair**, which is at least 300 miles away in the same geography — not just "another region" in general.

### Q21 — How high availability avoids financial losses
It's primarily about **ensuring uninterrupted revenue generation**, not directly about reducing operational costs.

### Q24 — Data rarely accessed, must be stored 180+ days
This describes the **Archive** access tier. Cool is for infrequently accessed data that still needs quick access when retrieved.

### Q25 — App requiring Windows Registry access
Only **IaaS** (Virtual Machines) gives full OS-level control needed for Registry access. PaaS/Serverless/SaaS abstract this away.

### Q31 — Key benefit of Microsoft Entra Domain Services
It provides a **managed domain service in the cloud** without needing to run and maintain your own domain controllers.

### Q37 — Adding more resources to a pool of existing resources
This is **horizontal scaling** (scale-out). Vertical scaling (scale-up) means increasing the capacity of an existing resource.

### Q40 — Can subscriptions be nested?
**No.** Each Azure subscription is a standalone entity; subscriptions cannot be nested within one another.

### Q41 — Packaging apps + dependencies for consistent behavior across environments
**Containers** — lightweight, portable, and consistent across environments (vs. VMs, serverless, or functions).

### Q42 — Max data in a single Azure Storage account
**5 Petabytes.**

### Q45 — Program-to-program communication via Queue Storage
Queue Storage is best suited for **asynchronous communication**, decoupling sender and receiver.

### Q49 — Autoscaling VMs based on demand
This is an example of **"management of the cloud"** (managing your cloud resources), as opposed to "management in the cloud" (the tools/interfaces used to manage, like Portal, CLI, or APIs).

---

## Patterns to Review Further
These concepts came up more than once and are worth extra drilling before the real exam:

- **Storage redundancy & tiers** — LRS/ZRS/GRS/GZRS, and Hot/Cool/Archive access tiers (Q8, Q24, Q42)
- **Scaling terminology** — horizontal vs. vertical scaling, and "management of the cloud" vs. "management in the cloud" (Q37, Q49)
- **Networking connectivity options** — VPN vs. ExpressRoute vs. Peering (Q10)
- **Service model boundaries (IaaS/PaaS/SaaS/Serverless)** — what level of control each gives you (Q25)
