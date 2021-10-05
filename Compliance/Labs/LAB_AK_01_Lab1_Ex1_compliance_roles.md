# Lab 1 Exercise 1 - Manage Compliance Roles

In your role as Joni Sherman, the newly hired Compliance Administrator for Contoso Ltd. you are tasked to configure the new Microsoft 365 tenant of your organization, to meet the organizations compliance requirements. Contoso Ltd. is a company with a headquarters in the United States and several new subsidiaries in the European Union and your organization needs to make sure the new Microsoft 365 tenant fulfills the legal requirements of different countries and regulatory requirements of your industry sector.

### Task 1 – Assign Compliance Roles

In this exercise, you will follow the principal of least privilege and use the default Global Administrator to assign the Compliance Admin role to Joni Sherman, which is required to perform the operations described in this lab.

1. Log into the Client 1 VM (LON-CL1) as the **lon-cl1\admin** account.  The password should be provided by your lab hosting provider.

2. Open **Microsoft Edge** from the taskbar and when a **Welcome to the new Microsoft Edge** windows is displayed, select **Complete setup**.

3. Select **Confirm** to accept the default browser settings and **Continue without signing in**.

4. In **Microsoft Edge**, navigate to **https://admin.microsoft.com** and log into the Microsoft 365 Admin center as **MOD Administrator** admin@WWLxZZZZZZ.onmicrosoft.com (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider).  Admin's password should be provided by your lab hosting provider.

5. On the **Stay signed in?** dialog box, select the **Don’t show this again** checkbox and then select **No**.

6. Close the password save dialog from the bottom with Never, to not save the default global admins credentials in your browser.

7. If a welcome screen is displayed, close it. If the Office 365 apps notification appears, also close it.

8. If a welcome window is displayed, select Get started and close it.

9. In the left navigation pane, expand **Users** and then select **Active users**.

10. In the **Active users** list, search and select **Joni Sherman**, to open the right-side settings pane.

11.	In the settings below the **Account** tab, scroll to **Roles** and select **Manage roles** below.

12.	When the **Manage admin roles** pane opens, select **Admin center access**, select **Show all by category** and scroll down to select **Compliance admin** in the Security & Compliance section.

13.	Select **Save changes** to apply the role. When the **Admin roles updated** message is displayed on the upper part of the pane, select the arrow pointing to the left to return to Joni's user record.

14.	Close the window of Joni Sherman’s account with the **X** in the upper right to go back to the **Active users** list.

15. Select the circle with **MA** in the upper right and select **Sign out**.

16. Close the **Microsoft Edge** browser window.

You have successfully assigned Joni Sherman the Compliance Administrator role, which is required to perform the different exercises of this lab. Continue with the next task.

### Task 2 – Explore the Compliance Center

In this task, you will sign out of the global admin account and sign-in again as Joni Sherman. Now that Joni Sherman was just assigned the Compliance admin role, her account will be sufficient for most of this lab's exercises.

1. You should still be logged into your Client 1 VM (LON-CL1) as the **lon-cl1\admin** account. 

2. In **Microsoft Edge**, navigate to **https://compliance.microsoft.com**.

3. When the **Pick an account** window is displayed, select **Use another account**.

4. When the **Sign in** window is displayed, sign in as JoniS@WWLxZZZZZZ.onmicrosoft.com (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider).  Joni's password should be provided by your lab hosting provider.  Hint: The password is probably the same as the MOD Administrator used earlier.

5. If the **Improve your compliance posture** message window opens, read the text and select **Next** twice and then select **Done**.

6. Scroll down and select **Settings** from the lower left side to see which settings are available to Joni.

7. Get yourself familiar with the different settings. When you are done, leave the browser window open.

You have successfully switched to Joni Sherman's account and you are now ready to start with the lab.

# Proceed to Exercise 2