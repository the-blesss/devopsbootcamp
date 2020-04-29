# Frequently Asked Questions

## Do I need to use the same email address for my Azure and GitHub Accounts

No, you can use different email addresses.

## How do I find my Azure Subscription ID?

Method 1: from the cloud shell, run the command `az account show --query "id"`
Method 2: from the Azure Portal, use the search box and type Subscriptions, view the list of your subscription(s) with their subscription ID

## Can I use my work email if signing up for a free Azure Account?

You should use a personal email when signing up for a free Azure Account, since someone else at your company could have already signed up and you may not be able to create another free account linked to the same organization.

## What permissions, roles, or rights do I need in my Azure Subscription or AAD Tenant?

If using your own free Azure Subscription, your account will be both a Global Admin in your Azure Active Directory (AAD) tenant (example: myemailaddress.onmicrosoft.com) and your account will also be an Owner Role (IAM) on the subscription.

If using an existing subscription, confirm you are a Global Admin in Azure Active Directory, and confirm you are an Owner of the subscription.
- Azure Active Directory Global Administrator: https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles
- Subscription Owner, also called Access Control or IAM, or Role Based Access Control (RBAC): https://docs.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal

## How do I fix or restart Azure Cloud Shell if I have an error?

-First, try doing a reset by selecting the restart icon on the cloud shell toolbar.
-Second, if you received an error about your cloud storage account, you may need to close cloud shell, delete your cloud shell storage account, which will be stored in a resource group similar to "cloud-shell-storage-eastus", but with your local region in the name. The name of the storage account if previously created, will start with "cs". If you are located in Canada, there are currenly no regions supported for cloud shell storage. When starting cloud shell the next time you will be prompted to create a cloud shell storage account, or you can use the advanced settings and select an existing storage account in a supported region. 
--https://docs.microsoft.com/en-us/azure/cloud-shell/persisting-shell-storage#supported-storage-regions
