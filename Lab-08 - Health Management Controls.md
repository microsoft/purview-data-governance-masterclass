![Banner](./assets/banner.png)

# Lab 8: Health Management Overview

**⏰ Duration:** 30 minutes

**🎯 Outcome:** At the end of this task you will understand the importance of data estate health and the tools provided by Purview to manage data estate health.

## Introduction

Data estate health is the degree to which an organization's data assets are accurate, consistent, complete, accessible, secure, and compliant with business rules and regulations. Data estate health is a key factor for ensuring data quality, trust, and value across the data lifecycle.

In the age of AI , it is imperative that we have accurate information about the health of our data to ensure that our models can provide the most best insights grounded on reliable and trustworthy data.

While organizations understand the need to have healthy data and the key requirements for achieving data health, they very seldom have practices in place to evaluate the health of their estate.

The purpose of Health Management is Purview is to provide customers with the tools they need to evaluate the progress on their quest for healthy data. Given that data estates are growing rapidly managing the data itself is challenging enough, staying on top of data health is often treated as a secondary objective.

By having a toolset available which can quantify the health of the data estate, emphasis can be placed on the importance and need to have a more proactive and dedicated approach to improving data health and drive behavior and decisions to actively improve it.

## Task 1: Understand the Health Management Controls

> Microsoft Purview Solution: Data Data Catalog

**⏰ Duration:** 15 minutes

**🎯 Outcome:** At the end of this task you will understand the 8 key pillars for data estate health. In Purview these can be considered the health control groupings. All individual controls fall into one of these groups.

### What are the 8 Key Pillars for Data Estate Health?

With health controls you can define and measure the vital signs of your data across the 8 key pillars critical for the health of any data estate:

- Access and use

  Do we have the right policies and procedures in place to facilitate access and compliant use of data? I.e. Do we have self-service data access policies in place? Are users declaring the intended use of the data?

- Discoverability:

  Are we enabling users to find the data they need? To what extent have we made data products available to our users with relevant data assets mapped.

- Estate Curation

  Are data products suitably classified and labelled?

- Health Observability

  Do we have the right tools in place to monitor the health of our data estate?

- Value Creation

  Are data products aligned to business outcomes?

- Trusted Data

  Do we know who owns the data? Has it been certified and quality checked?

- Metadata Quality Management

  How well are the data products and assets described?

- Data Quality Management

  What is the quality of our data in terms of accuracy, completeness, conformity, uniqueness, consistency and timeliness?

### Exercise: Review the Health Controls Dashboard

**🫂 Team Activity:** [15 minutes] Review the [available health controls](https://learn.microsoft.com/en-us/purview/how-to-health-controls) and discuss the importance of each of health control within your organization.

**✍️ Do in Purview:** [15 minutes] Using the Health controls tool, navigate to the Health Controls dashboard and review the health controls available.

![Register data source button](./assets/health-control-dashboard.png)

Here you will see a summary of the health controls and the number of controls that are in place. Initially there will not be any current scores displayed as these are calculated based on the controls that are in place and the rules that are defined. Once the controls are in place and the rules are defined, the scores will be calculated and displayed.

- Active controls: The number of controls that are currently in place
- Not Healthy: The number of controls which are considered not healthy based on the health status rules that have been defined.
- Fair: The number of controls which are considered fair based on the health status rules that have been defined.
- Healthy: The number of controls which are considered healthy based on the health status rules that have been defined.
- Expired: A control would be expired when it is not being evaluated or is no longer needed because it is always green, which would be rare.  The control can be set to not active which will make it expired.  This happens in the health control edit panel by flipping the active switch at the top.  This requires data health owner permissions.

Clicking on the arrow next to a control group, expands the list of controls within that group. Click on a control name to view the details of the control. This will show you a graph of the recent score, the control description, the health status, the owner, the business domain,the target value and when the control was created.

![Health Control Details](./assets/health-control-details.png)

**✨ Pro Tip:** The Health controls dashboard allows you to view your data estate health at a glance as a grid, a tree view or a chart view. You can also filter the controls by health status, Business domain, owner or keyword.

---

## Task 2: Updating Health Controls and thresholds

> Microsoft Purview Solution: Data Catalog Health Controls

**⏰ Duration:** 15 minutes

**🎯 Outcome:** At the end of this tasks, you will have updated the properties of a health control.

### Exercise: Edit health control properties

**✍️ Do in Purview:** [10 minutes]

1. Using either the tree view or grid view, select a health control and click on the Edit button. (The edit button is the pencil icon). This will bring you to the Edit control window for the specific control.

   ![Edit Health Control](./assets/edit-health-control.png)

2. On the Details tab, update the owner of the control.

3. Update the description of the control.

4. Select the business domains that the control is applicable to.

5. Decide if the control is active or not.

### Exercise: Update Thresholds

**✍️ Do in Purview:** [15 minutes]

The thresholds tab enables you to configure how the health status will be displayed on the Health Controls Dashboard.

1. While in the Edit control window, click on the Thresholds tab. This will show you the thresholds that are in place for the control. Thresholds are configured at the individual control level.
   ![Configure status rules](./assets/edit-status-rules.png)

2. Click on the New threshold button, which will add an if-then statement where you can configure the condition for one of the following statuses:

   - Healthy
   - Fair
   - Not healthy
   - Critical
   - Undefined

3. Configure the threshold by selecting the

- condition,
- the operator and
- the target value.

4. Click on the save icon to save your control changes and close the window.

## Task 3: Health control rules

> Microsoft Purview Solution: Data Catalog Health Management

**⏰ Duration:** 15 minutes

**🎯 Outcome:** At the end of this task you will understand how to configure health control rules.

The health control rules measures the performance of each of your controls.

### Exercise: Review Health Control Rules

**✍️ Do in Purview:** [15 minutes]

Click on the Rules tab in the Edit control window to view the rules that are in place for the control.

![Register data source button](./assets/meta-data-quality-rules-default.png)

In this example shown in this screenshot is the rule for "Self-serve access enablement". This rule is defined as follows:

- Scope: The scope to which this rule should apply. In this case it applies to the Data product scope. The scope is determined by the type of rule that is being defined. Highlighted in light blue.
- Rule name: The name of the rule. In this case the last rule is "Classification count of related data assets". Highlighted in light purple.
- Comparison operator: When a comparison operator is relevant, it is defined here. In this case the comparison operator is "Greater than". Not all rules have comparison operators as in some cases it can be a binary rule. This will be shown in green.
- Value: The target value that the rule is compared against. In this case the value is 0. This means that the rule will be considered healthy if the number of published terms of use is greater than 0.

**🫂 Team Activity:** [15 minutes] Review the other rules available and discuss the importance of each of these rules within your organization. Consider the relevance and target values of each rule in your discussion.

**Permission Requirement:** To update and manage the control rules, you need to have the data health owner permissions assigned to you.

### Exercise: Update and Create Health Control Rules

> Microsoft Purview Solution: Data Catalog

**⏰ Duration:** 25 minutes

**🎯 Outcome:** At the end of this exercise, you will

- have updated the logic of an existing health control rule and
- created a new health control rule
- combined 2 health control rules
- Updated the severity of a health control rule

**✍️ Do in Purview:**

#### Update an existing Control rule

Following on from the previous exercise, we will now edit one of the control rules.

1. Click on the Edit button (the pencil icon) which becomes visible when you hover over the rule.
   ![Edit Health Control](./assets/edit-health-control-rule.png)This will open the editable settings for the specific rule.

2. Select the relevant comparison operator and target value for the rule. (If applicable). In this example the rule is binary and the valid options are only Is true or Is false.
   ![Edit Rule Value](./assets/edit-health-control-rule-2.png)

3. Click on the check mark button to accept the changes to the rule.

4. Click on the Save changed button to save the changes to the rule.

---

#### Create a new Health control rule

1. Continuing on from the previous exercise we will now add an additional rule to the Self-service access enablement control.

2. Click on the Add rule button, which will open a list of all available rules that can be added to the control.
   ![Add Rule](./assets/add-metadata-quality-rule.png)

3. Scroll through the list of available rules and select the rule that you want to add to the control. Click on the OK button to add the rule.

4. Configure the rule by selecting the operator and the target value.

5. Click on the check mark button accept the changes.
6. Click on the Save changes button to save the changes to the rule.

**✨ Pro tip:** Control rules can be combined using the logical operators AND/OR after rule creation to create complex rules that are relevant to your organization.

Combine two rules by checking the checkbox next to the rule and clicking on the "Combine rules" button. This will allow you to select the logical operator that you want to use to combine the rules.
![Combine Rules](./assets/combine-rules.png)

---

#### Update the severity of a health control rule

1. Click on the Configure severity button to open the severity configuration window.
   ![Configure Severity Button](./assets/configure-severity-button.png). This will open the severity configuration window.

2. Click on the control for which you want to configure the severity of the rules and select the severity level that you want to assign to the rule.

- Low
- Medium
- High

  ![Configure Severity](./assets/configure-severity.png)

3. Click on the Save button to save the changes to the severity level of the rule.

---

### Exercise: Schedule Control Refresh

**✍️ Do in Purview:**
[15 minutes] Schedule Control refresh.

Schedule control refreshes by clicking on the Schedule Refresh button at the top of the health controls screen.

- Select a start date and time for the refresh
- Select the desired time zone
- select the frequency of the refresh (daily, weekly, monthly)
  ![Schedule Control Refresh](./assets/schedule-control-refresh.png)

**⏸️ Wait:** Wait for the control refresh to run and check the health control dashboard to see the updated health status of the control.

---

**⏸️ Reflection:** The health control rules are a powerful tool to define how the quality of your data estate should be measure. How do you think you can use these rules to improve the quality of your data estate?

👉 [Continue: Lab 9](./Lab-09%20-%20Data%20Quality%20Management.md)
