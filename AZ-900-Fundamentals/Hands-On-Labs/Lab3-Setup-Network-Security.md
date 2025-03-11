# Lab 3: Set Up Network Security in Azure

## **Objective**
This hands-on lab provides a step-by-step guide to **configuring network security** in Azure. By the end of this lab, you will:
- Create a **Virtual Network (VNet)** and define **subnets**.
- Configure **Network Security Groups (NSGs)** to enforce traffic control.
- Set up **firewall rules and VPN connectivity** for secure access.

---

## **Prerequisites**
- An **Azure account** with an active subscription.
- Basic understanding of **Azure networking concepts**.
- Access to **Azure Portal**.

---

## **Step 1: Log in to Azure Portal**
1. Open a web browser and go to [Azure Portal](https://portal.azure.com).
2. Sign in with your **Azure credentials**.

---

## **Step 2: Create a Virtual Network (VNet) and Subnets**
### **2.1 Navigate to the Virtual Networks Section**
1. In the **Azure Portal**, search for **Virtual Networks**.
2. Click **+ Create** to create a new Virtual Network.

### **2.2 Configure Virtual Network Settings**
1. **Subscription**: Select your active subscription.
2. **Resource Group**: Choose an existing one or create a new one.
3. **VNet Name**: Enter a unique name (e.g., `MySecureVNet`).
4. **Region**: Choose the closest region to your location.

### **2.3 Define Subnets**
1. Click on **+ Add subnet**.
2. Enter a **Subnet Name** (e.g., `WebSubnet`).
3. Assign an **IP address range** (e.g., `10.0.1.0/24`).
4. Click **OK** to save the subnet.
5. Repeat the process to create additional subnets (e.g., `DatabaseSubnet`).

---

## **Step 3: Configure Network Security Groups (NSGs)**
### **3.1 Create an NSG**
1. In the **Azure Portal**, search for **Network Security Groups**.
2. Click **+ Create** to start a new NSG.
3. Configure the following settings:
   - **Subscription**: Select your subscription.
   - **Resource Group**: Use the same as the Virtual Network.
   - **NSG Name**: Enter a name (e.g., `WebSubnet-NSG`).
   - **Region**: Select the same region as your Virtual Network.
4. Click **Review + Create**, then **Create**.

### **3.2 Attach the NSG to a Subnet**
1. Navigate to the newly created **NSG**.
2. Click **Subnets** under **Settings**.
3. Click **+ Associate** and select your **VNet and subnet** (e.g., `WebSubnet`).
4. Click **OK**.

### **3.3 Configure NSG Inbound Rules**
1. In the **NSG settings**, go to **Inbound security rules**.
2. Click **+ Add Rule** to create a new rule:
   - **Name**: Allow-HTTP
   - **Priority**: 1000 (lower numbers have higher priority)
   - **Source**: Any
   - **Destination**: Any
   - **Port**: `80` (for HTTP)
   - **Action**: Allow
3. Click **OK** to apply the rule.
4. Repeat for other required ports (e.g., `443` for HTTPS, `3389` for RDP, `22` for SSH).

### **3.4 Configure NSG Outbound Rules**
1. Go to **Outbound security rules** in the NSG settings.
2. Click **+ Add Rule** and configure:
   - **Name**: Allow-Internet-Outbound
   - **Priority**: 1000
   - **Source**: Any
   - **Destination**: Internet
   - **Port**: `Any`
   - **Action**: Allow
3. Click **OK** to save.

---

## **Step 4: Set Up an Azure Firewall (Optional)**
1. Search for **Azure Firewall** in the Azure Portal.
2. Click **+ Create** and configure:
   - **Subscription & Resource Group**: Use the same as your VNet.
   - **Firewall Name**: Enter a unique name.
   - **Region**: Select the same as your Virtual Network.
   - **Virtual Network**: Attach the firewall to the VNet.
3. Click **Review + Create**, then **Create**.

### **4.1 Configure Firewall Rules**
1. Navigate to your **Azure Firewall**.
2. Under **Rules**, click **+ Add Rule Collection**.
3. Configure an **Application Rule** to allow outbound internet access:
   - **Name**: Allow-Web
   - **Priority**: 1000
   - **Action**: Allow
   - **Target FQDNs**: `*.microsoft.com`, `*.azure.com`
4. Click **Save**.

---

## **Step 5: Configure VPN Gateway (Optional)**
If you need secure on-premises connectivity, you can create a **VPN Gateway**.

### **5.1 Create a VPN Gateway**
1. Search for **Virtual Network Gateway** in the Azure Portal.
2. Click **+ Create**.
3. Configure:
   - **Name**: Enter a unique name (e.g., `MyVPNGateway`).
   - **Virtual Network**: Select your existing VNet.
   - **Gateway Type**: VPN
   - **SKU**: Basic (for testing) or higher for production.
4. Click **Review + Create**, then **Create**.

### **5.2 Configure VPN Client Settings**
1. Go to your **VPN Gateway** and select **Point-to-Site Configuration**.
2. Enable **Point-to-Site (P2S) VPN**.
3. Configure an **address pool** (e.g., `192.168.1.0/24`).
4. Select **Authentication Type** (Azure AD or certificate-based).
5. Download and install the VPN client on your local machine.

---

## **Step 6: Validate Network Security Settings**
1. Open **Azure Network Watcher**.
2. Select **IP Flow Verify** to check if NSG rules allow expected traffic.
3. Run **Connection Troubleshoot** to test connectivity between resources.
4. Monitor **NSG Logs** in **Azure Monitor** for security insights.

---

## **Step 7: Clean Up Resources (Optional)**
1. Navigate to the **Resource Group** used for this lab.
2. Click **Delete Resource Group** to remove all resources.

---

## **Conclusion**
Congratulations! 🎉 You have successfully:
- Created a **Virtual Network (VNet) with subnets**.
- Configured **Network Security Groups (NSGs)** to enforce security policies.
- Set up an **Azure Firewall and VPN Gateway** for secure connectivity.
- Used **Azure Network Watcher** to test and monitor network security.

You can now explore **more advanced network security features** like **DDoS Protection, Azure Bastion, and Private Endpoints** to further secure your Azure environment.