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
Scenario goal: The team must work together to identify necessary compliance improvement actions and implement the measures where possible. The Compliance manager in Microsoft 365 assessments will determine the improvement actions. Contoso has offices within the UK and EU and must meet the EU GDPR and the GDPR.
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

##  Challenge 4 - Information Protection and Governance + Insider Risk Management + Secure Sharing** 

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
Stretched goal (optional):

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



## Challenge 4 - Microsoft 365 Defender

**Scenario goal:** 
Earlier, the CIO notified the CISO and team that they are currently working with vendors who will be helping evaluate the security team’s readiness to protect the company’s assets. Your team needs to deploy a lab in Microsoft Defender for Endpoint to evaluate the product. The team now needs to become familiar with its capabilities and run simulations to see Microsoft Defender for Endpoint’s prevention, detection, and remediation features in action.

The team must run an attack delivered by SafeBreach that simulates techniques such as malware infection, data collection and modification of registry keys. This simulated attack should be run against one of the deployed evaluation lab virtual machines.

The team must run a simulated attack against a test device in the Microsoft Defender Security Center. Once complete, the team should be able to identify different elements of the attack. Additionally, the team must create one advanced hunting rule that identifies antivirus reports from a specific target device. 

### Part 1 - Defender for Endpoint

After the simulation is complete, the team must identify any high severity incidents. The team must be able to answer the following questions:
1. What categories does the incident fall under?
2. Was there a payload or multiple payloads and what were they?
3. If there was malware, what malware was identified?
4. Can a hacker or bad actor group be identified? If so, who?

### Part 2 - Defender for Office 365
Contoso Mortgage has had regular annual cyber security training for its employees for nearly three years. In the past, the CIO has chosen not to use any in-house or third-party email-based attack simulations and relied on the online training to educate employees. With most employees now working remotely, this is being reconsidered. Your team must use the available attack simulator feature to execute simulated attacks. Using the two spear phishing attacks, launch an attack targeting members of your team. After team members receive the emails, review the messages, and brief the team on identified items that should alert the recipient of danger. Be prepared to explain your findings to the CISO. Additionally, each one of the attack messages’ payloads should be triggered for the team to understand the simulated attack experience. The CISO is okay with the team creating their own templates or using the built-in templates.

In addition to the goals above the following MUST also be met:
- The organization should be protected from malicious content in email attachments and files in SharePoint, OneDrive, and Microsoft Teams 
- Messages with attachments should be immediately delivered while the attachments are scanned.
- Phishing thresholds should be set to at least 2. 
- Your users should receive spam notifications every 3 days.
- Users should be protected from common attachment types.

## Challenge 5 - Endpoint Management
**Scenario goal:** 
The company has transitioned from the more traditional work-from-office approach to remote workers. Although working from home or working remotely gives employees more flexibility throughout the day, it does present additional security concerns for the company. The company cannot control the employee’s home network nor can it deny network access to other devices that may be present on someone’s home network. With the proliferation of IoT devices in homes, potential access vectors for bad actors to infiltrate company assets increases with every newly deployed smart device.

Contoso is moving from their traditional on-premises based device hygiene and management system to their already licensed Microsoft Endpoint Manager integrated endpoint management platform. Microsoft Intune in Endpoint Manager will be used for the mobile device and application management of Windows, macOS, iOS, and Android devices. 
The initial focus will be on company purchased hardware that has been issued to the employees and Windows devices in particular. All Windows devices will eventually be enrolled in Microsoft Intune automatically.

Allan Deyoung will be delivering the EndPoint Manager features so will need to be given appropriate permissions, including being a member of the Help Desk group. He will lead the team to help test the planned Windows devices’ automatic enrollment and compliance configurations before including all employees in automatic enrollment.

Prior to launching simulated attacks, the CISO wants the team to integrate Microsoft Defender for Endpoint with Microsoft Intune as a mobile threat defense solution

**General:**
The profile should be assigned to the Windows 10 Enterprise and Windows 10 Professional OS editions: the approved Windows desktop operating systems in the company. Additional configuration settings do not need to be configured.

The team must also create compliance and conditional access policies for Windows 10 devices in Endpoint Manager.
The compliance policy will require Windows 10 devices to be at or under the machine risk score of High. If a device is not compliant, it should be marked as such immediately. The policy should be assigned to the testing group that Larry is a member of.

The conditional access policy should control the testing groups access to Office 365 cloud apps when using modern authentication clients or legacy authentication clients. Access should require a device to be marked as compliant or when using multi-factor authentication. For now, the policy should only report violations and exclude non-Windows based devices.

**Success Criteria:**
- Enable automatic enrollment of Windows devices.
- Enable Microsoft Defender for Endpoint with Intune. 
- Create a configuration profile to onboard devices into Microsoft Defender for Endpoint.
- Create a compliance policy for Windows devices that enforces company compliance requirements.
- Create an access control policy to protect Office 365 apps.
- Enroll test laptop (ask coach to borrow one) in device management.

Link to this repo - https://aka.ms/scs-sci-repo

Feedback form - https://aka.ms/scs-predayscifeedback
