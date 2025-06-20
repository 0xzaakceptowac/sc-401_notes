# Data classification overview
* Data classification helps organizations understand and protect their data by identifying, categorizing, and tagging information based on sensitivity and business needs

# **Sensitive information types (SITs)**: 
* ==Identify structured patterns like credit card numbers, Social Security numbers, and keywords using predefined or custom detection rules.==

## Purview classifies data using 3 methods
*  **Manually by users**: Users apply labels based on their understanding of the data.
- **Pattern-based classification**: SITs recognize predefined patterns, such as credit card numbers or Social Security numbers.
- **AI-powered classification**: Trainable classifiers use AI models to recognize data based on meaning and context rather than predefined patterns.

# Compare built-in and custom sensitive information types

## Built-in sensitive information types
==Built-in SITs detect common types of sensitive data and are ready to use without customization.

- **Standard SITs**: ==Identify commonly recognized sensitive data==, such as credit card numbers, bank account details, and government-issued IDs.
- **Named entity SITs**: ==Detect predefined named entities==, such as personal names, addresses, or medical terms.

## Custom sensitive information types

==Custom SITs allow organizations to create their own classifiers to detect data unique to their environment==. 

- **Keyword-based SITs**: ==Define sensitive data patterns using specific keywords, dictionaries, or regular expressions.==
- **Exact data match (EDM) SITs**: Classify data by ==referencing a structured dataset containing specific values==, improving accuracy for structured records.
- **Document fingerprinting**: Creates SITs based on ==document templates==, allowing organizations to detect and classify content that follows a specific form.


# **Trainable classifiers**: 
* ==Use AI to recognize content based on context and meaning rather than specific keywords.== Organizations can create their own classifiers by training them on real-world examples.
## Types of trainable classifiers
- **Pretrained classifiers**: ==Built-in classifiers that are ready to use for common content types== such as resumes, source code, and offensive language. Microsoft regularly updates these classifiers to improve accuracy.
- **Custom trainable classifiers**: ==Organizations can train their own classifiers using real-world examples to detect data unique to their business.== Custom classifiers require manual training and refinement to improve accuracy over time.
### Pretrained classifiers
Microsoft provides pretrained classifiers for specific types of content, such as:
- **Offensive language**: Detects profane or inappropriate content.
- **Resumes**: Identifies job applicant resumes for HR data management.
- **Source code**: Helps track and protect proprietary or sensitive code.

### Custom trained classifiers
Trainable classifiers integrate with several Microsoft Purview solutions, allowing organizations to classify and govern data effectively:

- **Auto-labeling policies**: Apply sensitivity labels automatically based on classifier results.
- **Retention policies**: Identify and retain important content while disposing of obsolete data.
- **Data loss prevention (DLP)**: Prevent sensitive information from being shared outside the organization.
- **Communication compliance**: Monitor messages for policy violations, including inappropriate content.

## Limitations of trainable classifiers
- They **don't work on encrypted content**.
- They **only classify content in supported locations** (such as SharePoint, OneDrive, and Exchange).
- They require an initial **training and review** process to improve accuracy.