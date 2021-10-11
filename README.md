# Welcome to the SCI Hack Challenge @ South Coast Summit  
----------------------------------------------------------------------------------------------------

![image](https://github.com/AllyT-MS/south-coast-summit-sci/blob/main/scs.png)

## OpenHack - An Introduction for Attendees

OpenHack is a hands-on experience in which participants work in team to solve a series of coding challenges based on the requirements and resources provided. It is *not* designed to be delivered as a traditional training session or hands-on lab.

The OpenHack consists of a series of challenges that reflect the experiences an organization may have as they begin improving or modernize their security, compliance, and identity posture. The challenges cross multiple security functions used to support an organization.

Most teams will **not** complete all the challenges within the time available. This is by-design (it is better to have some stretch-goal challenges for experienced attendees who may get through the challenges unusually quickly than to run out of challenges partway through the event!)

Contoso are a fictitious company who showcase the future of SCI. 

**1 - Select a challenge (Complete challenge 1 then any order)**
	· There are multiple distinct challenges set out within the South Coast Summit Hackathon case study. The focus of these challenges is to learn new skills, ask questions and learn about Zero Trust, Microsoft Identity, Microsoft Defender and Data Compliance.
**2 - Learn together**
	· The idea is to share knowledge and ask questions, make your team mates aware of your level of knowledge when it comes to the particular task or tasks at hand and try to chip in as much as possible and remember no questions are silly questions.
**3 - Show the coaches what you have impleneted before moving onto next challenge**
**4 - Be creative and have fun!**

## Challenge 1 - Secure Score

**Scenario goal:** Discuss the identified Microsoft 365 Secure Score improvements and implement top 3-5 corrective actions. 

## Challenge 2 - Identity & Access Management

**Scenario goal:** Configure conditional access policies to support different security group requirements based on business rules. Configure privileged identity management rules to elevate permissions only when necessary. Establish alerting for risky sign in behavior and enforce a password change policy for sign ins identified as Medium or High.

### General

Solution should include creating the following:

- Conditional access rule for that will enforce MFA for users assigned the Password Administrators role.

- Conditional Access rule for the "General Staff" group that allow them to work from anywhere but enforces MFA if not at a trusted location. 

- Conditional Access rule for the "Financial System Access" group. These members can only log on from trusted locations. 

- When testing the conditional access policies, team members can impersonate the volunteer users.

- Trusted locations defined with at least one IP address of a trusted location to sign in from. One of the public IP addresses of a team member is an example of a trusted location access.  

- Identity Protection policy setup to enforce password change when any users risk level is set to Medium or High. If students cannot simulate a risk event to trigger this rule, then at least check that they have the policy configured on PIM.

- Privileged Identity Management configured to assign the "Password Administrator" role to Julian Isla, but their default role is User as observed in their profile.

## Challenge 3 - Compliance Manager

**Scenario goal:** The team must work together to identify necessary compliance improvement actions and implement the actions where possible. The Compliance manager in Microsoft 365 assessments and regulatory compliance in the Azure Security center will be used to identify the improvement actions.

Each team member will be assigned or select three improvement actions whose control maps to all three assessments. If this is not possible, choose the improvement actions that have two or more.  
The team members will:

- Implement the corrections and test.

- Update the implementation status and test status.

- Verify remediation has been updated in the assessment.  

The points achieved should increase as improvement actions are completed and the status updated.
For actions that cannot be performed in the OH environment, the team member must be able to describe how this was implemented and tested.  
The team will report their finding to the coaches


## Challenge 3 - Information Protection and Governance + Insider Risk Management

**Scenario goal:** Deploy policies and configurations that support information protection and governance and insider risk management. 

### General

At the end of this challenge, the team will have:
Labeling:
- Created five sensitivity labels
    - Public
    - General
    - Confidential
    - Highly Confidential
    - Attorney Client Privilege 
- Created two sensitivity label policies
    - An org-wide policy
    - A policy scope to the Legal group
- Created a custom sensitive information type
    - Defines the keyword "ACP" 

Data loss prevention:  

- Created a DLP policy to prevent the sharing of customer data.

    - The policy will need to be applied to Exchange, Teams, SharePoint, and Devices.

    - Define the endpoint DLP settings to block Google Drive and Box and Copy to a USB removable media.

Insider risk management:  

- Created a data theft by departing users policy


## Challenge 4 - Microsoft 365 Defender

**Scenario goal:** 
The team must run a simulated attack against a test device in the Microsoft Defender Security Center. Once complete, the team should be able to identify different elements of the attack. Additionally, the team must create one advanced hunting rule that identifies antivirus reports from a specific target device. 

### General

At the completion of this challenge, the team will have successfully executed the ATP29 attack simulation against one of the test devices. They will have created and saved an advanced hunting query.

## Challenge 5 - Endpoint Management

**Scenario goal:** 

The team will be expected to configure Microsoft Endpoint Manager to automatic enrollment devices based on a user's group membership and enable Microsoft Defender for Endpoint in Intune so that it can be used when onboarding devices. Using the newly onboarded device, the team will run an attack simulation from Microsoft Defender for Endpoint and analyze the attack. For employees, the team will use the attack simulator in Microsoft 365 security to deploy simulated attacks against target mailboxes and experience some available methods that can be used to help educate and evaluate readiness.

### General
When complete, the team will have deployed features in found in Microsoft Endpoint Manager to include automatic enrollment of devices and deployment of Microsoft Defender for Endpoint using Intune. The team will have used a simulated attack against a deployed workstation and evaluated the event in Microsoft Defender for Endpoint. Finally, the team will test the capabilities of the attack simulators found in Microsoft 365 security.


Link to this repo - https://aka.ms/scs-sci-repo

Feedback form - https://aka.ms/scs-predayscifeedback









