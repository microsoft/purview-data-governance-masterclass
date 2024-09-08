![Banner](./assets/banner.png)

# Lab 2: Designing the Data Map

## Task 1: Consider the Design

> Microsoft Purview Solution: Data Map

**⏰ Duration:** 30 minutes

**🎯 Outcome:** At the end of this task, you will have answered important questions that will form part of the structure of the workshop and help the instructor know where to focus the session.

**🫂 Team Activity:** [30 minutes] Together as a group, revisit the questions posed at the start of Lab 1, adding a little detail around each answer to guide you in the following exercises.

- Are you interested in Security, Privacy, and Compliance capabilities too, or just Purview Data Governance over structured data?
- Have you got the respective Microsoft 365 Enterprise licence to test out the Security/Privacy/Compliance features?
- Do you have E3/E5 Risk and Compliance policies in place already (Information Protection, Insider Risk Management, Information Barriers etc)?
- Are there any on-premises services that need to be considered/evaluated as part of the Purview Data Governance / cataloging initiative?
- Given data governance is interdisciplinary, have you considered use cases and identified stakeholders throughout the business?
- Have you figured out how data governance costs will be apportioned?
- Have you planned your path to production?

If you were unable to answer many of these questions, lets aim to get clarity at the end of the session/workshop - once capabilities become clearer to you.

---

## Task 2: Create your Platform Domains

> Microsoft Purview Solution: Data Map

**⏰ Duration:** 10 minutes

**🎯 Outcome:** At the end of this task, you will have implemented your platform domains such that you can confidently divide your Purview Data Map based on environment / isolation requirements.

### Understanding Platform Domains

> Source: [Domains](https://learn.microsoft.com/en-us/purview/concept-domains)

Microsoft Purview has introduced 'domains' (not to be confused with the Business Domains concept) as a structure within the Microsoft Purview Data Map. Domains, which can only be used by Microsoft Purview accounts operating on a tenant-level account, are designed to distribute organizational responsibility, create hard logical separations, ensure consistent management across assets and glossaries, and replace multiple accounts within a tenant to multiple domains within a single Microsoft Purview resource.

**Key Facts:**

- Every Microsoft Purview Data Map starts with a default domain. This domain is the primary account's root collection when an account is upgraded to the new experience.
- Up to 4 additional custom domains can be created for better organization and governance.
- A new role, the domain admin, can be assigned. They will have the ability to assign permissions within a domain and manage its resources.
- In the future, you will be able to merge tenants with multiple Microsoft Purview accounts into the new experience using domains.

![A tenant contains multiple domains, each domain enclosing collections and glossaries](./assets/tenant-with-domains.png)

### Understanding Collections inside Domains

> Source: [Manage Domains and Collections](https://learn.microsoft.com/en-us/purview/how-to-create-and-manage-domains-collections)

In the context of Microsoft Purview, collections are a way to organize resources like data sources, scans, and assets within a domain. Each domain, both default and custom, starts with one root collection and can contain multiple sub collections.

![Creating a new Collection](./assets/creating-new-collection.png)

**Key Characteristics:**

- Hierarchical Structure: Collections form a tree structure, allowing you to organize your resources into a hierarchy based on access control boundaries.
- Role Assignments: Collections support role assignments, allowing you to manage access and permissions at a granular level. These roles could include Domain admins, Collection admins, Data curators, and more.
- Resource Management: Resources (data sources, scans, assets) associated with a collection are automatically included when the collection is identified. Depending on the assigned permissions, these resources can be viewed, edited, or deleted.
- Movement of Resources: Collections allow for movement of registered sources between them and also let you add assets.
- Inheritance: In Purview, permissions are inherited automatically from the parent collection to its sub collections. This inheritance can be restricted if needed.

Remember that, to manage collections, one needs to be at least a Domain Admin or Collection Admin within the Microsoft Purview governance portal.

### Exercise: Create Domains and Collections

**🫂 Team Activity:** [5 minutes] As a group, identify whether there is a need to create multiple platform domains in Purview? These allow you to separate data sources into isolated domains such as dev/prod.

- Is there a requirement to create a dev/prod type of setup (bearing in mind that a data source can only be registered in one place at a time)?
- Can you use one platform domain (prod) and rely on the ability to change the status of non-curated assets instead of doing so in multiple domains?
- Does your organization have parent/child company setups where you need to consider how to represent the child company under the same Purview Data Map?

**✍️ Do in Purview:** [5 minutes] Navigate to the Data Map and create a new platform/technical domain if required. If not required, continue on.. you will be working inside the default domain.

- Assign the respective platform domain admin(s).

---

## Task 3: Create and Extend Sensitivity Labels

> Microsoft Purview Solution: Information Protection

**⏰ Duration:** 30 minutes

**🎯 Outcome:** At the end of this task, you will have created tenant-wide sensitivity labels in the Compliance solution. These can be added manually (or automatically if an E5 Risk & Compliance license is available) to data assets at the time of creation (or labelled later). You will also learn to expand these labels to the Purview Data Map solution for labelling of structured data assets.

### Understanding Sensitivity Labels

Sensitivity Labels are a feature that help you classify and protect organizational data (usually at the time of creation, but can be applied or modified at any time). They help ensure that user productivity and collaboration capabilities remain uncompromised by 'stamping' the data (file, folder etc) with a consistent text and protective properties that follow the data no matter where it is stored.

![Sensitivity Label Recommendation](./assets/sensitivity-label-recommendation.png)

Sensitivity labels can be used to control access to content using encryption, add watermarks or headers to content, apply access policies automatically, protect content in Teams, Groups, and SharePoint sites, protect chat and meeting data, extend to Power BI and Microsoft Purview Data Map, and even integrate with third-party applications. [Supported data sources](https://learn.microsoft.com/en-us/purview/microsoft-purview-connector-overview) (see 'labeling' column).

The label's scope determines the label's settings and its availability to apps and services. The label's order in the list also sets its priority (with labels appearing lower on the list having a higher order number and thus higher priority).

![Applying Sensitivity Labels](./assets/applying-sensitivity-labels.png)

Sub labels, or 'child' labels beneath a 'parent' label, present labels to users in logical groups. They do not inherit the protection settings of their parent label but do inherit their color.

Sensitivity labels are also recognized and used by Microsoft services like Microsoft Copilot for Microsoft 365 and Azure Information Protection. These services check the usage rights for the user and allow an extra layer of protection for labeled items.

### Exercise: Implement Sensitivity Labels

**🫂 Team Activity:** [5 minutes] Discuss whether your organization has an E3/E5 licence today and whether sensitivity labels are set up in your business already.

- Are you using sensitivity labels today and do these get automatically or manually applied to unstructured data assets like Microsoft 365 apps to protect new business data at the time of creation?
- Are sensitivity labels enforced for all users in the business (recommended) or targeted selectively?

**✍️ Do in Purview:** [5 minutes] Open the Information Protection solution:

- Create, review, and publish organization-wide sensitivity labels as required.
  ![Sensitivity Labels Overview in Microsoft Purview](./assets/sensitivity-labels-overview.png)
- Define Auto-labeling policies as required by your organization.
- Define Trainable Classifiers and Sensitive Information Types as applicable.
- Enable the option to 'Extend Sensitivity Labels to the Purview Data Map'. New scans and supported data sources can now be labelled (automatically) with the sensitivity label.

---

## Task 4: Adding Lineage Connections

> Microsoft Purview Solution: Data Map

**⏰ Duration:** 10 minutes

**🎯 Outcome:** At the end of this task, you will have linked an Azure Data Factory and Azure Data Share account to the Data Catalog. This ensures that transformations inside of ETL processes (e.g. at the column level) are accurately captured in the overall lineage once we start registering data sources.

### Understanding Data Lineage

Data Lineage represents the lifecycle of an organization's data, tracing its origin and movement across the data estate. This data could include raw data from various platforms, transformed and prepared data, and data utilized by visualization platforms.

Knowing the lineage of data assets is important for troubleshooting, root cause tracing in data pipelines, debugging, data quality analysis, compliance, and impact analysis. It helps in representing data that moves from source to destination, including how the data was transformed.

<!-- TODO: Update with latest lineage UI -->

![Asset Lineage](./assets/asset-lineage.png)

**Types of Lineage:**

- **Entity (or asset) Lineage:** Lineage is typically represented as a graph showing source and target entities, linked by a process invoked by a compute system, assisting in making the lineage human-readable.
- **Column-level (or attribute) lineage:** It identifies columns of a source entity that are used to create or derive columns in the target entity, assisting in tracking column-level changes from the source to the target.

### Exercise: Adding Lineage Connections (optional)

**✍️ Do in Purview:** [5 minutes] Navigate to the Data Map solution's Source Management, and enter the 'Lineage connections' tab. Add one or more Azure Data Factory resources.

![Adding Data Factory Lineage Connections](./assets/data-factory-lineage-connection.png)

After registration, the Status should appear as: `Connected`

![Data Factory Lineage Overview](./assets/data-factory-lineage-overview.png)

**✍️ Do in Purview:** [5 minutes] Navigate to the Data Map solution's Source Management, and enter the 'Lineage connections' tab. Add one or more Azure Data Share resources.

**✨ Pro Tip:** Each Data Factory or Azure Data Share can only be connected to one Purview account.

---

**⏸️ Reflection:** At this point you have understood the need for multiple platform domains and the collection hierarchy within each. You also learned about the types of roles a Purview administrator may assign at the top-most levels of the Data Map. You experimented with Sensitivity Labels and extended them to the Purview Data Map for automatic labeling in the next lab.

Lastly, you learned about the benefit of data lineage and how common ETL tools like Azure Data Factory and data sharing services like Azure Data Share can be connected to Microsoft Purview to inform transformation and external content sharing lineage.

👉 [Continue: Lab 3](./Lab-03%20-%20Managing%20Data%20Sources.md)
