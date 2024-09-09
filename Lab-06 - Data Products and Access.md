![Banner](./assets/banner.png)

# Lab 6: Mastering Data Products & Data Access

## Task 1: Creating Data Products

**⏰ Duration:** 20 minutes

**🎯 Outcome:** At the end of this task, you will have created one or more data products based on data assets curated in [Lab 5](/Lab-05.md), and make these discoverable and consumable through access policies.

### Data Products vs Data Assets

Assets by themselves are not always useful. They typically need to be packaged together in a meaningful way to be useful for a specific use case. For example, a single fact table of 'Sales' likely requires 'Customers', 'Sales Representatives', and 'Regions' dimension tables to make the sales data more useful for analysis or reporting. This is where data products come in. They are the building blocks for data consumers to discover, understand, and consume data assets by grouping commonly used together data assets into a single package, a data product to which users can subscribe.

Data Products can be published for consumption by other users in the organization. They can be associated with governance domains, business glossary terms, and objectives and key results (OKRs) to provide context and alignment with business goals (more on this in the next lab).

Finally, data products can be secured with access policies to control who can access the data assets within the data product.

### Exercise: Create Data Products

