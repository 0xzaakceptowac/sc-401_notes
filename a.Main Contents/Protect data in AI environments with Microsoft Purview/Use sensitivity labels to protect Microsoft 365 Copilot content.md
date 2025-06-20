
## Understand sensitivity labels

==Sensitivity labels are part of Microsoft Purview Information Protection. They allow organizations to classify and protect their content based on its sensitivity level.== Each label can apply a set of protection settings, including:

- **Encryption**: Ensures only authorized users can access the content, even if it's shared externally.
- **Content markings**: Adds headers, footers, or watermarks to indicate the sensitivity of the content.
- **Access restrictions**: Limits who can view, edit, print, or forward the content.

Sensitivity labels help organizations apply consistent protections, both within Microsoft 365 and across supported non-Microsoft tools and services.

## How Microsoft 365 Copilot works with sensitivity labels

Copilot respects the sensitivity labels that are applied to content it accesses. It follows the protection settings defined in those labels and only processes content the user has permission to access. This ensures that data protection policies remain in effect even when AI features are used.

Here's how sensitivity labels interact with Copilot:

- **Label recognition**: Copilot identifies and respects sensitivity labels when accessing data.
- **Label inheritance**: When Copilot creates new content based on labeled source files, it inherits the labels from those files.
- **Permission checks**: Copilot checks user permissions before accessing labeled content. If the user isn’t authorized, the content isn’t used.

### Understand how the one-click policies behave

The two DSPM for AI one-click policies differ in how they're applied:

- **DSPM for AI: Detect sensitive info added to AI sites** is created as an active policy. It begins auditing pastes into generative AI websites immediately.
- **DSPM for AI – Block sensitive info from AI sites** is created in simulation mode. It uses Adaptive Protection to target elevated risk users and applies a warning with override, but doesn't enforce blocks until you move the policy out of simulation mode.