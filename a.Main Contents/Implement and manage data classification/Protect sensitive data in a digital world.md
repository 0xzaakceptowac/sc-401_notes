# Understand data classification and protection
* Before organizations can effectively protect their data, they need to identify what data they have and assess its sensitivity.
* As data volumes grow, organizations face increased risks of accidental exposure, unauthorized access, and regulatory noncompliance.
## KEYPOINTS

- **Data classification** to categorize information based on sensitivity.
- **Sensitivity labels** to define and enforce handling rules.
- **Encryption** to protect data from unauthorized access.
- **Data loss prevention (DLP) and retention policies** to ensure compliance and prevent accidental leaks.
# Components of data classification and protection
## Data classification
* ==helps organizations identify and categorize sensitive information==, making it easier to apply appropriate security controls.

### Microsoft Purview - Data classification
- **Sensitive information types**: ==Predefined and customizable patterns that detect data== such as financial records, personal identifiers, and healthcare information.

- **Trainable classifiers**: ==AI-powered classifiers that recognize sensitive content based on real-world examples==, improving detection accuracy for unstructured data.

## Sensitivity labels
* Sensitivity labels ==classify and protect data by enforcing encryption, access control, and visual markings.==
### Microsoft Purview - Sensitivity labels
* **Classify and protect data** with ==persistent labels that travel with content== across emails, files, and cloud services.
- **Apply automatic or manual labels** based on content inspection and policy rules.
- **Restrict file sharing and enforce access controls** to ==ensure only authorized users can access or modify data.
- **Apply encryption** to ==protect information at rest and in transit.
- **Add visual markings** such as ==headers, footers, and watermarks to indicate data sensitivity.*

## Encryption
* ==Encryption secures data by converting it into an unreadable format, ensuring that only authorized users can access it. It protects information at rest, in transit, and in use to prevent unauthorized exposure.==
### Microsoft Purview -Encryption
- **Sensitivity labels in Microsoft 365 apps**: Encrypt emails and files in Outlook, Word, Excel, and PowerPoint with automatic encryption based on classification and security policies.
- **Microsoft Purview Information Protection scanner**: Discover, classify, and encrypt sensitive data across on-premises locations.
- **Microsoft Purview Message Encryption**: Encrypt email communication for secure messaging inside and outside the organization.

## Data loss prevention (DLP) and retention policies
* ==DLP policies help organizations prevent accidental data leaks by monitoring and restricting data movement based on sensitivity.== 
* Retention policies ensure that critical business information is preserved for compliance purposes.

### Microsoft Purview -DLP

- Detect and block unauthorized data sharing across cloud and endpoint environments.
- Enforce automatic retention or deletion of data based on compliance requirements.
- Monitor and analyze policy violations to improve security strategies.



# Mitigation strategies
## Microsoft Purview Insider Risk Management
- Detect unusual file access, data transfers, and security violations.
- Identify risky behavior while maintaining user privacy.
- Automate risk alerts and investigations to reduce response times.

## Implement DLP policies
- Prevent data leaks across email, cloud services, and endpoints.
- Enforce restrictions on copying, pasting, or transferring sensitive files.
- Apply policies dynamically to protect regulated data and intellectual property.

## Use Adaptive Protection
* ==Adaptive protection adjusts security controls based on real-time risk insights from insider risk management== ensuring that sensitive data is only accessible under safe conditions.
### Microsoft Purview uses Adaptive Protection
- Assess user activity and apply security policies dynamically.
- Restrict data access for users exhibiting risky behavior based on Insider Risk Management signals.
- Reduce unnecessary security friction for trusted users.

# Manage security alerts and respond to threats
## Microsoft Purview Audit
* ==Organizations must be able to track and investigate user activities across their environment to identify security incidents. ==
* **Microsoft Purview Audit** provides detailed visibility into user actions, helping security teams detect unusual behavior, unauthorized access, and policy violations.
Sec team can:
- Review user activity logs to investigate security incidents.
- Identify unauthorized access attempts and detect unusual behavior.
- Use Audit (Premium) capabilities to retain logs for long-term forensic analysis.
## Alerts in Microsoft Purview
* Alerts are managed within specific Purview solutions, ==such as Insider Risk Management and Data Loss Prevention (DLP)==, allowing security teams to address risks in their relevant contexts.
Sec team can:
- Monitor security and compliance alerts directly within Insider Risk Management, DLP, and other Microsoft Purview solutions.
- Take immediate action on alerts within Microsoft Purview tools to prevent security incidents.
- Prioritize alerts based on severity and risk to focus on the most critical incidents.
## Activity and content explorer
* Security teams need to understand how data is accessed, shared, and classified within an organization. 
* ==**activity explorer** and **content explorer** provides real-time insights into user activities and content classification, helping security teams monitor security events.
*  **Activity explorer**: ==Provides insights into user activity, tracking data access, movement, and security events.
- **Content explorer**: ==Helps security teams view and classify sensitive data across Microsoft 365 applications, identifying potential risks.

## Microsoft Defender XDR
* provides a unified threat detection and response capability by correlating security signals from multiple sources.

# AI

## Use Data Security Posture Management (DSPM) for AI to enforce security policies and manage AI-related risks.

## Implement **AI governance policies** to define acceptable AI-generated content.

## **Implement Data Loss Prevention (DLP) policies** to prevent unauthorized data from being used in AI tools.