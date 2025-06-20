[Data Classification][obsidian://open?vault=sc-401_notes&file=a.Main%20Contents%2FImplement%20and%20manage%20data%20classification%2FClassify%20data%20for%20protection%20and%20governance]
# **Information Protection Reports** 
* ==Microsoft Purview provide a centralized view of data classification, protection policies, encryption, and security activities across Microsoft 365==, Azure, AWS, on-premises storage, and Microsoft Fabric

- **Monitor sensitivity label adoption**: ==Identify how labels are applied across cloud and on-premises data.==
- **Assess protection coverage**: ==Detect unprotected data across multicloud environments.==
- **Analyze user interactions with labeled content**: ==Track data access, movement, and policy violations.==
- **Review encryption trends**: ==Verify email and file encryption across multiple platforms==.
- **Gain insights into Microsoft Purview Data Governance sources**: Track sensitive data within governed data estates.
- **Monitor findings from the Microsoft Purview Information Protection (MIP) scanner**: Identify sensitive data in on-premises file shares and SharePoint.

## Deeper insights

- **Data explorer**: ==Provides detailed visibility== into labeled and sensitive content.
- **Activity explorer**: Shows how ==users interact with labeled data.==
- **Protection policies (preview)**: Helps ==assess and adjust protection== settings.
- **Scan reports**: ==Displays details of scanned content across cloud== and on-premises storage.
- **Encryption reports**: Tracks ==email encryption and protection trends.==

| Report                                 | Details                                                                                                           | Purpose                                                                 | Linked                        |
| -------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------- |
| **Sensitivity label coverage**         | ==Percentage of labeled vs. unlabeled items== across Microsoft 365, Azure, AWS, and on-premises.                  | Ensures sensitive data is labeled for proper protection and governance. | Data Explorer                 |
| **Sensitivity label usage**            | ==Top sensitivity labels applied to files== across all connected environments.                                    | Helps track label adoption trends and identify policy gaps.             | Data Explorer                 |
| **Sensitive information taypes (SITs)** | ==Most commonly detected sensitive data types (for example, credit card numbers, SSNs, medical data).==           | Helps identify high-risk data needing protection.                       | Data Explorer                 |
| **Data sources with sensitive info**   | ==Top locations where labeled or sensitive data is stored== (for example, SharePoint, OneDrive, Exchange, Azure). | Identifies data concentration areas to enhance security controls.       | Data Explorer                 |
| **Trainable classifiers**              | ==Most-used AI classifiers for autolabeling== (for example, threat intelligence, HR records).                     | Supports automated classification for large-scale data protection.      | Data Explorer                 |
| **Top activities detected**            | ==Logs of file access, labeling changes==, DLP matches, and encryption actions.                                   | Detects unauthorized modifications or suspicious access patterns.       | Activity Explorer             |
| **Data scanning summary**              | ==Percentage of scanned data sources across cloud and on-premises.==                                              | Detects unscanned areas that might pose compliance risks.               | Scan reports                  |
| **Email encryption summary**           | ==Number of emails encrypted manually== or by policy.                                                             | Ensures confidential emails are properly protected.                     | Encryption reports            |
| **Protection coverage**                | ==Percentage of encrypted and access-controlled data across cloud and on-premises sources.==                      | Identifies gaps in encryption and access control policies.              | Protection policies (preview) |

# Analyze classified data with data and content explorer

- **Data explorer** ==provides a consolidated view of classified data==, making it easier to analyze multiple classification types at once.
- **Content explorer** ==offers similar insights but requires more navigation to see classification details.==

These tools help security and compliance teams:

- **Identify sensitive data** across Microsoft 365 and connected environments.
- **Analyze data classification trends** based on sensitivity labels, retention labels, and sensitive information types (SITs).
- **Review access patterns** to detect potential security risks.
- **Validate compliance policies** by verifying encryption, classification, and retention settings.
### Permissions

Access to these tools is highly restricted because they allow visibility into sensitive data. Permissions override local file access settings.

| Role                            | Access level                                                  |
| ------------------------------- | ------------------------------------------------------------- |
| Data Explorer List Viewer       | View file metadata and classification labels but not content. |
| Data Explorer Content Viewer    | View file contents in addition to metadata.                   |
| Content Explorer List Viewer    | View a list of items with classification details.             |
| Content Explorer Content Viewer | View file contents in addition to metadata.                   |

| Feature                                         | Data explorer                                                                                                                            | Content explorer                                                                                                            |
| ----------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Data organization and visibility                | Shows sensitive information types, sensitivity labels, trainable classifiers, and retention labels in a single table for quick analysis. | Requires navigating into each location to view classification details, rather than displaying them in a consolidated table. |
| Integration with Information Protection Reports | Links directly from information protection reports, allowing users to drill into classification details.                                 | Not linked from reports, so users must navigate to content explorer manually.                                               |
| Copilot data visibility                         | Includes Copilot as a data source when applicable.                                                                                       | Doesn't list Copilot as a distinct source.                                                                                  |
# Monitor and review actions on labeled data

**Activity explorer** in Microsoft Purview ==allows security and compliance teams to track how labeled content is accessed, modified, and shared.== By analyzing activity trends, organizations can assess policy effectiveness, detect potential security risks, and refine data protection measures.

## Why use Activity explorer?

- **Monitor classified data usage**: ==Track how labeled content is accessed, modified, or shared.==
- **Audit policy effectiveness**: ==Identify compliance gaps by analyzing data loss prevention (DLP) matches, labeling changes, and file actions.==
- **Refine analysis with filters**: ==Apply filters for date, user, activity type, sensitivity label, location, and more.==
- **Use predefined filter sets**: ==Quickly view activities such as labeling changes, DLP detections, and endpoint data movement.==
- **Use Security Copilot (preview)**: ==AI-driven insights detect anomalies, analyze patterns, and suggest policy refinements.==

## Access Activity explorer

### Permissions

Users must be assigned one of the following roles or role groups in Microsoft Purview or Microsoft 365.

| Category          | Roles                                                                                                                                                | Role groups                                                                                                                                                                            |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Microsoft Purview | - Information Protection Admin  <br>- Information Protection Analyst  <br>- Information Protection Investigator  <br>- Information Protection Reader | - Information Protection  <br>- Information Protection Admins  <br>- Information Protection Investigators  <br>- Information Protection Analysts  <br>- Information Protection Readers |
| Microsoft 365     | - Compliance Admin  <br>- Security Admin  <br>- Compliance Data Admin                                                                                | - Compliance Administrator  <br>- Security Administrator  <br>- Security Reader                                                                                                        |

## Activity Explorer predefined filter sets

Filter sets help quickly identify specific activities. Activity explorer includes built-in filter sets such as:

- **Endpoint DLP activities**: Actions on files from managed devices.
- **Sensitivity label changes**: Applied, changed, or removed labels.
- **Egress activities**: Data movement outside the organization. Use this to detect potential data exfiltration.
- **DLP detections**: Activities triggering DLP policies.
- **Network DLP activities**: Data movement across monitored networks.
- **Protected Browser**: Track actions within secure browsers. Useful for monitoring activity in Microsoft Edge with security policies enabled.

## Security Copilot in Activity explorer (preview)

Microsoft **Security Copilot** enhances Activity explorer with AI-driven insights, helping identify security risks, policy violations, and suspicious activity.

AI-driven capabilities include:

- **Data hunting**: Use machine learning to surface critical data activity.
- **Prompt-based filtering**: Enter natural language queries to generate filter sets.
- **Investigative assistance**: Drill down into suspicious activities.