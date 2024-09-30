![Banner](./assets/banner.png)

# Lab 12: Custom Functionality with APIs and SDKs

## Task 1: Capturing Events

**⏰ Duration:** 20 minutes

**🎯 Outcome:** At the end of this task, you will have a better understanding of the Purview APIs available to your organization to build, extend and automate aspects of Purview Data Governance.

### Context

Azure and its services are programmatically addressable via [REST APIs](https://learn.microsoft.com/rest/api/azure). Representational State Transfer (REST) APIs are service endpoints that support sets of HTTP operations (methods), which provide create, retrieve, update, or delete access to the service's resources. This enables the interoperability between services, the creation of customised solutions/UI's, integration with 3rd party process and tooling, etc.

Classic Purview Data Governance reflected the [Apache Atlas](https://atlas.apache.org) API set and many organisations used these to extend upon the classic out-of-the-box feature set.

For Purview's New Data Governance experience, the [Data Map APIs](https://learn.microsoft.com/rest/api/purview), remain as they were for Classic. New API's covering the New Experience feature set are planned to have a stable release in H1/2025.

✨ **Pro Tip:** While some of the new API's are currently available, they should be treated as Public Preview (PP). As per Microsoft's [Terms of Use](https://azure.microsoft.com/support/legal/preview-supplemental-terms/?msockid=2114a70960fe65991122b5c4618d6462), features can change and there is no guarantee that a feature appearing in PP will make it to General Availability (GA). Therefore, [Caveat emptor](https://en.wikipedia.org/wiki/Caveat_emptor) applies.

### Capturing Microsoft Purview Events

Most actions in Purview raise notification 'events' that can be pushed to an [Azure Event Hub](https://learn.microsoft.com/azure/event-hubs/event-hubs-about) for external-to-purview consumption. A custom-coded [Azure Function](https://learn.microsoft.com/azure/azure-functions/functions-overview) App could be used to react to new events, then execute any business logic and optionally write data back into Purview.

For example, Purview detects a scan failed due to a specific reason, this 'scan failed' event is written to the Event Hub alongside additional information, from where an Azure Function (external to Purview) picks it up to execute a piece of code or call other APIs that (for example) restart a virtual machine or self-hosted integration runtime.

❗**Callout:** By creating custom processes as above, carefully consider the trade-off between the desired functionality and the Product ownership roles this introduces across the full SDLC lifecycle. i.e. patching, updates when services are updated, validation/updates when Azure changes, etc. If you do decide to customise a process, create a Key-Design-Decision (KDD) which articulates the rationale, considerations, and implications. This will create transparency and an audit trail for this decision.

**🫂 Team Activity:** [10 minutes] As a team, discuss whether you foresee a need to implement custom integrations and automation using the API.

- Investigate Microsoft Purview's API and [SDKs](https://learn.microsoft.com/purview/tutorial-using-python-sdk).
- What are the challenges you see that may require the use of the APIs?
- Which department would be owning any potential custom integration work?
- Would your custom business logic / integration be actioned in near real-time or in batches? i.e. do you need to react to an event immediately?

**✍️ Do in Purview:** [10 minutes] Navigate to the Microsoft Purview resource in Azure, then select its Events tab. You can configure a notification and/or a hooks Event Hub. These let Purview either push data out (notify) or consume Apache Kafka messages from external sources.

## Task 2: Utilizing APIs and SDKs

**⏰ Duration:** 20 minutes

**🎯 Outcome:** At the end of this task, you will have a better understanding of the Purview APIs available to your organization to build, extend and automate aspects of Microsoft Purview Data Governance.

**🫂 Team Activity:** [5 minutes] Review the Microsoft Purview APIs and SDKs available for you to consume in your own applications.

---

**⏸️ Reflection:** You now have a better understanding of the Purview APIs available to your organization to build, extend and automate aspects of Microsoft Purview Data Governance. Lastly, let's review the pricing and licensing for Microsoft Purview.

👉 [Continue: Lab 13](./Lab-13%20-%20Pricing%20and%20Licensing.md)
