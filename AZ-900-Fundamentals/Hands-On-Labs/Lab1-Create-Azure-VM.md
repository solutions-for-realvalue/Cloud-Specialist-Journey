# Lab 1: Create an Azure Virtual Machine

## **Objective**
This hands-on lab provides step-by-step instructions to deploy a **Virtual Machine (VM)** in Microsoft Azure. By the end of this lab, you will:
- Create a **Windows or Linux VM** using the **Azure Portal**.
- Configure **networking, storage, and authentication** settings.
- Access and manage the VM remotely.

---

## **Prerequisites**
- An **Azure account** with an active subscription.
- Internet access to connect to the **Azure Portal**.
- Basic knowledge of **Azure compute and networking concepts**.

---

## **Step 1: Log in to Azure Portal**
1. Open a web browser and go to [Azure Portal](https://portal.azure.com).
2. Sign in with your **Azure credentials**.

---

## **Step 2: Create a Virtual Machine**
### **2.1 Navigate to the Virtual Machines Section**
1. In the Azure Portal, search for **Virtual Machines** in the search bar.
2. Click on **Virtual Machines** and select **+ Create > Azure virtual machine**.

### **2.2 Configure Basic Settings**
1. **Subscription**: Select your active subscription.
2. **Resource Group**: Click **Create new** or choose an existing one.
3. **Virtual Machine Name**: Enter a unique name (e.g., `MyAzureVM`).
4. **Region**: Select the closest Azure region (e.g., `East US`).
5. **Availability Options**: Choose:
   - `No infrastructure redundancy` (default for simple deployments)
   - `Availability Zone` or `Availability Set` (for high availability)
6. **Image**: Choose an OS:
   - `Windows Server 2022` (for Windows-based workloads)
   - `Ubuntu 22.04` (for Linux-based workloads)
7. **Size**: Select a VM size based on workload requirements (e.g., `Standard_B1s` for testing).

### **2.3 Configure Authentication**
1. **Administrator Account**:
   - **For Windows:** Create a username and password.
   - **For Linux:** Choose SSH public key or password authentication.
2. **Inbound Port Rules**:
   - Allow **RDP (3389)** for Windows or **SSH (22)** for Linux to enable remote access.

---

## **Step 3: Configure Networking**
1. **Virtual Network (VNet)**: Select an existing VNet or create a new one.
2. **Subnet**: Choose a subnet for network isolation.
3. **Public IP**: Enable if you want external access.
4. **Network Security Group (NSG)**:
   - Configure inbound rules for **RDP (Windows)** or **SSH (Linux)**.
   - Restrict access to specific IPs for security.

---

## **Step 4: Configure Disks and Storage**
1. **OS Disk Type**: Choose **Standard SSD** (recommended for general workloads).
2. **Enable Boot Diagnostics**: Helps with troubleshooting VM issues.

---

## **Step 5: Review and Deploy**
1. Click **Review + Create** to validate configurations.
2. If everything looks good, click **Create**.
3. Wait for the deployment to complete.

---

## **Step 6: Connect to the VM**
### **6.1 Connect to a Windows VM using RDP**
1. Navigate to your deployed **Windows VM** in the Azure Portal.
2. Click on **Connect > RDP**.
3. Download the **RDP file** and open it.
4. Enter the **Administrator credentials** created earlier.

### **6.2 Connect to a Linux VM using SSH**
1. Open a terminal or PowerShell.
2. Use the following SSH command:
   ```bash
   ssh azureuser@<public-ip-address>
   ```
3. Accept the fingerprint and enter your password or use your private SSH key.

---

## **Step 7: Verify VM Status and Performance**
1. Navigate to the **Azure Portal > Virtual Machines**.
2. Click on your VM and review:
   - **CPU & Memory usage**
   - **Networking statistics**
   - **Disk performance**

---

## **Step 8: Shut Down or Delete the VM (Optional)**
- **Stop the VM**: Navigate to **Virtual Machines**, select the VM, and click **Stop**.
- **Delete the VM**: Navigate to **Resource Groups**, select the VM’s resource group, and click **Delete**.

---

## **Conclusion**
Congratulations! 🎉 You have successfully deployed a Virtual Machine in Azure. You learned how to configure networking, authentication, and storage settings while ensuring secure remote access. You can now experiment with **installing applications, configuring security, and automating VM management** in Azure.

Next, let’s explore the **[Configure Storage in Azure](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/Hands-On-Labs/Lab2-Configure-Storage.md)** in the next section.