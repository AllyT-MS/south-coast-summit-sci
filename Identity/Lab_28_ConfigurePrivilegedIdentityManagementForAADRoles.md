---
lab:
    title: '28 - Configure Privileged Identity Management for Azure AD roles'
    learning path: '04'
    module: 'Module 03 - Plan and implement privileged access'
---

# Lab 28: Configure Privileged Identity Management for Azure AD roles

## Lab scenario

A Privileged role administrator can customize Privileged Identity Management (PIM) in their Azure Active Directory (Azure AD) organization, including changing the experience for a user who is activating an eligible role assignment. You must become familiar with configuring PIM.

#### Estimated time: 15 minutes

## Configure Azure AD role settings

### Open role settings

Follow these steps to open the settings for an Azure AD role.

1. Sign in to the [https://portal.azure.com](https://portal.azure.com) as a Global administrator.

1. Search for and then select **Azure AD Privileged Identity Management.**

1. In the Privileged Identity Management blade, in the left navigation, select **Azure AD roles.**

1. On the Quick start page, in the left navigation, select **Settings.**

    ![Screen image displaying the Azure AD roles page with the Settings menu highlighted](./media/lp3-mod3-pim-ad-roles-settings.png)

1. Review the list of roles and then, in the **Search by role name**, enter **compliance**.

1. In the results, select **Compliance Administrator**.

1. Review the role setting details information.

### Require approval to activate

If setting multiple approvers, approval completes as soon as one of them approves or denies. You cannot require approval from at least two users. To require approval to activate a role, follow these steps.

1. In the Role setting details page, on the top menu, select **Edit**.

    ![Screen image displaying the top portion of the Role setting details -Compliance Administrator page with Edit highlighted](./media/lp4-mod3-pim-edit-compliance-role.png)

1. In the Edit role setting – Compliance Administrator blade, select the **Require approval to activate** check box.

1. Select **Select approvers**.

1. In the Select a member pane, select your administrator account and then select **Select**.

    ![Screen image displaying the edit role settings blade and select a member pane with the selected members highlighted](./media/lp4-mod3-pim-add-approver.png)

1. Once you have configured the role settings, select **Update** to save your changes.
