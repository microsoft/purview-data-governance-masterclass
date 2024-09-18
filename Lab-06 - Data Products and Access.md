![Banner](./assets/banner.png)

# Lab 6: Mastering Data Products & Data Access

## Task 1: Creating Data Products

**⏰ Duration:** 20 minutes

**🎯 Outcome:** At the end of this task, you will have created one or more data products based on data assets curated in [Lab 5](/Lab-05%20-%20Curating%20Data%20Assets.md), and make these discoverable and consumable through access policies.

### Data Products vs Data Assets

Assets by themselves are not always useful. They typically need to be packaged together in a meaningful way to be useful for a specific use case. For example, a single fact table of 'Sales' likely requires 'Customers', 'Sales Representatives', and 'Regions' dimension tables to make the sales data more useful for analysis or reporting. This is where data products come in. They are the building blocks for data consumers to discover, understand, and consume data assets by grouping commonly used together data assets into a single package, a data product to which users can subscribe.

Data Products can be published for consumption by users throughout the organization. They can be associated with governance domains, business glossary terms, and objectives and key results (OKRs) to provide context and alignment with business goals (more on this in the next lab).

Finally, data products can be secured with access policies to control who can access the data assets within the data product, track active subscribers, and revoke access in a timely manner.

### Exercise: Create Data Products

**🫂 Team Activity:** [10 minutes] Identify a business unit (governance domain) and [on a whiteboard] map out their data assets into groups that can easily be packaged together for specific use cases. It may be that transaction information and customer details that can be grouped into an Open Banking data product for example.

While Microsoft Purview advocates for a one-to-many relationship between data assets and data products, it is important to note that a data asset can belong to no, one, or more data products. You may decide to implement a one-to-one mapping between assets and data products, but consider how this approach scales across thousands of data assets in the organization. It may thus present an anti-pattern.

**✍️ Do in Purview:** [5 minutes]

- Define your Data Products per governance domain via the 'New data product' wizard. Supply a name and description, and list the use cases in the respective text area. Take advantage of rich text and bullet points for better readability.
- In the data product overview, note the status (draft/published).
- Now associate Data Assets via the 'Add data assets' option as per the whiteboard exercise above. The data assets added here should be relevant to the data product and may belong to no, one, or more data products.
- Associate any Terms via the 'Add term' option.
- Associate any OKRs via the 'Add OKR' option (more on this in the next lab).
- Review the data product owner contact, and ensure it correctly reflects the employee(s) directly responsible for its upkeep.

**✨ Pro Tip:** To speed up your curation experience, explore the option to let Copilot discover recommended data assets to associate with each data product.

## Task 2: Defining Data Product Access

**⏰ Duration:** 15 minutes

**🎯 Outcome:** At the end of this task, you will have defined access controls for the data product to enable it for self-service consumption.

### Understanding Data Product Access

Access policies are essential to ensure that data is used responsibly and in compliance with organizational policies. Data Access defines who can access the data product, what they can do with the data, and under what conditions they can access the data. Access policies are defined at the data product level and enforced across all data assets within it.

**🫂 Team Activity:** [15 minutes] Discuss access controls for a given data product you created in Task 1 of this lab.

- What are the list of authorized purposes for accessing and using the data product? These may already be outlined in the data product use cases. Outline the data usage purposes with a name and brief description to put access requests into context for business users.
- Define the access approval requirements for the data product. Who are the people that need to approve and grant access to the physical data assets in the data product?
- Should employee manager approval be required?
- Is a privacy and compliance review required?
- Does the requestor need to accept any data use terms before proceeding with the request?
- What is the maximum duration for which access can be granted at any one time?

**✍️ Do in Purview:** [10 minutes] Now define data product access using the 'Manage access' option and add the relevant purpose and approval requirements based on the team activity. Repeat with other data products.

---

**⏸️ Reflection:** You have now created data products and defined access controls for them. How do you think this will help your organization in making data more discoverable and consumable? What are some of the challenges you foresee in maintaining these data products and access controls as the business evolves?

**✨ Pro Tip:** Remember that you are aiming for a federated data governance model. The task of maintaining data products and access isn't all on you.

👉 [Continue: Lab 7](./Lab-07%20-%20OKRs.md)
