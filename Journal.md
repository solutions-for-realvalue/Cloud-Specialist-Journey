# Journal.md

### **Cloud Specialist Journey - Learning & Development Log**

This journal serves as a **chronological record** of my learning process, challenges, insights, and milestones as I progress through my **Azure Cloud Specialist Journey**.

---

## **Azure Fundamentals Learning Path (AZ-900)**

### **1. Describe Cloud Computing**

- [**1.1 Define Cloud Computing**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/1-Describe-Cloud-Computing/1.1-Define-Cloud-Computing.md)
  - Introduction to cloud computing and its significance.
  - Key characteristics: scalability, elasticity, resource pooling.
  - On-premises vs. cloud environments.

- [**1.2 Benefits of Cloud**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/1-Describe-Cloud-Computing/1.2-Benefits-of-Cloud.md)
  - High availability, scalability, elasticity.
  - Disaster recovery, security, compliance benefits.
  - Cost savings with pay-as-you-go models.

- [**1.3 Cloud Service Types**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/1-Describe-Cloud-Computing/1.3-Cloud-Service-Types.md)
  - Infrastructure as a Service (IaaS), Platform as a Service (PaaS), Software as a Service (SaaS).
  - Use cases and best practices.

---

### **2. Describe Azure Architecture and Services**

- [**2.1 Core Architectural Components of Azure**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/2-Describe-Azure-Architecture-Services/2.1-Core-Architecture.md)
  - Azure regions, availability zones, region pairs.
  - Resource groups, subscriptions, and management hierarchy.

- [**2.2 Compute & Networking**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/2-Describe-Azure-Architecture-Services/2.2-Compute-Networking.md)
  - Virtual Machines (VMs), Azure Kubernetes Service (AKS).
  - Virtual Networks (VNets), Peering, VPN Gateway, ExpressRoute.

- [**2.3 Storage Services**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/2-Describe-Azure-Architecture-Services/2.3-Storage-Services.md)
  - Blob storage, file shares, storage redundancy options (LRS, GRS, RA-GRS).
  - Azure SQL Database and Azure Cosmos DB.

- [**2.4 Identity & Security**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/2-Describe-Azure-Architecture-Services/2.4-Identity-Security.md)
  - Microsoft Entra ID (formerly Azure AD), Role-Based Access Control (RBAC).
  - Multi-Factor Authentication (MFA) and Azure Key Vault.

---

### **3. Describe Azure Management & Governance**

- [**3.1 Cost Management**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/3-Describe-Azure-Management-Governance/3.1-Cost-Management.md)
  - Azure Pricing Calculator, Cost Management and Billing.
  - Cost-saving strategies and best practices.

- [**3.2 Governance & Compliance**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/3-Describe-Azure-Management-Governance/3.2-Governance-Compliance.md)
  - Azure Policy, Blueprints, Resource Tags, Locks.
  - Microsoft Defender for Cloud for compliance tracking.

- [**3.3 Managing & Deploying Resources**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/3-Describe-Azure-Management-Governance/3.3-Managing-Deploying-Resources.md)
  - Azure Portal, Azure CLI, PowerShell.
  - ARM Templates and Azure Arc for hybrid cloud management.

- [**3.4 Monitoring Tools**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/3-Describe-Azure-Management-Governance/3.4-Monitoring-Tools.md)
  - Azure Monitor, Log Analytics, Service Health.
  - Prometheus and Grafana for custom monitoring.

---

## **Hands-On Labs**

- [**Lab 1: Create an Azure VM**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/Hands-On-Labs/Lab1-Create-Azure-VM.md)
- [**Lab 2: Configure Storage**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/Hands-On-Labs/Lab2-Configure-Storage.md)
- [**Lab 3: Setup Network Security**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/Hands-On-Labs/Lab3-Setup-Network-Security.md)
- [**Lab 4: Identity & Access Management**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/Hands-On-Labs/Lab4-Identity-Access-Management.md)
- [**Lab 5: Azure Pricing Calculator**](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/Hands-On-Labs/Lab5-Azure-Pricing-Calculator.md)

## **Infrastructure as Code (Terraform & ARM Templates)**

**Topics Covered:**
- Introduction to Terraform & Infrastructure as Code (IaC).
- Writing basic Terraform configurations for Azure resource deployment.
- Understanding ARM Templates and their role in automation.

**Hands-on Labs:**
- Deployed an Azure Virtual Machine using Terraform.
- Configured a Virtual Network and Subnet using Terraform modules.
- Automated deployments using ARM Templates.

**Key Takeaways:**
- IaC significantly improves deployment consistency and scalability.
- Terraform state management and remote backends are crucial.
- ARM Templates provide native automation but require deep JSON knowledge.

---

## **Azure Kubernetes Service (AKS) Deployment & Management**

**Topics Covered:**
- Fundamentals of Kubernetes & container orchestration.
- Setting up Azure Kubernetes Service (AKS).
- Managing Kubernetes workloads with Helm Charts.
- Securing AKS clusters using RBAC and Azure Policy.

**Hands-on Labs:**
- Created an AKS cluster with Terraform.
- Deployed containerized applications using Helm.
- Configured Ingress Controllers and load balancers for secure access.

**Key Takeaways:**
- Kubernetes simplifies scaling and managing microservices-based applications.
- RBAC is crucial for securing Kubernetes workloads.
- Helm Charts simplify application deployment and versioning.

---

## **Cloud Security & Compliance (IAM, RBAC, Azure Policy)**

**Topics Covered:**
- Role-Based Access Control (RBAC) and Identity & Access Management (IAM).
- Configuring Privileged Identity Management (PIM).
- Implementing security baselines using Azure Policy.
- Encrypting data at rest, in transit, and in use.

**Hands-on Labs:**
- Created and managed Entra ID users and roles.
- Implemented RBAC to control access to Azure resources.
- Enforced security policies using Azure Policy and Defender for Cloud.

**Key Takeaways:**
- Least privilege access should always be enforced.
- Security policies help maintain compliance and governance.
- Azure Policy is a powerful tool to prevent misconfigurations.

---

## **Monitoring & Cost Optimization**

**Topics Covered:**
- Introduction to Azure Monitor and Log Analytics.
- Cost management strategies using Azure Advisor.
- Setting up alerts for performance and security anomalies.
- Integrating third-party tools (Prometheus & Grafana) with Azure Monitor.

**Hands-on Labs:**
- Created dashboards and alert rules in Azure Monitor.
- Configured Log Analytics workspaces for centralized logging.
- Implemented budget alerts and auto-scaling policies.

**Key Takeaways:**
- Monitoring is key to ensuring application reliability and performance.
- Azure Cost Management provides insights into cloud spending.
- Proactive alerting helps in identifying and resolving issues quickly.

---

## **Next Steps:**
- [ ] Continue refining Terraform automation scripts.
- [ ] Deepen Kubernetes and Helm knowledge.
- [ ] Explore advanced security features like Microsoft Sentinel.
- [ ] Implement serverless architectures with Azure Functions.
- [ ] Achieve AZ-104 certification.

---

### **Additional Resources**
- [AZ-900 Fundamentals Notes](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/Notes.md)
- [GitHub Repository](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey)

**Stay tuned for more updates on my Azure Cloud Specialist Journey!**