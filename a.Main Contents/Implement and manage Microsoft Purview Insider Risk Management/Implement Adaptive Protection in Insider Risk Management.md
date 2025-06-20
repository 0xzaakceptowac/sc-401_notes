==Adaptive Protection in Microsoft Purview uses machine learning to identify and mitigate critical risks by dynamically applying the most effective data loss prevention (DLP) controls.== It extends risk-based policy enforcement beyond insider risk management to include DLP policies, Microsoft Purview Data Lifecycle Management, and Microsoft Entra Conditional Access, helping security teams automate responses to potential threats.

Adaptive Protection helps mitigate risks by using:

- **Context-aware detection**: ==Identifies high-risk activities with machine learning analysis of user behavior, content interactions, and risk indicators.==
- **Dynamic policy enforcement**: ==Applies security controls in real time based on a user's risk level.==
- **Automated mitigation**: ==Adjusts security restrictions automatically, applying stricter policies to high-risk users while allowing low-risk users to work without disruption.==
## Risk levels

Risk levels in Adaptive Protection define how risky a user's activity is. ==Risk levels can be based on criteria such as how many exfiltration activities they performed or whether their activity generated a high severity insider risk alert.== These risk levels have built-in risk level definitions, but these definitions can be customized as needed:

- **Elevated risk level**: ==The highest risk level includes built-in definitions for users with high severity alerts, users with at least three sequence insights ==that each have a high severity alert for specific risk activities, or one or more confirmed high severity alerts.
- **Moderate risk level**: ==The medium risk level includes built-in definitions for users with medium severity alerts or users== with at least two data exfiltration activities with high severity scores.
- **Minor risk level**: ==The lowest risk level includes built-in definitions for users with low severity alerts or users== with at least one data exfiltration activity with a high severity score.


### Quick setup

The quick setup option is the fastest way to get started with Adaptive Protection. ==With this option, you don't need any preexisting insider risk management or DLP policies. You also don't need to preconfigure any settings or features.==

### Custom setup

The custom setup option allows you to customize the insider risk management policy, the risk levels, and the DLP policies configured for Adaptive Protection. ==This option also allows you to configure these items before enabling the Adaptive Protection connections between insider risk management and DLP. Most organizations with existing insider risk management policies and/or DLP policies should use this option.==

# Manage Adaptive Protection

==Adaptive Protection in Microsoft Purview dynamically applies security controls based on user risk levels. By integrating with Data Loss Prevention (DLP), Data Lifecycle Management (DLM), and Conditional Access, it ensures that security policies automatically adjust as user behavior changes.== This helps organizations mitigate risks without imposing unnecessary restrictions on low-risk users.

Once Adaptive Protection is enabled and Insider Risk Management policies are configured, administrators can view risk levels and review policy assignments.

They can also manage security controls dynamically. The **Dashboard** in Adaptive Protection provides a centralized view of assigned risk levels and the policies in effect.


