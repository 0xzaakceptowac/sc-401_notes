# Sensitivity label overview
You can use sensitivity labels for:

- **Encryption and content markings**: Apply labels like _Confidential_ to encrypt documents and emails and add watermarks, headers, and footers. Encryption restricts actions for authorized users.
- **Cross-platform content protection**: Protect content across Office apps on various platforms, including desktop and web on Windows, macOS, iOS, and Android.
- **Non-Microsoft app protection**: Secure content in apps like SalesForce, Box, or DropBox with Microsoft Defender for Cloud Apps.
- **Container protection**: Manage privacy and access settings for Teams, Microsoft 365 Groups, and SharePoint sites.
- **Meeting and chat Security**: Secure Teams meetings and chats with encryption and specific access controls.
- **Data intelligence**: Integrate labels with Power BI and Microsoft Purview Data Map to safeguard data across services.
- **Non-Microsoft app extension**: Integrate sensitivity labels with external apps using the Microsoft Purview Information Protection SDK for consistent data protection.
- **Visual marking**: Label data without enforcing protection, allowing for future application of security measures.
- **Microsoft Copilot integration**: Use sensitivity labels within Microsoft Copilot to ensure data protection during interactions.

## Application of sensitivity labels

To apply sensitivity labels, users must sign in with their Microsoft 365 work or school account. ==These labels, part of Microsoft Purview, are designed to help organizations manage the sensitivity of their data consistently across the digital environment.==

### What sensitivity labels are

Sensitivity labels are like customizable stamps for your organization's content. They are:

- **Customizable**: Tailored to your organization's needs, categorizing content into levels like _Personal_, _Public_, _General_, _Confidential_, and _Highly Confidential_.
- **Clear text**: Stored in clear text, making them readable by non-Microsoft apps for more protective actions.
- **Persistent**: Remain with content wherever it's saved or stored, enforcing your organization's policies.

### What sensitivity labels can do

Once applied, sensitivity labels enforce protection settings on emails, meeting invites, and documents. Configurations can include:

- **Encryption and content marking** to restrict access and visually mark the content.
- **Container protection** for collaborative tools like Teams, Microsoft 365 Groups, and SharePoint sites.
- **Auto-labeling** to automatically classify files and emails or to prompt users for labeling.

#### Editing or deleting a sensitivity label
==If you delete a sensitivity label from the Microsoft Purview portal, the label isn't automatically removed from content. Any protection settings continue to be enforced on content that had that label applied.==


### What label policies can do

==After you create your sensitivity labels, you need to publish them to make them available to people and services in your organization.== The sensitivity labels can then be applied to Office documents and emails, and other items that support sensitivity labels.

- **Publish to users and groups**: Unlike retention labels that are often applied to locations like Exchange mailboxes, sensitivity labels are assigned to specific users or groups.
- **Default label for content**: Policies can set default labels for content such as documents, emails, meeting invites, and new containers like Teams and SharePoint sites.
- **Require justification for label changes**: Policies can require users to give a reason when changing a label, especially if it lowers the data's sensitivity level.
- **Mandatory labeling for certain content**: Some types of content might need to have a label before actions like saving, sending, or sharing are allowed.
- **Help links for users**: Policies can include customized help links for more guidance on label use.
- **Policy priority (order matters)**: The order of label policies shows their priority, affecting how settings are applied in cases of conflict.
- **Policy application time**: It might take up to 24 hours for changes in label policies to fully apply across an organization.


# Create and configure sensitivity labels and label policies

Sensitivity labels are critical for protecting sensitive information, meeting compliance requirements, and supporting secure collaboration across the organization.

## How sensitivity labels work

![[Pasted image 20250619095915.png]]


# Implement auto-labeling policies
* Automating sensitivity labeling helps manage sensitive information across SharePoint Online, OneDrive, and Exchange Online

* Auto-labeling policies automatically apply sensitivity labels to emails, documents, and other content across Microsoft 365. This process helps organizations protect sensitive data consistently ==without relying on users to manually classify every piece of content.==

There are two ways to automatically apply sensitivity labels in Microsoft 365:
- **Client-side labeling**: Office apps recommend or automatically apply labels while users are working in Word, Excel, PowerPoint, or Outlook.
- **Service-side labeling**: Labels are applied automatically to stored content in SharePoint, OneDrive, and Exchange, even if users don't interact with the content.

