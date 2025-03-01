# Lab 2: Configure Storage in Azure

## **Objective**
This hands-on lab provides a step-by-step guide to configuring **Azure Storage Accounts**, managing **Blob Storage**, and setting up **File Shares**. By the end of this lab, you will:
- Create an **Azure Storage Account**.
- Configure **Blob Storage** and upload data.
- Set up **Azure File Shares** for network storage.
- Apply **storage access policies** and redundancy settings.

---

## **Prerequisites**
- An **Azure account** with an active subscription.
- Internet access to log into **Azure Portal**.
- Basic understanding of **Azure Storage Services**.

---

## **Step 1: Log in to Azure Portal**
1. Open a web browser and go to [Azure Portal](https://portal.azure.com).
2. Sign in with your **Azure credentials**.

---

## **Step 2: Create an Azure Storage Account**
1. In the **Azure Portal**, search for **Storage Accounts**.
2. Click **+ Create** to start a new storage account.
3. Configure the following settings:
   - **Subscription**: Select your active subscription.
   - **Resource Group**: Choose an existing one or create a new one.
   - **Storage Account Name**: Enter a unique name (e.g., `mystorageaccount`).
   - **Region**: Choose a location close to your users.
   - **Performance**: Select `Standard` for general use or `Premium` for high-performance workloads.
   - **Redundancy**: Choose from:
     - **Locally Redundant Storage (LRS)**: Stores copies within a single region.
     - **Geo-Redundant Storage (GRS)**: Replicates data across regions.
4. Click **Review + Create**, then **Create** to deploy the storage account.

---

## **Step 3: Configure Blob Storage and Upload a File**
1. Navigate to the **Storage Account** you just created.
2. In the left panel, select **Containers** under **Data Storage**.
3. Click **+ Container**, enter a name (e.g., `myblobcontainer`), and set **Public access level** to `Private`.
4. Click **Create**.
5. Open the newly created container and click **Upload**.
6. Select a file from your local system and click **Upload**.

#### **Common Use Cases for Blob Storage:**
- Storing **media files, backups, and logs**.
- Hosting **static website content**.
- Storing **machine learning datasets**.

---

## **Step 4: Configure Azure File Shares**
1. In the **Storage Account**, select **File Shares**.
2. Click **+ File Share**, enter a **name**, and set the **quota limit (e.g., 5GB)**.
3. Click **Create**.
4. Open the newly created file share and click **Connect**.
5. Choose **Windows** or **Linux**, and copy the provided PowerShell or Bash command to mount the file share on a VM.

#### **Common Use Cases for Azure File Shares:**
- Centralized **file storage for enterprise applications**.
- Shared drives for **remote teams**.
- Hosting **configuration files** for cloud applications.

---

## **Step 5: Configure Access Control and Security**
### **5.1 Set Up Shared Access Signature (SAS) Token**
1. In the **Storage Account**, go to **Shared Access Signature** under **Security + Networking**.
2. Configure permissions (Read, Write, Delete, etc.) and **expiration time**.
3. Click **Generate SAS Token and URL**.
4. Copy the SAS URL and use it to access the storage securely.

### **5.2 Configure Network Access Controls**
1. Navigate to **Networking** in the **Storage Account** settings.
2. Choose **Allow access from selected virtual networks and IPs**.
3. Add IP addresses or VNets to restrict storage access.

---

## **Step 6: Monitor and Optimize Storage Usage**
1. In the **Storage Account**, go to **Insights** under **Monitoring**.
2. Review metrics like **storage capacity, transactions, and latency**.
3. Set up **alerts** to monitor unusual activity or cost spikes.

---

## **Step 7: Clean Up Resources (Optional)**
To avoid unnecessary charges, you can delete the resources created in this lab:
1. Navigate to the **Resource Group** used for the lab.
2. Click **Delete Resource Group** and confirm.

---

## **Conclusion**
Congratulations! 🎉 You have successfully:
- Created an **Azure Storage Account**.
- Configured **Blob Storage** and uploaded a file.
- Set up an **Azure File Share**.
- Applied **security and access controls**.
- Monitored storage usage to optimize performance and costs.

You can now explore **more advanced storage options**, such as **Azure Table Storage, Queue Storage, and encryption features**.

Next, let’s explore the **[Set Up Network Security in Azure](https://github.com/solutions-for-realvalue/Cloud-Specialist-Journey/blob/main/AZ-900-Fundamentals/Hands-On-Labs/Lab3-Setup-Network-Security.md)** in the next section.