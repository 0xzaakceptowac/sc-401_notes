# Data loss prevention overview
* ==Data Loss Prevention (DLP) helps address this by identifying, monitoring, and safeguarding sensitive information across your organization's digital environment.==
* These policies detect and respond to specific types of data, such as credit card numbers or personal identification details, ensuring that sensitive information is protected and managed effectively.

# Plan and design DLP policies
* When planning for DLP, consider your organization's specific needs.
* . What kind of sensitive information you handle, where it's stored, and how it's shared

## Steps to plan a DLP deployment

1. **Identify stakeholders**: ==Planning and implementing DLP requires input from across the organization.== This ensures that policies are comprehensive and reflect both legal requirements and business needs. Common stakeholders include:

- IT and security teams
- Compliance officers
- Legal and risk management teams
- Data owners and business unit leaders

2. **Define categories of sensitive information**: Once stakeholders are identified, the next step is to define the categories of data your organization must protect. These categories could include:

- Financial data
- Personal information
- Intellectual property
- Any other sensitive or regulated information

3. Set Goals and strategies

4. **Determine where DLP will be applied**: DLP policies can be applied across a wide range of platforms

- **Exchange Online** for email
- **SharePoint** and **OneDrive** for stored and shared files
- **Microsoft Teams** for chat and shared documents
- **Office applications** like Word, Excel, and PowerPoint
- **Windows 10**, **Windows 11**, and **macOS** (latest three versions) for endpoint protection
- **Non-Microsoft cloud apps** monitored through Microsoft Defender for Cloud Apps
- **On-premises file shares** and on-**premises SharePoint**
- **Microsoft Fabric** and **Power BI** for data analytics and reporting


## Three axes of DLP deployment management

When you deploy a DLP policy, three main factors need to be considered:

- State of the policy
- Scope of the policy
- Actions taken by the policy

### State of the policy

==DLP policies can be set to different states depending on where they are in the deployment process==. The state determines whether the policy is active, inactive, or running in simulation mode.


### Scope of the policy

==The scope defines where the policy applies==. You start by choosing locations like Exchange, SharePoint, Teams, or devices. By default, the policy covers all instances in that location. You can then include or exclude specific instances, like certain sites, users, or groups.


### Actions taken by the policy

==Actions define how a DLP policy responds to policy violations.== These actions can range from passive monitoring to full enforcement:

## Understand simulation mode

==Simulation mode allows you to see how a DLP policy would behave in your environment without fully enforcing it.== This mode runs as if the policy were fully deployed, but no actions are taken, so there's no effect on user activity or business processes.

### How simulation mode works

Simulation mode provides insights across all supported locations:

- **Real-time scanning**: ==For locations like Exchange, Teams, and endpoints, content is scanned in real-time as new items are created or modified.==
- **Scans for existing content**: ==For SharePoint and OneDrive, simulation mode scans both new and existing items, providing a comprehensive view of how the policy would affect them.==

### Permissions

To create, manage, or deploy DLP policies, your account must be part of one or more of these role groups:

- Compliance Administrator
- Compliance Data Administrator
- Information Protection Admin
- Security Administrator


# Integrate Adaptive Protection with DLP
==Adaptive Protection in Microsoft Purview works alongside Microsoft Purview Insider Risk Management to automatically adjust data loss prevention (DLP) policies based on user behavior.== This adaptive approach ensures that data protection evolves as risk levels associated with specific users change.


## How Adaptive Protection works

- **Dynamic risk levels**: ==Users are assigned a risk level based on their behavior, which updates automatically as new information about their actions emerges.==
    
- **DLP policy integration**: ==Adaptive Protection adds the **Insider risk level for Adaptive Protection is** condition to DLP policies.== This allows DLP rules to apply different protections for users based on their risk level in services such as Exchange Online, Teams, and Devices.



#### Adaptive Protection policy for Teams and Exchange DLP

Quick setup generates one policy for both Teams and Exchange, which includes two rules:

- **Block Rule for Elevated Risk Level**: Blocks content from being shared externally, notifying the user with a policy tip.
    
- **Audit Rule for Moderate and Minor Risk Levels**: Allows content sharing but logs the event for auditing purposes.
    

#### Adaptive Protection Policy for Endpoint DLP

For endpoint devices, quick setup creates more restrictive policies, depending on the user's risk level:

- **Block Rule**: If a user is at an Elevated Risk Level, actions such as copying data to USB drives, cloud services, or printing sensitive information might be blocked.
    
- **Audit Rule**: For Moderate and Minor Risk Levels, the same actions might be audited but not blocked, providing visibility into potential risks without disrupting workflows.

## Enable DLP analytics

==DLP analytics is turned **off** by default ==and needs to be manually enabled. It takes seven days for recommendations and insights to appear after activation.