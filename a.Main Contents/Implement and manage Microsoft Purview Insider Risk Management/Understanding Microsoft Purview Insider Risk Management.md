# What is an insider risk?

==While external threats like hackers are a focus, some of the most significant risks come from within. Insider risks involve trusted individuals like employees, contractors, or business partners, who have legitimate access to sensitive information.== Their actions, whether intentional or accidental, can lead to serious consequences for the organization. Understanding insider risks is essential to safeguarding data, systems, and reputation.

## Types of insider risks

- **Malicious insider risks**: ==These occur when someone deliberately acts against the organization.== Their actions might include theft, sabotage, or leaking confidential information.
- _Example_: A frustrated employee downloads trade secrets and shares them with a competitor.

- **Accidental insider risks**: ==These involve unintentional actions, like mistakes or negligence, that result in harm to the organization.==
- _Example_: An employee opens phishing link, exposing sensitive company data.

## What is Microsoft Purview Insider Risk Management?

==Microsoft Purview Insider Risk Management is a solution that helps organizations minimize internal risks by detecting, investigating, and responding to potentially harmful activities.== It analyzes signals from across the Microsoft ecosystem and integrates with other tools to provide actionable insights.

- **Identify risks**: Surface activities that could lead to data breaches, compliance violations, or other harmful outcomes.
- **Investigate context**: Analyze the circumstances behind risky activities to understand their significance and determine next steps.
- **Take action**: Use tools to address risks effectively, such as sending notifications, adjusting policies, or escalating cases for deeper review.

## How Insider Risk Management works

Microsoft Purview Insider Risk Management follows a clear workflow to help organizations identify and address internal risks effectively:

- **Policies**: Define the types of activities to evaluate, such as data exfiltration or security violations, using predefined templates.
- **Alerts**: Flag activities that meet policy conditions, prioritizing those that require attention.
- **Triage**: Evaluate alerts to determine if they indicate actual risks and decide on the next steps.
- **Investigate**: Examine cases with tools that provide insights into risk patterns and related activities.
- **Take action**: Resolve issues through notifications, policy adjustments, or escalating to legal or compliance teams.

## Taking action with investigations and notifications

Once risks are identified, actions can be taken to mitigate them:

- **Investigations**: Cases allow for detailed analysis of risky activities, including reviewing associated data files, timelines, and user behavior patterns.
- **Notifications**: For less severe incidents, user notifications can serve as reminders or direct users to training resources to avoid future violations.
- **Escalations**: For serious risks, cases can be escalated to other tools like eDiscovery (Premium) for comprehensive legal and compliance reviews.

# Microsoft Purview Insider Risk Management features
## Policies

Policies are the backbone of Microsoft Purview Insider Risk Management. They define the types of activities to evaluate, ensuring a targeted and efficient approach to identifying risks.


## Signals

Insider Risk Management uses signals, which are data points from user activities from Microsoft 365, Microsoft Defender, and other integrated tools to identify activities that might indicate risks. These signals provide the data needed to analyze user actions and determine whether they align with policy criteria.


## Analytics

Analytics help organizations identify areas of higher user risk before implementing policies. For example, you might discover that departing employees frequently download sensitive files, allowing you to prioritize policies for this group. By identifying potential risks early, analytics can guide the creation or refinement of policies, ensuring that efforts focus on the most impactful areas.

## Dashboards

Microsoft Purview Insider Risk Management offers dashboards that provide a high-level view of risk activities, policies, alerts, and cases.


## Investigative tools

==When an alert requires further review, Microsoft Purview provides tools to help administrators and investigators understand risky activities in detail.== These tools are designed to provide the necessary context for identifying whether an activity truly poses a risk and to support decision-making during investigations.

**Key features for investigations**:

- **User activity reports (preview)**: Allow investigators to view detailed records of a user's actions over a specific time period. For example, ==these reports can highlight unusual activity such as multiple file downloads in a short timeframe, helping investigators assess whether the behavior aligns with a policy violation.==
    
- **Content explorer**: ==Displays files, emails, and other data associated with flagged activities. Investigators can review these items to understand the context of an alert,== such as whether sensitive information was shared externally.
    
- **Case notes**: ==Help investigators document their findings during an investigation.== For example, a reviewer might note that a flagged email contained confidential data or that a user accessed sensitive files without proper authorization. These notes ensure consistent tracking and can be shared with team members for collaboration.
    

Together, these tools ensure investigators have a complete picture of risky activities, from initial alerts to the final resolution of cases.


## Integrated risk management across Microsoft Purview

Microsoft Purview Insider Risk Management integrates with other tools to create a holistic approach to managing risks.

- **eDiscovery (Premium) enables ==legal teams to manage investigations involving insider risks.==
- **Microsoft Defender for Endpoint  ==contributes alerts about device-related risks.==
- **Communication Compliance  helps address risks ==related to inappropriate messaging behavior.==

These integrations allow Insider Risk Management to combine signals from multiple sources, providing a more comprehensive view of risks across your organization.

Microsoft Purview Insider Risk Management provides organizations with the tools they need to detect, investigate, and address insider risks. By using these features, organizations can protect sensitive data, ensure compliance, and build a culture of trust and accountability.


## How the organization responds

1. **Policy detection and alert review**: ==The organization previously created a **Data theft by departing users** policy to detect risky activities==, like large downloads or file transfers by departing employees. ==This policy is designed to flag potential data exfiltration attempts.==
    
    The project manager's download activity triggers an alert in Microsoft Purview Insider Risk Management, appearing in the **Alerts dashboard** as high priority. The reviewer notes the unusual volume and timing of the downloads, raising concerns about potential data theft.
    
2. **Investigation**: Using ==**Content explorer**, the investigator examines the downloaded files. These include product roadmaps and client presentations marked with a "Confidential" sensitivity label==
    
    The investigator also uses **User activity reports** to confirm that the downloads occurred outside the project manager's normal working hours, adding to the concern.
    
3. **Action taken**: The organization takes the following steps:
    
    - **Notification**: The project manager receives a notice reminding them of company policies on handling sensitive information.
    - **Escalation**: The case is escalated to the legal team using eDiscovery (Premium) to ensure compliance with regulatory requirements and organizational policies.
    - **Policy refinement**: Based on the incident, the organization updates its "Departing Users" policy to flag downloads of labeled files during non-business hours.