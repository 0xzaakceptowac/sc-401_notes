# Plan for Insider Risk Management

### Collaborate with stakeholders

Effective insider risk management begins with identifying the right stakeholders. ==Since insider risks often span multiple functions, collaboration across departments is crucial.== Your planning team should include representatives from:

- **IT and security**: Configure systems and ensure technical integrations.
- **Compliance and privacy**: Align policies with regulatory requirements.
- **Human resources**: Provide context for role changes or employee departures.
- **Legal**: Address cases requiring escalation to legal oversight.

### Understand regional compliance requirements

If your organization operates in multiple regions, compliance and privacy regulations might vary.==Address these differences by tailoring your policies and processes to specific regions or roles.== Consider these factors:

- Design policies that restrict access to sensitive information based on location or role.
- Assign investigators fluent in the languages used by employees to streamline reviews.
- Maintain privacy by anonymizing user identities during investigations whenever possible.

### Define roles and permissions

Insider Risk Management ==uses role-based access controls to delegate responsibilities effectively.== For instance, an investigator might review alerts related to data theft while administrators manage policy configurations globally. Plan for the following key roles:

- **Administrators** to configure global settings and policies.
- **Analysts and Investigators** to review alerts and manage cases.
- **Viewers** to review dashboards for trends and risks.

## How Insider Risk Management settings work

Insider Risk Management settings operate globally, affecting all policies regardless of the template you choose. These settings allow you to:

- Customize how user activities are analyzed and scored.
- Prioritize evaluating activities for specific users or groups.
- Ensure compliance with privacy and data handling requirements.
- Reduce false positives by refining detection criteria.

### Privacy
==Choose whether usernames in alerts and cases are anonymized or displayed.== Anonymizing usernames can help organizations maintain employee privacy during investigations.

### Policy indicators
==Enable and adjust indicators that track activities such as downloading sensitive files or forwarding emails.== Configuring thresholds for these indicators ensures that alerts reflect the organization's risk tolerance.

### Detection groups
==Create detection groups to apply specific thresholds or criteria to different sets of users.== For example, you can assign more tailored thresholds for users in high-risk roles, like IT admins or executives.

### Global exclusions (preview)
==Exclude specific users, groups, or activities from being included in policy detections.== For instance, service accounts or routine administrative tasks can be excluded to reduce unnecessary alerts.

### Policy timeframes
==Define the time period for which activities are reviewed when a policy is triggered.== This setting allows organizations to focus on relevant activity periods, such as the 30 days following a policy violation.

### Intelligent detections
Use intelligent detections ==to identify unusual activities, adjust alert volumes, and incorporate alerts from external tools like Microsoft Defender for Endpoint. This setting also allows organizations to prioritize risks related to specific domains or activities.==

### Priority user groups
==Assign higher risk-scoring thresholds to users in critical roles or those with elevated access.== For example, users with access to sensitive data might need more detailed activity evaluations.

### Priority physical assets
==Identify and track activity related to sensitive locations, such as data centers or secure facilities.== Correlating this activity with other user events can provide additional risk insights.

### Notifications
Set up email notifications for admins and other Insider Risk Management role groups. Notifications can be triggered for new alerts, unresolved warnings, or high-severity cases.

### Data sharing
==Enable the export of alerts to external tools like SIEM or SOAR platforms.== Using the Office 365 Management Activity API, this integration allows for centralized alert aggregation and investigation.

### Analytics
==Run analytics scans to evaluate risk trends and identify potential areas of concern before creating policies.== This feature provides insights without requiring policy deployment.

### Inline alert customization
==Adjust thresholds for policies directly from the **Alert dashboard**.== This feature allows real-time tuning of detection criteria based on the specifics of an alert.

### Power Automate flows (preview)
==Automate tasks such as sharing case updates or posting case notes using Power Automate flows.== This can streamline workflows and improve efficiency during investigations.

### Microsoft Teams
==Enable private Teams channels to facilitate collaboration among investigators.== Teams can be used to securely share evidence, coordinate actions, and track responses.

## What are connectors?

==Connectors allow Insider Risk Management to import data from internal and external systems. This data provides insights that support the creation of effective policies and the identification of relevant patterns or activities.== The imported data is securely managed and used to align with organizational goals and compliance requirements.

- **HR connectors**: Use employee lifecycle data, ==such as resignation or termination dates, to inform policies about departing employees.==
- **Healthcare connectors**: Import electronic health record (EHR) ==audit data to help identify unauthorized access or data handling.==
- **Cloud app connectors**: ==Bring in detections from non-Microsoft applications, such as Dropbox or Google Drive, to expand visibility into data usage.==

## Key integrations

Several tools and data sources enhance the capabilities of Insider Risk Management by providing additional signals or enabling centralized management. These include:

- **HR and healthcare connectors**: Import employee and healthcare data to support policy creation and refine risk detection.
- **Cloud app integrations**: U==se detections from cloud apps like Amazon S3 or Salesforce to identify activities that could pose risks to sensitive data.==
- **Data loss prevention (DLP)**: ==Link high-severity DLP alerts to insider risk policies to help prevent unintentional or intentional data leaks.==
- **Microsoft Defender for Endpoint**: Integrate endpoint security alerts to provide additional context for risk assessments.
- **SIEM and SOAR platforms**: Export alerts to solutions like Microsoft Sentinel for centralized alert management and automated responses.

These integrations provide flexible ways to enhance risk detection, align with organizational needs, and maintain compliance.


