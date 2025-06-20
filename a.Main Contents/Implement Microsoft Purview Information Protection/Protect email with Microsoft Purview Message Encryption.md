
# Understand message encryption
Important to make sure only the intended recipient can read the message.

## **Microsoft Purview Message Encryption**
which lets users send encrypted email to both internal and external recipients even if the recipient uses Gmail, Yahoo, or another non-Microsoft email service.

## How message encryption works
Encryption happens automatically when the message meets the defined conditions, which can be based on keywords, recipient domains, or other criteria

## How message encryption compares to other options

Microsoft 365 includes other encryption technologies that serve different purposes:

- **Information Rights Management (IRM)**: ==Also built on Azure RMS, IRM adds usage restrictions in addition to encryption.== It's a good choice when you need to prevent forwarding, printing, or copying.
    
- **S/MIME**: ==Uses certificates for encryption and digital signing.== S/MIME is often used in government settings or when strict peer-to-peer encryption is required, but it requires more overhead to manage.
    
- **Transport Layer Security (TLS)**: ==Encrypts the connection between mail servers. TLS helps secure data in transit between trusted endpoints but doesn't encrypt the message content itself.==

## Email client support
==One of the key strengths of Purview Message Encryption is that it works across many platforms, including Outlook for desktop, mobile, and web. External recipients using Gmail, Yahoo, or other services can access encrypted messages through a secure web portal. They don't need to install special apps or sign in with a Microsoft 365 account.==

## Choosing between encryption templates and sensitivity labels

In Microsoft 365, you can apply encryption in two primary ways:
- **Encryption templates**, used in mail flow rules or configured manually by admins
- **Sensitivity labels**, which allow users to classify and protect content themselves

## When to use Advanced Message Encryption

Advanced Message Encryption builds on the base encryption experience and provides more granular control over external access. With this feature, you can:
- Expire access to encrypted messages after a specific time
- Revoke access to a message after it's has been sent
- Apply custom branding and ensure recipients use the secure portal

## Verify Azure Rights Management is active


Run the following command to verify that Azure RMS licensing is enabled:

```
Get-IRMConfiguration
```

Check that the AzureRMSLicensingEnabled value is set to True.


- Then run a test to verify encryption is working:
```
Test-IRMConfiguration -Sender user@contoso.com -Recipient user@contoso.com
```


## Create and configure encryption templates
```
Get-RMSTemplate
```

## Set expiration dates for encrypted emails

```
New-OMEConfiguration -Identity "Expire in (X) days" -ExternalMailExpiryInDays X
```

change x to integer



## Revoke access to encrypted emails

### Revoke as the sender
- In Outlook on the web, go to your **Sent Items** folder.
- Open the encrypted message.
- If the message is eligible for revocation, you'll see a **Remove external access** option at the top of the message. Select it to revoke access.

### Revoke as an administrator

1. Identify the message ID using a message trace or encryption report in the Microsoft Purview portal.
2. Connect to Exchange Online PowerShell.
3. Run this command to revoke the message:

 ``` 
 Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
```

To confirm revocation:
```
Get-OMEMessageStatus -MessageId "<messageId>" | ft Subject, Revoked
```

## Monitor encrypted message activity

Enable tracking logs for the encrypted message portal:
```
Set-IrmConfiguration -EnablePortalTrackingLogs $true
```
