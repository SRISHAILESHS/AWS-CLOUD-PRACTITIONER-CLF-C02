# Amazon S3 Storage Classes

Amazon S3 storage classes help us choose where to store files based on how often we access them and how quickly we need them.

## 1. S3 Standard

**Purpose:** Store files that we access frequently.

**Example:** A clothing shop stores shirt photos that customers view every day on its website.

**Remember:** Frequently used files.

## 2. S3 Intelligent-Tiering

**Purpose:** Help reduce storage costs when file access patterns change or are unpredictable. AWS automatically moves eligible data between access tiers.

**Example:** A company stores project files that employees sometimes use frequently and sometimes rarely.

**Remember:** Access frequency changes.

## 3. S3 Standard-IA (Infrequent Access)

**Purpose:** Store files that we rarely access but need to retrieve quickly when required.

**Example:** A clothing shop keeps last year's sales reports, which are opened only occasionally.

**Remember:** Rarely used, but quick access is needed.

## 4. S3 One Zone-IA

**Purpose:** Store infrequently accessed data in one Availability Zone. It costs less, but data is not redundantly stored across multiple Availability Zones.

**Example:** A company stores replaceable backup files that can be recreated if lost.

**Remember:** Rarely used, replaceable files in one Availability Zone.

## 5. S3 Glacier Instant Retrieval

**Purpose:** Store archive files that are rarely accessed but need immediate retrieval.

**Example:** A hospital keeps old medical images that may occasionally be needed immediately.

**Remember:** Archive files with immediate access.

## 6. S3 Glacier Flexible Retrieval

**Purpose:** Store archive files when retrieval can take minutes to hours, depending on the retrieval option.

**Example:** A company keeps old financial reports for audits and can wait for them to be retrieved.

**Remember:** Archive files; waiting is acceptable.

## 7. S3 Glacier Deep Archive

**Purpose:** Store data for long-term retention at a very low storage cost. Retrieval usually takes hours.

**Example:** A company keeps legal records that must be retained for many years and are rarely accessed.

**Remember:** Long-term storage; very rare access.

---

## Quick Revision Table

| Storage class | Main purpose |
|---|---|
| S3 Standard | Frequently accessed files |
| S3 Intelligent-Tiering | Access patterns change or are unpredictable |
| S3 Standard-IA | Rarely accessed files that need quick retrieval |
| S3 One Zone-IA | Rarely accessed, replaceable files stored in one Availability Zone |
| S3 Glacier Instant Retrieval | Archive files needing immediate retrieval |
| S3 Glacier Flexible Retrieval | Archive files where retrieval can take minutes to hours |
| S3 Glacier Deep Archive | Long-term archival with retrieval usually taking hours |

## Easy Way to Remember

- **Standard:** Use frequently.
- **Intelligent-Tiering:** Access pattern changes.
- **Standard-IA:** Use rarely, retrieve quickly.
- **One Zone-IA:** Rarely used, replaceable data in one Availability Zone.
- **Glacier Instant Retrieval:** Archive, access immediately.
- **Glacier Flexible Retrieval:** Archive, wait minutes to hours.
- **Glacier Deep Archive:** Keep for years, rarely access.

## Interview Answer

“Amazon S3 provides different storage classes based on data access patterns. S3 Standard is for frequently accessed data. Intelligent-Tiering helps optimize costs when access patterns change. Standard-IA is for infrequently accessed data that needs quick retrieval. One Zone-IA stores infrequently accessed data in one Availability Zone. Glacier classes are used for archiving: Instant Retrieval provides immediate access, Flexible Retrieval allows a delay, and Deep Archive is designed for long-term retention.”

**Note:** Some storage classes have minimum storage-duration charges and retrieval charges. Check the current AWS pricing for your Region before choosing a class.
