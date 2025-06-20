
==Managing AI security risks requires visibility into AI activity, a clear understanding of where data is being used,== and tools that help organizations take action. 

# **Microsoft Purview Data Security Posture Management (DSPM) for AI**
helps organizations identify AI usage, uncover potential risks, and recommend actions that improve data security and compliance.

### AI insights and analytics

DSPM for AI provides visibility into how AI tools interact with organizational data. It provides:

- Identify which AI tools are in use, including Microsoft 365 Copilot, enterprise AI tools like ChatGPT Enterprise, and other public AI services
- Insights into data exposure risks in AI-generated content
- Reports to help assess compliance and security posture

### Security policies for AI usage

==DSPM for AI includes prebuilt policies that help detect when sensitive data might be at risk in AI interactions.== These policies surface risk indicators and provide recommendations for protective actions. Based on these insights, organizations can:

- Warn users before sharing regulated or confidential data with AI tools
- Apply sensitivity labels or data loss prevention (DLP) policies to AI-generated content
- Escalate high-risk activity to Insider Risk Management or Communication Compliance

### Data assessments

DSPM for AI runs **weekly data assessments** for the top 100 SharePoint sites used by Copilot. These assessments help identify:

- Data that is frequently accessed or overshared
- Files containing sensitive information that might be exposed through AI
- Content missing appropriate labeling or governance controls

Organizations can also create custom assessments to scan specific users or sites for potential data exposure risks.


## Get started with DSPM for AI

To start using DSPM for AI:

- **Access the Microsoft Purview Portal**: Navigate to DSPM for AI from the Microsoft Purview portal.
- **Review AI activity insights**: Identify AI usage patterns and potential data security risks.
- **Activate preconfigured security policies**: Enable built-in policies to monitor and control AI interactions.
- **Run data assessments**: Evaluate AI-related data exposure risks and implement remediation actions.
- **Monitor compliance reports**: Use AI activity logs, security alerts, and policy reports to track AI risks over time.

DSPM for AI helps organizations manage AI-related security and compliance risks by applying the same security principles to AI-generated content as other enterprise data.

# Review AI security reports

After configuring Data Security Posture Management (DSPM) for AI, use Microsoft Purview to analyze AI activity, assess data security risks, and review reports. ==These insights help determine whether AI interactions across Microsoft 365 Copilot, enterprise AI apps, and other AI tools comply with organizational policies. They also help identify areas that require attention.==

### Data insights

==**Data** reports highlight risks related to AI interactions involving sensitive data.== These reports help organizations identify where sensitive information is being processed and whether AI tools are being used responsibly.

The reports available here include:

- **Sensitive interactions per AI app**: I==dentifies AI applications that process sensitive data. This report helps security teams assess which AI tools pose the highest data exposure risks.
- **Top unethical AI interactions**: ==Surfaces instances where Microsoft 365 Copilot has generated or responded to unethical, inappropriate, or noncompliant content.== This information is useful for organizations using Communication Compliance policies to analyze AI-generated messages.
- **Top sensitivity labels referenced in Copilot for Microsoft 365**: ==Displays which sensitivity-labeled content is being referenced by AI tools.== This insight helps organizations assess whether AI interactions involve confidential or highly classified data.

### User risk reports

==**User** risk reports help organizations identify potential insider threats based on how employees interact with AI tools.== These reports assess user behavior, AI usage trends, and the severity of security risks.

The reports available here include:

- **Insider risk severity**: ==Shows user AI interactions grouped by risk levels, helping security teams identify patterns that might indicate excessive or inappropriate AI usage.==
- **Insider risk severity per AI app**: ==Breaks down user risk levels by specific AI applications, showing where risky behavior is occurring. This report helps organizations assess whether additional protections ==or oversight are needed for Copilot or non-Microsoft AI tools.

### Take action on reports

==After reviewing AI security reports, organizations can take specific actions to strengthen visibility, reduce risks, and enforce security policies.== Some reports might initially appear blank if data tracking hasn't been enabled. In these cases, adjustments might be needed to begin collecting insights.

To act on report findings, consider:

- **Extend insights**: ==If a report shows "Data discovery is yet to be defined," AI interactions aren't currently being tracked.== Select **Extend insights** to begin capturing activity in Microsoft 365 Copilot and other AI tools.
- **Enable policies**: Some reports require data loss prevention (DLP) policies, sensitivity labels, or communication compliance policies to be active before data is captured. If a report is empty despite known AI activity, verify that the appropriate policies are enabled and scoped correctly.
- **Review flagged activity**: Reports can surface sensitive data exposure, risky interactions, or insider risk indicators. Use Activity Explorer to investigate flagged events, then apply necessary controls, such as blocking AI interactions with labeled content or restricting access to specific AI tools.

# AI interactions with Microsoft Purview
==Microsoft Purview Audit supports this by capturing logs of user interactions and administrator activity related to Copilot and AI applications.== These audit logs help support internal policies, security controls, and compliance requirements.

## How Microsoft Purview Audit captures Copilot and AI activity

==Audit logging for Copilot and AI applications is included with Microsoft Purview Audit (Standard). If auditing is enabled in your Microsoft 365 tenant, no extra configuration is required to begin capturing these activities.==

Audit logs include both user interactions with Copilot and administrator actions that affect how Copilot is deployed or configured. These logs are available through the Microsoft Purview portal or PowerShell and can be searched using filters based on activity type, app, or user.


## Key fields in Copilot and AI audit records

Audit records contain structured fields to help you interpret each interaction or activity. Some of the most important fields include:

- **Operation**: Describes the type of action, such as CopilotInteraction or AINotesUpdate.
- **RecordType**: Identifies the category of application:
    - `CopilotInteraction`: User interacted with a Microsoft Copilot app
    - `ConnectedAIAppInteraction`: User interacted with a deployed non-Microsoft or custom Copilot app
    - `AIAppInteraction`: User interacted with a non-Microsoft AI app not deployed in the tenant
- **Workload**: Describes the app category (such as `Copilot`, `ConnectedAIApp`, or `AIApp`)
- **AppIdentity**: Identifies the specific app in the format `workloadName.appGroup.appName`
- **AppHost**: Indicates which host application was used during the interaction, such as:
    - `Word`, `Excel`, `PowerPoint`, `Outlook`
    - `BizChat` (for Microsoft 365 Chat)
    - `Teams`, `Loop`, `Whiteboard`, `OneNote`
    - `Defender` (for Security Copilot)