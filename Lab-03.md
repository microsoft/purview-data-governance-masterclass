![Banner](./assets/banner.png)

# Lab 2: Managing Data Sources

## Task 1: Registering Data Sources

> Microsoft Purview Solution: Data Map

**⏰ Duration:** 30 minutes

**🎯 Outcome:** At the end of this task you will have registered a series of data sources throughout your business.

### Why register Data Sources?

Microsoft Purview lets you to register, manage, and move data sources in your organization's data map. This aids in the organized categorization and systematic access control of your data.

To register a source, you require the role of a Data Source Admin alongside another Microsoft Purview Data Map role. The process involves selecting 'Data sources' in the Microsoft Purview Data Map, choosing a source type, and filling out the form on the 'Register sources' page. Note that most data sources have additional specific information and prerequisites for registration and scanning.

### Exercise: Adding Data Sources

**🫂 Team Activity:** [15 minutes] Review the [supported data sources](https://learn.microsoft.com/en-us/purview/microsoft-purview-connector-overview) and discuss which data sources you would like to onboard first. Start with something that minimises admin overhead or extensive configuration (think: Azure SQL Database or Azure Data Lake Storage).

- What are the common data sources throughout your organization?
- Is the data source in Azure, another cloud provider, or on premises?
- Do you have any data sources that are not on the supported list? We caution against bespoke integrations.

**✍️ Do in Purview:** [15 minutes] Using the Data Map solution, 'Register' a data source by following the wizard. Be sure to select the domain and collection name into which this data source should be registered. You should be confident on your collection hierarchy before continuing.

![Register data source button](./assets/register-datasource-button.png)

Once registered, your data map should be polulated. Next:

- Navigate to the data source overview and observe the registration date, collection path, source hierarchy.
- Should the data source be enabled for automated data access policy enforcement? (access policies will be set up in subsequent tasks)

**✨ Pro Tip:** Because a data source can only be registered once, in cases where the data source is shared across business domains, it may make sense to lift it into a parent collection shared by both business domains. More best practices can be found in the Purview documentation.

After registering your source, you can move it to another collection within the same domain to which you have access. However, it's important to note that when a source moves to a new collection, its scans move with it, but its assets will not appear in the new collection until the next scan is performed.

---

## Task 2: Configure Data Source Scans

> Microsoft Purview Solution: Data Map

**⏰ Duration:** 20 minutes

**🎯 Outcome:** At the end of this tasks, you will have scanned the data source(s) previously registered to let Purview populate the data map with "Data Assets".

### Exercise: Scanning a Data Source

**🫂 Team Activity:** [10 minutes] Remembering that Purview scans metadata and only samples a set number of rows (not the entire database or file), discuss the frequency at which it makes sense to scan each data source.

- How often do data source schemas evolve?
- What data lake layers make sense to be included in a scan? I.e. Do we need to scan raw zones in a data lake when we expect this data to be transformed by business processes prior to becoming "useful" throughout our organization?
- Is it economical to scan a source every day or does it make sense to do so on a weekly/monthly basis given metadata typically doesn't evolve at the same rate as the data itself?
- Do you require scans to occur over a specific runtime? Azure auto-resolved integration runtime vs. self-hosted integration runtime?
- Which credential is required to scan the data source? Microsoft Purview MSI (system) or another?
- What scan level is appropriate for this scan activity?
- Which collection should the assets be scanned into? This may be different from the collection in which the physical data source itself is registered.
- Should scans be full scans or incremental scans?

**✨ Pro Tip:** Don't scan folders of data sources where data is created faster than a data scan can execute (think: files in a raw zone that are created every second). As there is a potential for the data discovery process to endlessly continue before a scan is executed.. leading to cost blowouts.

**✍️ Do in Purview:** [10 minutes] Transfer your discussion into practice by configuring a data source scan for the selected data source.

1. Start by selecting a data source to scan, the select the 'New Scan' button.
   ![Configure a new Data Source Scan](./assets/data-map-configure-scan-button.png)

2. Set up the name, credential, and scan level. Then determine into which collection the data source scan's artifacts (assets) will be written. Follow the steps to provide the Purview MSI its required access to the data source. Test the connection, then proceed.
   ![Configure Scan Details](./assets/configure-scan-details.png)

3. The next steps depend on the type of data source but typically require you to select the scope of your scan (ie. which locations in the Storage Account need to be scanned), the types of file extensions to be scanned, the scan ruleset to use (we will look at this next), and the freqency of the scan.

Save and run the scan. After a scan is configured, open the Data Source and note the recent scans, each scan has options to trigger the scan manually, edit, or delete it.

![Data Source Overview](./assets/data-source-overview.png)

**⏸️ Wait:** A data source scan will have to complete before you can move on to the next section. You can use the 'Monitoring' tab of the Data Map or the Scan Details to track scan the scan status.

## Task 3: Defining Scan Rulesets

> Microsoft Purview Solution: Data Map

**⏰ Duration:** 20 minutes

**🎯 Outcome:** At the end of this task, you will have a better understanding of scan rulesets, how to implement them, and when to use them to optimise data source scanning and reduce cost.

### Understanding Scan Rulesets

> Source: ...

TODO: Add content

---

**⏸️ Reflection:** ....coming soon....

👉 [Continue: Lab 4](./Lab-04.md)
