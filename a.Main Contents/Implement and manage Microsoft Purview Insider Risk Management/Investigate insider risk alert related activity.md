# Understand insider risk alerts and investigations

Alerts in Microsoft Purview Insider Risk Management aren't generated randomly. ==They follow a defined sequence of actions that begins with policy settings and ends with a triggered alert. ==

Understanding how alerts are generated is critical to reviewing and interpreting them accurately during investigations. This understanding allows investigators to identify relevant activity, determine why it was evaluated, and assess whether it meets the defined risk criteria.

## Why alert generation matters

Knowing how an alert was generated helps investigators:

- Identify what triggered the alert
- Understand which activities were evaluated
- Determine appropriate next steps
- Align alert evaluation with policy criteria

This context supports more consistent triage decisions and helps reduce time spent on irrelevant or low-risk activity.

## Alert generation process

Alerts are generated through a five-step process:

![[Pasted image 20250619181229.png]]


1. **Settings configured**: ==Organizations configure policy settings to align with their insider risk management strategy.== This includes defining which risk indicators to monitor, identifying sensitive domains, and setting privacy preferences.
    
2. **Policy created**: ==Policies define whose activity to evaluate, what activity to detect, and which events should trigger active monitoring.== For example, a policy might monitor users in finance for data exfiltration after a resignation is submitted.
    
3. **Triggering event occurs**: ==A triggering event activates the policy for a specific user. This could include events such as a resignation date being set or a risky website being accessed.== It might also include detection of exfiltration behavior.
    
4. **User activity evaluated and scored**: ==The system begins monitoring the user's actions.== Activities are assigned risk scores based on the type of activity, configured thresholds, and the user’s history.
    
5. **Alert generated**: ==An alert is generated if the user's risk score exceeds the policy-defined threshold.==

## When you're receiving too few alerts

Receiving fewer alerts than expected might indicate that your policies are too narrow or that thresholds are set too high. To increase alert volume:

- **Enable more risk indicators** in the **Policy indicators** settings. This expands the types of activities that policies detect.
- **Include more users** in policy scope by editing the **Users and groups** section of the policy.
- **Lower trigger thresholds** to start evaluating users earlier based on specific events, such as resignation or access to sensitive content.
- **Lower indicator thresholds** to generate alerts based on less frequent or less severe activity.
- **Adjust the alert volume slider** under **Settings > Intelligent detections**. Moving the slider toward "More alerts" increases overall alert generation, including medium- and low-severity alerts.

## When you're receiving too many alerts

High alert volume can overwhelm analysts and reduce the effectiveness of your investigation process. To reduce alert volume:

- **Enable analytics** in **Settings > Analytics** to identify high-risk areas and adjust your approach accordingly.
- **Use real-time insights** to update thresholds and indicator selections based on recommended values.
- **Refine policy scope and content** by narrowing the list of in-scope users or prioritizing only the most sensitive files and communication channels.
- **Enable inline alert customization** to allow analysts to adjust thresholds during triage.
- **Dismiss multiple low-priority alerts in bulk** to reduce noise in the alert queue.

## Configuration options for alert management

Beyond basic tuning, Microsoft Purview provides several configuration options to help manage alert volume more effectively:

- **Use appropriate policy templates** to target specific risk scenarios.
- **Configure global exclusions** to prevent benign activity from triggering alerts.
- **Define detection groups** to apply different policies to different user populations.
- **Create indicator variants** to refine detection logic.
- **Adjust policy timeframes** to control how far back activity is evaluated.
- **Assign appropriate roles** to ensure only qualified users can make sensitive configuration changes.

Effective alert volume management requires both upfront planning and ongoing tuning. Use built-in analytics and threshold recommendations to maintain a manageable signal-to-noise ratio. When alert volume is tuned effectively, your investigation process becomes more focused, efficient, and aligned with organizational risk priorities.


### Spotlight high-priority alerts

Insider Risk Management includes a **Spotlight** feature that automatically ==highlights high-priority alerts in the alert queue.== This helps analysts focus on the most critical cases first. Spotlight uses rule-based logic to evaluate alerts based on activity type, tags, and risk scoring patterns observed across organizations. Spotlighted alerts appear visually distinct in the alert list and support faster triage decisions.


## Review individual alerts

After identifying an alert of interest in the dashboard, you can select it to open the Alert details page. This view provides a deeper investigation workspace with information about the triggering activity, user context, and risk factors. From here, analysts and investigators can assess whether the alert warrants further action.

- **Alert summary**: Displays the risk severity level, alert score, activity that triggered the alert, and triggering event.
- **User details and history**: Shows general user information and past alerts, including unresolved or repeated risk patterns.
- **Tabs for deeper analysis**: Includes tabs for **All risk factors**, **User activity**, and **Activity explorer** to review specific behavior in detail.
## Triage and take action on alerts

Once you've identified an alert that needs review, you can triage and take action directly from the Alert details page:

- **Dismiss** the alert if it was triggered by expected or non-risky behavior.
- **Confirm and create a case** to escalate the alert for deeper investigation.
- **Assign** the alert to another analyst or investigator.

Each alert is assigned a risk severity score based on multiple factors, including frequency of activity, user history, and the presence of risk indicators. If an alert remains untriaged and more risky behavior occurs, its severity level might increase.


## Use Security Copilot to accelerate triage

If enabled, Security Copilot embedded in Microsoft Purview can summarize an alert to help you triage faster. Without opening the alert, you can select **Summarize with Copilot** to generate an overview that includes:


## Retention and alert limits

Alerts in a "Needs review" state are retained for 120 days. After this period, they're automatically deleted unless linked to an active case. Active and unresolved cases are retained indefinitely. Organizations can have up to 100 active cases at any given time.


# Analyze alert context with the All risk factors tab

The **All risk factors** tab in Microsoft Purview Insider Risk Management provides a summary of potentially risky activity associated with an alert. This view helps investigators understand why an alert might be significant by showing which risk signals are present, even if those signals weren’t the direct cause of the alert.

Use this tab to evaluate the broader context of a user's behavior and decide whether to investigate further, dismiss the alert, or take action.


## Risk factors shown in this tab

The All risk factors tab surfaces several types of behavior that might increase a user's overall risk level:

- **Top exfiltration activities**: Lists the most frequent exfiltration actions, such as archiving or uploading files.
- **Cumulative exfiltration**: Shows whether repeated actions build over time to indicate rising risk.
- **Sequences of activities**: Highlights related activities that form a recognizable risk sequence.
- **Priority content**: Indicates whether the user interacted with files marked as sensitive or business-critical.
- **Unallowed domains**: Flags any file or data transfers to domains that aren't permitted by policy.
- **Unusual behavior or high-impact user status**: Detects abnormal patterns or identifies users whose role or access level contributes to elevated risk.

Not all alerts are directly caused by these factors, but the tab helps you assess what else might be happening that could influence the user’s risk level.


# Investigate activity details with the Activity explorer tab

==The **Activity explorer** tab in Microsoft Purview Insider Risk Management helps analysts investigate the full context of potentially risky behavior.== This tab shows a timeline of user activity that contributes to the alert, with detailed metadata to support investigation, filtering, and review.

Use this tab to confirm what triggered the alert and identify patterns or supporting evidence that indicate whether further action is needed.

## Filter activity for investigation

To help focus your review, use filters at the top of the page to narrow the activity list. You can filter by:

- **Activity scope**: Show all scored activity for the user or only activity associated with this specific alert
- **Risk factor**: Focus on specific indicators like sequences, cumulative exfiltration, unallowed domains, or priority content
- **Review status**: Hide previously reviewed items to focus on new activity

Filtering helps streamline triage and identify which events require the most attention.

## Investigate ongoing risk with the User activity tab

==The **User activity** tab in Microsoft Purview Insider Risk Management shows a visual timeline of potentially risky behavior over time (scatter plot).== This view helps investigators assess whether a user’s activity is ongoing, escalating, or part of a broader pattern.

Use this tab to evaluate risk across multiple alerts and understand how individual actions fit into a larger risk profile.


# Investigate insider risk alerts in Microsoft Defender XDR

**Microsoft Defender Extended Detection and Response (XDR)** ==helps expand investigation capabilities for insider risk by integrating alerts from Microsoft Purview Insider Risk Management with other Microsoft security data. ==This combined view gives security operations center (SOC) analysts the context they need to assess user behavior, correlate risk signals, and take action across Microsoft 365 workloads.

Use this view to correlate insider risk alerts with data from other services like Microsoft Defender for Endpoint, Microsoft Entra ID, and Microsoft Purview Data Loss Prevention.


# Manage and take action on insider risk cases

==Cases in Microsoft Purview Insider Risk Management allow investigators to track user risk over time, review associated alerts, and take action based on the severity and context of the activity. Each case focuses on a single user and can include one or more alerts. ==Cases are created manually when an alert requires deeper review or coordination with other teams.

Use the **Cases** dashboard to view all active and closed cases, assign ownership, and manage follow-up actions such as escalation, communication, and resolution.

## Respond to alerts

Not all alerts require a case. You can take action directly from the **Alerts** queue by confirming or dismissing alerts as part of your triage process:

- **Dismiss** an alert if it's a false positive or doesn't require further review.
- **Confirm** an alert to indicate a policy violation and optionally create a case for deeper investigation.
## Create and manage cases

Cases are created from alerts when an incident needs further review or response. Once created, cases can be updated with new alerts and managed through their lifecycle. You can:

## Investigate a case

Selecting a case opens a detailed investigation view with multiple tabs:

- **Case overview**: User identity, department, risk score, associated alerts
    
- **Alerts**: Status, severity, and alert ID for each included alert
    
- **User activity**: Timeline of scored risk activity from the alert or broader user history
    
- **Activity explorer (preview)**: Detailed timeline and metadata for each associated event
    
    **User activity** shows the overall timeline of user risk behavior, while **Activity explorer** focuses on event-level details within the case scope.
    
- **Forensic evidence**: Screen captures from activity that triggered the alert
    
- **Content explorer**: Copies of files and email messages associated with risk alerts
    
- **Case notes:** Permanent, timestamped notes added by analysts
    
- **Contributors**: Users added to the case for collaboration

## Resolve a case

When investigation is complete, resolve the case as:

- **Benign**: Behavior is low-risk, accidental, or false positive
- **Confirmed policy violation**: Behavior is intentional or a serious violation

Enter a reason for the resolution. Resolution actions are recorded in Case notes, and the case status is updated to Closed.