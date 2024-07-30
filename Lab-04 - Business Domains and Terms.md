![Banner](./assets/banner.png)

# Lab 4: Business Domains

## Task 1: Creating Business Domains

**⏰ Duration:** 20 minutes

**🎯 Outcome:** At the end of this task, you will have conceptualised and created business domains in Purview.

### Understanding Business Domains

In Microsoft Purview, a 'business domain' is a new concept introduced to provide context to data assets and enable more effective scaling of data governance practices (in a federated, not centralized approach). Principally focused on improving data ownership management, a business domain can be seen as a boundary enabling consistent governance, ownership, and discovery of data products.

![Business Domain Overview](./assets/business-domain-overview.png)

**Key Facts**

- A business domain could represent functional business units, line of business, data domains, regulatory, or project domains for example.
- Business Domains could also be hierarchical, they can be nested inside parent business domains. For example: A hypothetical `Customer` domain may contain the `Customer Delivery` and the `Customer Experience` child domains.
- A business domain has a name, description, domain owner(s), data products, glossary terms, Objectives and Key Results (OKRs) and critical data elements among others.
- Through defining overarching categories for assets, business domains enable users to narrow down their search for relevant data. They further allow business domain owners to align data governance to their specific business areas.
- Business domains aid in managing an expanding catalog of data assets, ensuring effective governance as the data estate grows. Glossary terms defined within a business domain can be applied to any data product within that business domain, helping data owners and stewards govern a growing number of assets effectively.
<!-- - Glossary terms now also carry access policies, which get automatically applied when the term is attached to a data product. This means business domain owners and stewards only need to devise governance practices once, which can then be applied consistently across the data estate. -->

In essence, business domains utilize existing business context to ensure data is not only more discoverable but also well governed as it expands.

![Sample Business Domains](./assets/sample-business-domains.png)

### Excersise: Creating Business Domains

**🫂 Team Activity:** [20 minutes] Organize yourselves into smaller teams. As a team, discuss and organize business 'domains' within your organization. These may refer to departments / organizational units or other breakdowns of the company.

Use a whiteboard or paper to draw and document your business units.

- Name of the business domain as it is used throughout the company
- Description of the business domain and its responsibilities
- Name of the domain Owner(s)
- **Optional:** Discuss the data domain stewards, data product owners, and data quality stewards associated with each business domain.

At the end of this team exercise, you should have a mind map-like diagram that illustrates the output of your team activity.

Each team will briefly present their design back to the cohort. Once all teams have shared their design, its time to consolidate everything into one master diagram that will be used throughout the exercises.

You will expand on this master diagram as you continue through this course

**✍️ Do in Purview:** [10 minutes] Using your master diagram, transfer your business domains, descriptions, owners etc into the Purview Data Governance Portal. You will build on these going forward. You can mark them as 'draft' and notice how the results will be hidden from the search results.

## Task 2: Map Business Domains to Data Map Collections

**🎯 Outcome:** At the end of this task, you will have scoped your business domains to a subset of collections from your Data Map.

### Understanding the relationship between Business Domains and Data Map Collections

Business Domains may change frequently as your organization evolves or adopts Purview, and thus responsibilities for data assets may shift too. When you map your business domains to your data map collections, you are creating a link between the business context and the technical data assets.

This link (mapping to Data Map collections) is crucial for ensuring that data assets are managed and governed effectively. By mapping business domains to Data Map collections, you can ensure that the right people are responsible for, and the right policies applied to, the correct data assets.

**🫂 Team Activity:** [5 minutes] As a group, discuss the relationship between the Data Map's Collections and the Data Catalog's Business Domains.

- For a given Business Domain, which collection hierarchies would you expect to be included?
- What are the key data assets that would be included in this Business Domain?

**✍️ Do in Purview:** [5 minutes] Perform the required mapping for your business domains. This will help you to scope the data assets that are relevant to each business domain during the data curation and discovery phases.

## Task 3: Create Business Domain Terms (Glossary Terms)

**⏰ Duration:** 10 minutes

**🎯 Outcome:** At the end of this task, you will have defined one or more Business Domain Terms (glossary terms / vocabulary) for your newly created business domains.

### Understanging Business Domain Terms

Business domain terms, or glossary terms, are crucial for managing, governing, and making data discoverable. These terms are more than just a vocabulary for business users; they are related to data assets, categorized. and provide context - greatly simplifying technical jargon associated with your data or industry. Terms play a key role in data governance, helping data stewards to apply policies and scale data governance as the data estate expands.

Data Governance Scalability is achieved by transforming previously static glossary terms (in prior versions of Azure Purivew) into active terms containing policies going forward. This change allows automatic application of associated policies every time the term is applied to a data product, hence ensuring security and discoverability while offloading the burden from data stewards.

**Key Facts**

- **Terms** are grouped under their respective Business Domains as to provide context for each segment of your company, hence aiding the team to differentiate between the meanings if ever a term is shared across different domains.

- **Policies** attached to the terms provide specific business health goals, data governance requirements, and terms of use to any data product that the term is applied to.

- **Custom Attributes** can be added to the glossary terms to provide more information, and they can be edited, updated or removed as per business requirements.

- **Publishing** a Term makes it visible to all users, this step needs to be performed once the term is ready to be used within the business domain.

- **Linking Data Products** to Terms is a feature that allows glossary terms to become more contextual and accurate to their business domain.

- **Related Terms** provide better business context and can be managed from the glossary term page. They can be added as a synonym or a related term and can be removed when necessary.

### Excersise: Creating Business Domains Terms

**🫂 Team Activity:** [5 minutes] Discuss how your organization handles acronyms and word dictionaries today.

- Where do new starters go to get familiar with your glossary today?
- Do you have one or more large spreadsheet(s) of terminology?
- Are you using a SharePoint site to let users discover business terms?
- How beneficial would it be to co-locate the business glossary with the data governance tooling

**✍️ Do in Purview:** [5 minutes] Create new terms for Business Domains of your choosing and note the 'steward' and 'expert' fields where you can assign a respective colleague.

**✨ Pro Tip:** Try out the new Copilot integration to generate industry-relevant terms.

**✨ Pro Tip:** Try out the new Term Policies features.

---

**⏸️ Reflection:** At this point you have implemented one or more business domains and articulated the value of business concepts over your physical data estate to assist in data governance. You have also created glossary terms to provide context to your data assets. Ready to move on?

👉 [Continue: Lab 5](./Lab-05%20-%20Curating%20Data%20Assets.md)
