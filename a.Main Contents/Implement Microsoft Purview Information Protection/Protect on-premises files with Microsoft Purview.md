The **Microsoft Purview Information Protection scanner** is a ==Windows Server-based service that can scan, classify, and optionally label or protect files stored in:==

- UNC paths (SMB or NFS, preview)
- SharePoint Server document libraries (2013 through 2019)

==The scanner is part of the broader Microsoft Purview Information Protection solution ==and uses your existing sensitivity labels to apply classification and encryption policies across on-premises data.

You can use the information protection scanner to:

- **Apply sensitivity labels and encryption** to files in supported locations, based on your configured label policies.
- Use **data loss prevention (DLP) rules** to detect potential data exposure and automatically restrict access to sensitive files.
- **Scan in discovery mode** to identify sensitive data without labeling or protecting files, allowing you to assess results before taking action.
- **Scale scanning across large environments** by deploying multiple scanner nodes as part of a cluster.

## How does the scanner work?

Each time the scanner runs, it performs a series of steps to identify, label, and protect sensitive content:

1. **Determine which files to scan**: ==File inclusion and exclusion rules== are set through configuration. System and unsupported file types are automatically skipped.
2. **Inspect and label files**: The scanner uses ==Windows indexing filters (IFilters) to read file contents and identify sensitive data based on sensitive information types or regex patterns.==
3. **Apply labels and protection**: If a file matches the conditions defined in a sensitivity label, the label is applied. If encryption is part of the label policy and supported by the file type, encryption is applied.
4. **Fallback behavior**: ==For files that can't be inspected, a default label might be applied based on your label policy configuration==


## Microsoft Purview roles that can configure the scanner:

- Compliance Administrator
- Compliance Data Administrator
- Security Administrator
- Organization Management


## View scan reports

When the scan finishes, reports are saved locally on the scanner server:

shell

```
%localappdata%\Microsoft\MSIP\Scanner\Reports
```

Reports include:

- `.txt` summary files with scan time, number of scanned files, and detection counts
- `.csv` files with detailed results for each file

## Available DLP actions

When a file matches a DLP policy, the following actions can be applied:

- **Block all access**: Remove NTFS or SharePoint permissions for all users except the file owner, repository owner, last modifier (SharePoint only), and administrators.
- **Block broad access**: Remove built-in groups such as _Everyone_, _Authenticated Users_, and _Domain Users_ from the file's access list.
- **Force inheritance from parent folder**: Apply permissions from the parent folder. You can optionally override and enforce this even if the parent permissions are less restrictive.
- **Quarantine the file**: Replace the original file with a stub `.txt` file and move the file to a designated quarantine folder.

### Where to view DLP activity

DLP detection and enforcement for on-premises files is visible in:

- **Activity explorer**: View matches by file name, type, rule name, and applied actions.
- **Audit log**: Track when DLP actions are taken on files.
- **Local scan reports**: Stored in `%localappdata%\Microsoft\MSIP\Scanner\Reports`, including `.csv` logs with DLP-specific columns like `DLP Rule Name`, `DLP Status`, and applied permissions.

