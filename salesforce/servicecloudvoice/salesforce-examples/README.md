# Omni Flow Deployment Guide

This repository contains a sample **Omni Flow** packaged as a ZIP file for deployment into a Salesforce environment using **Workbench**.

## 🧰 Prerequisites

Before deploying, ensure that you have:

- Access to **Salesforce Workbench**: [https://workbench.developerforce.com](https://workbench.developerforce.com)  
- Valid Salesforce credentials for **Production** or **Sandbox**
- Appropriate permissions to deploy metadata (Flows)

---

## 🚀 Deployment Steps

### 1. Log in to Workbench
1. Go to [https://workbench.developerforce.com](https://workbench.developerforce.com).
2. Select either **Production** or **Sandbox**.
3. Agree to the terms and click **Login with Salesforce**.

---

### 2. Upload and Deploy the ZIP File
1. From the top menu, navigate to **Migration → Deploy**.
2. Click **Browse File** and upload the ZIP file from this repository.
3. Leave the default options as they are.  
   - *(Optional)* Select **Rollback On Error** to undo partial deployments in case of failure.
4. Click **Next**.
5. Click **Deploy**.

---

### 3. Verify Deployment Status
- Wait for the deployment to complete.  
- When successful, the **Status** column will show **Succeeded**.

---

### 4. Confirm the Flow in Salesforce
1. In Salesforce Setup, search for **Flows** using the **Quick Find** box.
2. Locate the newly deployed Omni Flow in the list.

## ✅ Notes

- If the deployment fails, verify that your Salesforce user has the necessary permissions to deploy flows.  
- Ensure that all referenced resources (e.g., subflows, variables) exist in the target environment.

---

**Author:** Cisco WxCC Team  
**License:** MIT
