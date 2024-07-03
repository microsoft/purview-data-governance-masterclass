![Banner](./assets/banner.png)

# Lab 5: Custom Functionality with APIs and SDKs

## Task 1: Capturing Events

**⏰ Duration:** 20 minutes

**🎯 Outcome:** At the end of this task, you will have a better understanding of the Purview APIs available to your organization to build, extend and automate aspects of Microsoft Purview Data Governance.

### Capturing Microsoft Purview Events

Most actions in Purview raise notification 'events' that can be pushed to an Azure Event Hub for external consumption. A custom-coded Azure Function App could be used to react to new events, then execute any business logic and optionally write data back into Purview.

For example, Purview detects a scan failed due to a specific reason, this 'scan failed' event is written to the Event Hub along side additional information, from where an Azure Function (external to Purview) picks it up to execute a piece of code or call other APIs that (for example) restart a virtual machine or self-hosted integration runtime.

**🫂 Team Activity:** [10 minutes] As a team, discuss whether you foresee a need to implement custom integrations and automation using the API.

- Investigate Microsoft Purview's API and SDKs.
- What are the challenges you see that may require the use of the APIs?
- Which department would be owning any potential custom integration work?
- Would your custom business logic / integration be actioned in near real-time or in batches? Ie. do you need to react to an event immediately?

**✍️ Do in Purview:** [10 minutes] Navigate to the Microsoft Purview resource in Azure, then select its Events tab. You can configure a notification and/or a hooks Event Hub. These let Purview either push data out (notify) or consume Apache Kafka messages from external sources.

## Task 2: Utilising APIs and SDKs

**⏰ Duration:** 20 minutes

**🎯 Outcome:** At the end of this task, you will have a better understanding of the Purview APIs available to your organization to build, extend and automate aspects of Microsoft Purview Data Governance.

**🫂 Team Activity:** [5 minutes] Review the Microsoft Purview APIs and SDKs available for you to consume in your own applications.

---

## Congratulations, that's a wrap!

**⏸️ Reflection:** Great job! You now have a better understanding of the Purview APIs available to your organization to build, extend and automate aspects of Microsoft Purview Data Governance.

🏁 [Back to Overview](./README.md)
