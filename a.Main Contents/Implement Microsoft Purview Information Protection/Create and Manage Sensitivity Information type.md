* ==Sensitive information types (SITs) in Microsoft Purview help organizations identify and protect sensitive data such as personal identification numbers, financial information, and intellectual property==

## Advantages of built-in SITs
==Use built-in SITs when your organization deals with standard types of sensitive information, such as payment details, government-issued IDs, or health records.== They're ideal for general compliance and data loss prevention (DLP) needs.

* ***Quick deployment**: Built-in SITs are ready to use out-of-the-box and require no extra setup. They allow organizations to rapidly deploy data protection solutions for common data types.

- **Managed by Microsoft**: Microsoft continuously updates and maintains built-in SITs to ensure they meet the latest compliance and regulatory standards.

- **Broad coverage**: These SITs cover a wide range of industries and sensitive data types, from financial information to healthcare records.


## Features of custom SITs

- **Exact data match (EDM)**: ==Matches exact data values by comparing content to predefined databases==, making it ideal for organizations that need to protect large datasets with precise information, such as patient records or employee data.

- **Document fingerprinting**: ==Converts standardized forms into custom SITs, enabling organizations to detect when sensitive documents, such as government forms or contracts, are shared.==

- **Keyword dictionaries**: ==Allows organizations to manage and detect large lists of sensitive keywords and phrases specific to their operations or industry, such as internal product codes or terminology.==

## Fundamental parts of a sensitive information type

Every sensitive information type entity includes these fields. Each component plays a role in how effectively the sensitive information type identifies and protects data.

- **Name**: The identifier of the SIT
    
- **Description**: Explains what data the SIT is looking for
    
- **Pattern**: A pattern defines the sensitive information detection criteria, consisting of:
    
    - **Primary element**: ==The main pattern that the sensitive information type is looking for. It can be a **regular expression** with or without a checksum validation, a **keyword list**, a **keyword dictionary**, or a **function**.==
        
    - **Supporting element**: ==Extra evidence that increases the confidence of the match. For example, keyword "SSN" in proximity to a Social Security Number (SSN). It can be a regular expression with or without a checksum validation, keyword list, keyword dictionary.==
        
    - **Confidence level**: ==Indicates how much supporting evidence is needed to classify data as sensitive.== Higher confidence levels require more corroborating data, reducing the chance of false positives.
        
    - **Proximity**: ==The maximum allowed distance between the primary element and the supporting evidence to be considered a match.==
## EDM SIT

==An EDM SIT is different from standard SITs because it matches exact data values== instead of relying only on patterns or keywords. It also includes a few specific concepts:

### Schema

The schema is an XML file that serves as the blueprint for your EDM SIT. It defines:

- The name of the schema, later referred to as the ==_DataStore_.==
- Field names that correspond to the ==columns in your sensitive information source table.==
- Which fields are searchable, allowing precise control over what the SIT will check.
- A _configurable match_ to ==refine your search, such as case sensitivity or ignoring punctuation.==

## Implement document fingerprinting

* As an information worker, you handle sensitive documents every day, whether they're legal forms, employee records, or compliance documents. Protecting this data from unauthorized access or accidental sharing is critical. ==Document fingerprinting in Microsoft Purview simplifies this by automatically detecting and safeguarding standard forms used in your 
* ==converts common forms, such as a standard contract or patent application, into a unique sensitive information type==

## Named Entities
==Named entities are specific types of [sensitive information types (SIT) that you can use to detect person names, physical addresses, and medical terms and conditions.==

### Unbundled

These ==named entity SITs have a narrower focus, such as a single region, or a single class of terms.== Use them when you need a DLP policy with a narrower detection scope.

### Bundled

Bundled named entity ==SITs detect all possible matches in a class, such as _All physical addresses_. Use them as broad criteria in your DLP policies for detecting sensitive items. To use bundled SITs,== you must activate Advanced classification scanning and protection  for the relevant data loss prevention settings before they're discoverable.








