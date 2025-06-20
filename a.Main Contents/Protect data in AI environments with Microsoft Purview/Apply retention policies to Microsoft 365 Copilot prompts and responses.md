Microsoft Purview Data Lifecycle Management plays a key role in managing content retention and deletion in Microsoft 365. It helps organizations meet regulatory requirements and reduce risk by deleting data that's no longer needed. ==Retention policies let you control how long to keep content in services like Exchange, SharePoint, OneDrive, Teams, and Viva Engage. ==You can retain content indefinitely, keep it for a set period, or delete it after a defined time.

Retention management is especially important for content generated through AI interactions, including Microsoft 365 Copilot. These policies help ensure compliance while supporting responsible data practices.


## How Copilot messages are retained

==Retention for Copilot relies on the Exchange Online mailbox of the user who initiates the Copilot interaction. ==Messages are copied to a hidden folder within that mailbox. This folder isn't visible to users but is accessible to compliance administrators using eDiscovery.


Retention behavior is governed by the policy type and the Exchange timer job, which runs every 1–7 days. If the message reaches the end of its retention period:

- It's moved to the hidden SubstrateHolds folder.
- It's retained there for at least one day.
- It's permanently deleted unless another retention policy, eDiscovery hold, or Litigation Hold applies.

# Investigate and delete Copilot interactions with Microsoft Purview eDiscovery

==Microsoft Purview eDiscovery helps organizations identify, investigate, and take action on electronically stored information (ESI). ==When Microsoft 365 Copilot is in use, eDiscovery can support internal investigations and compliance reviews involving user prompts and AI-generated responses. You can search for Copilot interactions, review findings, and delete content when necessary, for example, in cases involving inappropriate use or data exposure.

