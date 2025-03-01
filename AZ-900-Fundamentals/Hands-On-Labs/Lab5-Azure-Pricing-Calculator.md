# Lab 5: Using Azure Pricing Calculator

## **Objective**
This hands-on lab provides a step-by-step guide to using the **Azure Pricing Calculator** to estimate the cost of deploying Azure services. By the end of this lab, you will:
- Navigate and use the **Azure Pricing Calculator**.
- Estimate costs for **Virtual Machines, Storage, and Networking**.
- Understand how different pricing models impact costs.

---

## **Prerequisites**
- An **Azure account** (optional but recommended).
- Access to **Azure Pricing Calculator** via a web browser.
- Basic understanding of **Azure services**.

---

## **Step 1: Access the Azure Pricing Calculator**
1. Open a web browser and go to [Azure Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/).
2. The calculator homepage displays **Azure products and services**.

---

## **Step 2: Estimate Costs for a Virtual Machine**
1. Click on **Virtual Machines** from the list of services.
2. Configure the following settings:
   - **Region**: Choose the deployment region (e.g., `East US`).
   - **Operating System**: Select `Windows` or `Linux`.
   - **VM Series**: Choose a **machine type** (e.g., `Standard B2s` for general workloads).
   - **VM Size**: Select a size based on workload requirements.
   - **Billing Model**:
     - `Pay-As-You-Go` (Hourly billing)
     - `Reserved Instances` (1-year or 3-year commitment for cost savings)
   - **Quantity**: Enter the number of VMs.
3. The estimated cost will appear at the bottom.

#### **Common Use Cases:**
- Understanding **compute costs** for production or development environments.
- Comparing **on-demand vs. reserved pricing models**.

---

## **Step 3: Estimate Costs for Azure Storage**
1. Click on **Storage Accounts**.
2. Configure the following settings:
   - **Region**: Same as VM region.
   - **Storage Type**: Choose `Blob Storage`, `File Storage`, or `Managed Disks`.
   - **Redundancy**: Select storage replication type:
     - `Locally Redundant Storage (LRS)` (Low cost, single region)
     - `Geo-Redundant Storage (GRS)` (Higher availability, multi-region replication)
   - **Capacity**: Define storage size (e.g., `500 GB`).
   - **Transactions**: Estimate the number of read/write operations per month.
3. View the estimated cost in the summary section.

#### **Common Use Cases:**
- Estimating **backup and disaster recovery costs**.
- Comparing **different storage replication strategies**.

---

## **Step 4: Estimate Costs for Networking (Bandwidth & VPN)**
1. Click **Networking** and add **Bandwidth**.
2. Configure:
   - **Outbound Data Transfer**: Estimate monthly data usage (e.g., `1 TB`).
   - **Region**: Choose your deployment region.
3. Add **VPN Gateway**:
   - **SKU**: Choose `Basic` for testing or `High Performance` for production.
   - **Connections**: Estimate the number of VPN tunnels.
4. The cost breakdown appears at the bottom.

#### **Common Use Cases:**
- Calculating **bandwidth costs for global applications**.
- Planning **hybrid cloud VPN costs**.

---

## **Step 5: Export and Share Pricing Estimates**
1. Click **Save** to store the current estimate.
2. Click **Export** to download the estimate as a CSV file.
3. Share the estimate with your team for **budget approvals**.

---

## **Step 6: Compare Pricing Models**
Azure offers multiple pricing models:

| Pricing Model | Description | Best Use Case |
|--------------|-------------|--------------|
| **Pay-As-You-Go** | Pay for actual usage per hour/month | Short-term projects, testing environments |
| **Reserved Instances (RI)** | 1-year or 3-year upfront commitment with discounts | Long-term workloads, cost savings |
| **Spot Pricing** | Buy unused compute at a lower rate | Batch processing, fault-tolerant workloads |
| **Hybrid Benefits** | Use existing Windows or SQL Server licenses | Enterprise customers reducing software costs |

---

## **Step 7: Clean Up (Optional)**
If you created any test resources in **Azure Portal**, navigate to the **Resource Group** and delete them to avoid charges.

---

## **Conclusion**
Congratulations! 🎉 You have successfully:
- Used the **Azure Pricing Calculator** to estimate costs.
- Configured pricing for **VMs, storage, and networking**.
- Compared **different pricing models** to optimize costs.

Understanding **Azure pricing** helps organizations budget effectively and minimize cloud expenses.

Next, let’s explore the **[AZ-104: Microsoft Azure Administrator](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/Journal.md)** *(Upcoming)* certification.