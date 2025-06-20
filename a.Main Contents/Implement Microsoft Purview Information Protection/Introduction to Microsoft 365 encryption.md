==Encryption is the process of encoding information to ensure its confidentiality from those who don’t possess a unique key.== Using encryption protects data against theft, failures in physical security, and eavesdropping on data-in-transit. Depending on the type of encryption, one or more keys may be used. These keys provide the ability to read data that has been made unintelligible by encryption. Keys can be used to encrypt data, decrypt data, or both.


## **Examples of data-at-rest** 
include files uploaded to a SharePoint library, Teams chat messages, documents uploaded in Microsoft Teams meetings, email messages and attachments ==stored in mailbox folders, and files uploaded to OneDrive for Business.==

## **Examples of data-in-transit**
include email messages that are in the process of being delivered or conversations that are taking place in an online meeting. ==Data is in transit whenever a user's device is communicating with a Microsoft server, or when Microsoft servers are communicating with one another.==



# How Microsoft 365 data is encrypted at rest
All customer content at rest in Microsoft 365 is protected by one or more forms of encryption. BitLocker is used on disk drives at the volume level,


## BitLocker volume level encryption

* BitLocker is deployed with Advanced Encryption Standard (AES) 256-bit encryption on disks containing customer data. 
* Disk sectors are encrypted with a Full Volume Encryption Key (FVEK), which is itself encrypted with the Volume Master Key (VMK), which in turn is bound to the Trusted Platform Module (TPM) in the server.

## Service level encryption
Exchange Online, Microsoft Teams, SharePoint Online, and OneDrive for Business all use service level encryption to ==provide an additional layer of security for customer data-at-rest.==

![[Pasted image 20250619125820.png]]

## Customer key
Customer Key allows customers to use their own root keys to encrypt their data. Customer keys are uploaded to or generated within Azure Key Vault, allowing customers to control the ability of Microsoft services to decrypt and process customer data. This option is currently available for Exchange Online, SharePoint Online, and OneDrive for Business.

### Availability key
For customers who use the Customer Key feature, Microsoft 365 provides data recovery capabilities using availability keys. The primary purpose of the availability key is to provide recovery capability from the unanticipated loss of customer-managed root keys, including key loss from mismanagement or malicious action. If customers lose control of their root keys, Microsoft Support can initiate recovery at the customer's request using the availability key.