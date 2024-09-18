![Banner](./assets/banner.png)

# Lab 7: Objectives and Key Results (OKRs)

## Task 1: Creating OKRs

> Microsoft Purview Solution: Data Catalog

**⏰ Duration:** 20 minutes

**🎯 Outcome:** At the end of this task, you will have linked data products created in [Lab 5](/Lab-05.md) to OKRs in your governance domains to associate metrics that matter with data products that drive them.

### Understanding Objectives and Key Results (OKRs)

Objectives and Key Results (OKRs) provide a broadly adopted strategy for setting and communicating goals and results within an organization. The purpose of OKRs is to connect the objectives of a company or team to measurable results.

**Why do we bring OKRs into a Data Governance Solution?** Imagine you're a data scientist in an IT division, tasked with helping the sales unit improve its customer retention rate. You likely have little or no idea which expert data assets are available because you don't usually interact with the sales team and even less so, have an understanding which data sets will help you complete the task.

That's where OKRs shine! By linking data products to objectives, you empower users to easily find the data sets that directly influence or are most relevant to the business objective. This is especially useful in large organizations where data assets are spread across multiple business units and teams may be required to collaborate across departments. When used with the Microsoft Purview Copilot experience, the additional context OKRs and linked Data Products provide, can greatly improve the search experience for business users.

Here is an example of a Human Resources Objective with four Key Results. One Data Product has been linked to the Objective:

![Example OKR](/assets/okr-overview.png)

### Exercise: Creating an OKR

**🫂 Team Activity:** [10 minutes] Choose a governance domain and discuss what this business unit is measured on, what they "care" about.

- Are there any executive mandates or strategic initiatives that are top of mind?
- Can you identify any metrics that are tracked to measure success in this domain?
- What are the key results that would indicate success in this domain?
- Who owns the objectives that the business unit is working towards?

**✍️ Do in Purview:** [5 minutes]

- Using the 'New OKR' option in a governance domain of your choice, add the name, owners, and target date.
- Once the OKR is created, open it up and add a key result to create the measures that feed this objective.
- You can also explore the 'Link data product' option if you have data products that you created in the previous Lab which relate to this objective. Data products need to be published before they can be linked.
- Note the Status option. The objective is in Draft until you select 'Publish'.

The back on the governance domain's OKR overview page, you can now see the objective and key results that have been created. You can also see the overall progress of the OKR. This is calculated based on the average of the progress of the key results.

![OKR Overall Progress](./assets/business-domain-okr-list.png)

---

**⏸️ Reflection:** Now that you have seen how OKRs can be used to link business objectives to data products, how do you think this will help your organization? What are some of the challenges you foresee in maintaining these links as the business evolves?

👉 [Continue: Lab 8](./Lab-08%20-%20Health%20Management%20Controls.md)
