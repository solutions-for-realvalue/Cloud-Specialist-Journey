# Lab 4: Identity and Access Management in Azure

## **Objective**
This hands-on lab provides a step-by-step guide to configuring **Identity and Access Management (IAM)** in Azure. By the end of this lab, you will:
- Create and manage **Microsoft Entra ID (formerly Azure AD) users and groups**.
- Assign **Role-Based Access Control (RBAC)** permissions.
- Enable and configure **Multi-Factor Authentication (MFA)**.

---

## **Prerequisites**
- An **Azure account** with administrator privileges.
- Access to **Azure Portal**.
- Basic understanding of **Azure IAM concepts**.

---

## **Step 1: Log in to Azure Portal**
1. Open a web browser and go to [Azure Portal](https://portal.azure.com).
2. Sign in with your **Azure credentials**.

---

## **Step 2: Create a User in Microsoft Entra ID (Azure AD)**
### **2.1 Navigate to Microsoft Entra ID**
1. In the **Azure Portal**, search for **Microsoft Entra ID** (formerly Azure AD).
2. Click **Users** under **Manage**.

### **2.2 Create a New User**
1. Click **+ New User**.
2. Choose **Create User** and enter the following details:
   - **User Name**: `johndoe@yourdomain.onmicrosoft.com`
   - **Name**: `John Doe`
   - **Password**: Select `Auto-generate` and copy it for first login.
3. Click **Create**.

#### **Common Use Cases:**
- Managing **employee access** to Azure resources.
- Enforcing **role-based authentication** across the organization.
- Onboarding **contractors or temporary users** securely.

---

## **Step 3: Create a Security Group and Add Users**
### **3.1 Create a New Group**
1. In **Microsoft Entra ID**, click **Groups**.
2. Click **+ New Group** and configure:
   - **Group Type**: Security
   - **Group Name**: `IT-Admins`
   - **Membership Type**: Assigned
3. Click **Create**.

### **3.2 Add Users to the Group**
1. Open the newly created **IT-Admins** group.
2. Click **Members > + Add Members**.
3. Select `John Doe` (created in Step 2) and click **Add**.

#### **Common Use Cases:**
- Managing **department-wide access** to cloud resources.
- Enforcing **consistent security policies** for users.
- Simplifying **RBAC role assignments**.

---

## **Step 4: Assign Role-Based Access Control (RBAC) Permissions**
### **4.1 Navigate to Subscription IAM Settings**
1. In **Azure Portal**, go to **Subscriptions**.
2. Select your subscription and click **Access Control (IAM)**.

### **4.2 Assign a Role to a Group**
1. Click **+ Add Role Assignment**.
2. Select the following:
   - **Role**: `Contributor`
   - **Assign Access To**: `User, group, or service principal`
   - **Select Group**: Choose `IT-Admins`
3. Click **Review + Assign**.

#### **Common Use Cases:**
- Granting **admin access** to IT teams without full ownership permissions.
- Restricting **developers to specific Azure resources**.
- Preventing **unauthorized access to sensitive workloads**.

---

## **Step 5: Enable and Configure Multi-Factor Authentication (MFA)**
### **5.1 Navigate to Security Settings**
1. In **Microsoft Entra ID**, click **Security > Conditional Access**.
2. Click **+ New Policy**.

### **5.2 Create a Conditional Access Policy for MFA**
1. Set **Policy Name**: `Require MFA for Admins`
2. Under **Assignments**, select **Users and Groups**:
   - **Include**: `IT-Admins`
3. Under **Cloud Apps or Actions**, select **All cloud apps**.
4. Under **Grant**, select **Require Multi-Factor Authentication**.
5. Click **Create**.

### **5.3 User MFA Registration**
1. Navigate to [Microsoft MFA Setup](https://aka.ms/mfasetup).
2. Sign in as `John Doe` and follow the steps to:
   - Register a **mobile authenticator app**.
   - Set up **SMS or phone call authentication**.
3. Complete MFA registration.

#### **Common Use Cases:**
- Enforcing **MFA for admin and privileged accounts**.
- Preventing **phishing and credential theft**.
- Strengthening **Zero Trust security models**.

---

## **Step 6: Verify IAM Configuration**
1. Sign in as `John Doe` and try to access Azure resources.
2. Ensure that **RBAC roles** allow proper access.
3. Test **MFA prompts** to verify authentication security.

---

## **Step 7: Clean Up Resources (Optional)**
1. Navigate to **Microsoft Entra ID > Users** and delete `John Doe`.
2. Delete the **IT-Admins** security group.
3. Remove **RBAC role assignments** from the subscription.

---

## **Conclusion**
Congratulations! 🎉 You have successfully:
- Created and managed **users and groups** in Microsoft Entra ID.
- Assigned **Role-Based Access Control (RBAC) permissions**.
- Configured **Multi-Factor Authentication (MFA) policies**.
- Verified access controls and strengthened security.

You can now explore **more advanced IAM features** like **Privileged Identity Management (PIM)** and **Conditional Access Policies for device security**.

