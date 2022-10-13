# Welcome to the SCI Hack @ South Coast Summit October 2022
----------------------------------------------------------------------------------------------------

![image](https://github.com/AllyT-MS/south-coast-summit-sci/blob/main/scs.png)

## OpenHack - An Introduction for Attendees

OpenHack is a hands-on experience in which participants work in team to solve a series of coding challenges based on the requirements and resources provided. It is *not* designed to be delivered as a traditional training session or hands-on lab.

The OpenHack consists of a series of challenges that reflect the experiences an organization may have as they begin improving or modernize their security, compliance, and identity posture. The challenges cross multiple security functions used to support an organization.

Most teams will **not** complete all the challenges within the time available. This is by-design (it is better to have some stretch-goal challenges for experienced attendees who may get through the challenges unusually quickly than to run out of challenges partway through the event!)

Contoso are a fictitious company who showcase the future of SCI. You are reporting to the CIO (in this case the coaches in the room)

1. **Select a challenge (Complete challenge 1 then any order)** - There are multiple distinct challenges set out within the South Coast Summit Hackathon case study. The focus of these challenges is to learn new skills, ask questions and learn about Zero Trust, Microsoft Entra (Identity), Microsoft 365 Defender and Microsoft Purview (Compliance).

	Also think about what you might be currently doing or planning to do in your own organisation, or what you think should be recommended to be done.

2. **Learn together** - The idea is to share knowledge and ask questions, make your team mates aware of your level of knowledge when it comes to the particular task or tasks at hand and try to chip in as much as possible and remember no questions are silly questions.

3. **Show the coaches what you have impleneted before moving onto next challenge**

4. **Be creative and have fun!**

## Challenge 1 - General Security - Microsoft 365 Secure Score

**Scenario goal:** Discuss the identified Microsoft 365 Secure Score improvements and implement the corrective actions to meet the goals below:
- Identify the first 10-15 improvement actions found in your company’s Microsoft 365 Secure score.
- The CIO knows not all improvement actions can be implemented over night however he would like you to make a start.  Implement at least three improvement actions
- The improvement actions should have their status updated, such as 'Planned' when an implementation is not performed.

## Challenge 2 - Identity & Access Management

### Part 1 - Privileged Identity & Conditional Access
**Scenario goal:** 
Configure conditional access policies to support different security group requirements based on business rules. Configure privileged identity management rules to elevate permissions only when necessary. Establish alerting for risky sign in behavior and enforce a password change policy for sign ins identified as Medium or High.

**General:**
In addition to the scenario goal it MUST also meet the following criteria:
- All accounts must have multi-factor authentication enabled
- Passwords should not be set to expire
- Enforce MFA for users assigned the Security Administrators role.
- All users should accept a "Terms of Use agreement" when accessing any applications outside a trusted location.
- The "Sales & Marketing" group should be allowed to work from anywhere but enforce MFA if not at a trusted location. 
- The "Leadership" group -  These members can only log on from trusted locations
- The "Sales & Marketing" group MUST NOT have access Office 365 applications from IOS or Android devices
- Use an Identity Protection policy to enforce password change when any users risk level is set to Medium or High. If students cannot simulate a risk event to trigger this rule, then at least check that they have the policy configured on PIM.
- Privileged Identity Management must be configured to assign the "Security Administrator" role to Lee Gu, but their default role is User as observed in their profile. (e.g Role is only used when required - Just in Time) This role should be available for a maximum of 2 hours, and a reason to elevate privilege must be provided. Approval from manager for each request is NOT required.

**Helpful notes**
- When testing the conditional access policies, team members can impersonate the volunteer users.
- Trusted locations defined with at least one IP address of a trusted location to sign in from. One of the public IP addresses of a team member is an example of a trusted location access.  

### Part 2 - Identity Governance
**Scenario goal:** 
Configure access reviews on all guest users in the tenants to ensure no guests have extended access to resources when they no longer need them. Create an access package to allow internal users to request access to a set of Teams with an audited approval process.

**General:**
In addition to the scenario goal it MUST also meet the following criteria:
- If a review is not received for guest users, their access should be revoked
- All internal employees should be able to request access to the access package
- Users' line managers should provide the first level of approval
- Named HR users should provide the second level of approval

**Helpful notes:**
- When testing the access packages it is useful to have people signed in as each role to ensure the approval process works as intended

### Part 3 - Single Sign-on for an Enterprise Application - NB. THIS TASK WILL MIGHT TAKE A FEW HOURS
**Scenario goal:** 
Configure a cloud app for single signon.

**General**
Using the Azure AD SAML toolkit:
- Enable SSO via Azure AD to the SAML Toolkit

**Helpful notes:**
- If you already have an application that you want to intergrate to the test tenant such as Facebook developer, twitter developer, GCP, AWS etc you can use that instead. - See here - https://learn.microsoft.com/en-us/azure/active-directory/saas-apps/tutorial-list
- https://learn.microsoft.com/en-us/azure/active-directory/saas-apps/saml-toolkit-tutorial

## Challenge 3 - Compliance Manager
Scenario goal: The team must work together to identify necessary compliance improvement actions and implement the measures where possible. The Compliance manager in Microsoft 365 assessments will determine the improvement actions. Contoso has offices within the UK and EU and must meet the EU GDPR and data protection.
Each team should select three improvement actions whose control maps to the appropriate assessments. If this is not possible, choose the improvement actions with two or more.

The team will:
•	Discover within the assessment which actions are Microsoft's responsibility.
•	Using Challenge 4 below to implement the required controls and report the evidence into the Compliance Manager tool.
•	Apply controls that will improve the compliance posture of the M365 tenant.
•	Implement the corrections and test.
•	Update the implementation status and test status.
•	Verify that remediation has been updated in the assessment and test the implemented controls.
The points achieved should increase as improvement actions are completed, and the status is updated. If there is a delay with the new assessments being run, you can choose the Data Protection Baseline and implement actions from this instead.

The team will report their finding to the coaches.

##  Challenge 4 - Information Protection and Governance + Insider Risk Management + Secure Sharing

Scenario goal:  Your team has been asked by the CISO to implement controls that will significantly impact the organisation’s compliance posture and are looking to execute these improvement actions. 

The CISO is concerned about customer data not being correctly handled and exfiltrated outside the organisation, both intentionally and unintentionally. 
This data is composed of Personal Identifiable Information (PII), bank account information, and credit card information.
The CISO has directed your team to institute policies aligned with the GDPR and data protection baseline to identify and label content. 

You will look to set up a series of top-level labels such as: 
•	“General” and, if any label is downgraded, a business justification must be provided. 
•	Confidential - if any label is downgraded, a business justification must be provided. A header and footer should be applied automatically with the label name.
•	If any content contains customer data, it must be automatically labelled as “Highly Confidential” and needs to be visibly marked as such. If any label is downgraded, a business justification must be provided.
•	Content that looks like a CV or new starter form (once filled out) must be appropriately labelled and restricted so only the HR team can open it. 
Alongside data in Microsoft 365, the Contoso organisation also uses BOX (BOX.com) as one of its corporate repositories. You will also need to scan, discover and label content that equals the requirements above. 

**Part 1 - Protection and Governance**
•	Your team must implement measures designed to protect the company’s data and mark it in accordance with company policy.
•	The company has a documented data classification scheme of Public, General, Confidential, and Highly Confidential. Customer data that resides within the EU is considered Highly Confidential and should not leave the organisation. 
•	In addition to the above classification scheme, HR members have the additional requirements for protecting staff data that contains resume or new starter forms once filled out, and only HR members should have access to it.
•	Data also resides in BOX (box.com), where this company data also needs to conform to this governance framework.

(Task hints: You can create a free BOX developer account for this task: https://developer.box.com/) 
(Task hints 2: You will need some dummy data in your content to trigger on, could try something like: https://generatedata.com/)

**Stretched goal (optional):**

Set up and test a policy that will quarantine and move data away from inside BOX and OneDrive that contains credit card information (this data shouldn’t be stored in these locations in Contoso). 
Ensure that these policies alert security admins via Teams and allow only them to access this information ready for investigation.  The more information they have, the better the evidence.
Update and evidence in the relevant control within the Compliance Manager.

**Part 2 - Insider risk management** 

Contoso Leadership and data protection teams have become very concerned about the threat posed by employees leaving the organisation after a recent incident where a previous employee took customer lists with them. Luckily, Contoso found out that one of the employees accidentally emailed a copy of the customer list they had stolen to someone still at Contoso. 
Leadership & data protection would like to be alerted to potentially risky behaviour for employees who have given notice and performing unusual exfiltration behaviours. They would like to focus on data that contains customer data or content labelled Confidential or Higher. 
The only employee who has given notice in the past week has been Grady Archie.

Success Criteria:
•	Verify and implement the company’s classification scheme using sensitivity policies and labels.
•	Prevent sharing of company data with specified storage locations.
•	Implement Data loss prevention policies and create new insider risk policies to monitor them.
•	Update the relevant controls within the Compliance Manager.

**Stretched goal (optional):** 
Evidence of how the activities and behaviours can include the monitoring for potential access of risky websites where employees are looking to download possible malware or illegal software.

**Part 3 – Secure sharing of confidential data** 
There’s always a balance between security, compliance, and productivity. Now that your team has implemented the necessary controls to monitor and prevent new starter forms from being shared, your HR team's feedback is that they cannot share new starter information with an external partner for payroll. 
You will need to maintain security, compliance, and monitoring for this information that will be shared with your partner “Payroll4U.com”. 
Your team will discuss the possible options on how best to share information with them.

**Success Criteria:** 
Implement change controls in accordance with your GDPR and data protection baseline in Compliance Manager.
Test the relevant controls and set up monitoring, so the security teams have a report once a day if more than 20 instances are shared in one go by a staff member.
Data must be encrypted and labelled to ensure correct data handling.
No other 3rd party apart from Payroll4U should be able to read the new starter forms. 

**Stretched goal (optional):** 
Consider how new starter forms (once filled out) can be shared back to the new staff’s private Gmail (Google mail) accounts securely, set up and test the process.
Update the relevant controls within the Compliance Manager.



## Challenge 5 - Microsoft 365 Defender

### Part 1 - Defender for Endpoint

**Scenario goal:** 
Your team needs to deploy Microsoft Defender for Endpoint (MDE) using Microsoft Intune. You have identified two types of devices: high-risk and low-risk. High-risk devices should be configured with the most protection possible, but low-risk devices can have a lower acceptable security stance to ensure productivity.  The organisation's devices are only Windows. Some iOS BYOD devices are used.

You must:
- Enable MDE integration with Intune. 
- Enable device onboarding with Intune for Windows.
- Configure Endpoint Security Antivirus and Attack Surface Reduction policies that cater to high and low risk scenarios.
- Configure app protection policies to confirm device health using MDE for iOS.
- Configure compliance policies that check device health using MDE for Windows.

### Part 2 - Defender for Office 365

**Scenario goal:** 

Your organisation is migrating from a third-party email protection platform to Exchange Online Protection (EOP) and Microsoft Defender for Office 365 (MDO). You have been tasked with achieving the following objectives:

- The organization should be protected from malicious content in email attachments and files in SharePoint, OneDrive, and Microsoft Teams 
- URLs and their clicks should be trackable and scanned at the time of click.
- Messages with attachments should be detonated in the cloud prior to any mail delivery. 
- Spam should only be available from the quarantine, which users can release.
- Your users should receive quarantine notifications every 3 days.
- Users should be protected from common attachment types but also MP3 and MP4 files.


### Part 3 - Defender for Cloud Apps

**Scenario goal:** 

Your organisation has never had a cloud access security broker (CASB) but are interested in using MDA to discover shadow IT and control the SaaS estate. Using MDA, you should work towards the following objectives:

- If a new OAuth app with high level of permissions but low worldwide prevalence is added to the tenant, administrators should be alerted. 
- If a new file-sharing web app is detected on Windows 10 devices, it should be blocked until an administrator explicitly allows it.
- If files with ransomware-like extensions are detected in OneDrive for Business or SharePoint Online, the uploading user should have their account access blocked.
- If internal users access Office 365 web apps from BYOD devices, their sessions should block all downloads.
- If guests access Office 365 web apps, their sessions should block all downloads unless they have a certificate issued by your organisation.



Link to this repo - https://aka.ms/scs-sci-repo

Feedback form - https://aka.ms/scs-predayscifeedback
