![Banner](./assets/banner.png)

# Lab 11: Business Continuity and Disaster Recovery

## Task 1: Understand your Responsibilities

**⏰ Duration:** 15 minutes

**🎯 Outcome:** At the end of this task, you will have understood your backup/restore, and [disaster recovery](https://learn.microsoft.com/azure/reliability/disaster-recovery-overview) choices and responsibilities.

### What is the SLA for Microsoft Purview?

At the time of writing, Microsoft Purview as a [SaaS](https://azure.microsoft.com/resources/cloud-computing-dictionary/what-is-saas/?msockid=2114a70960fe65991122b5c4618d6462) service, has a **99.9%** uptime Service Level Agreement (SLA). This SLA is based on the Monthly Uptime Percentage formula.
**✨ Pro Tip:** This is a financial guarantee of service. 99.9% (three nines) equates to no more than ~8.76 hours of downtime per year.   

If Microsoft fails to meet this guarantee, you may be eligible for service credits. For more information, including the uptime calculation, please refer to the [Microsoft SLA page](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

### A word on Business Continuity and Disaster Recovery (BCDR)...

Most actions in Purview raise notification 'events' that can be pushed to an [Azure Event](https://learn.microsoft.com/azure/event-hubs/event-hubs-about) Hub for external-to-purview consumption. A custom-coded [Azure Function](https://learn.microsoft.com/azure/azure-functions/functions-overview?pivots=programming-language-csharp) App could be used to react to new events, then execute any business logic and optionally write data back into Purview.

For example, Purview detects a scan failed due to a specific reason, this 'scan failed' event is written to the Event Hub alongside additional information, from where an Azure Function (external to Purview) picks it up to execute a piece of code or call other APIs that (for example) restart a virtual machine or self-hosted integration runtime.

❗- By creating custom processes as above, carefully consider the trade-off between the desired functionality and the Product ownership roles this introduces across the full SDLC lifecycle. i.e. patching, updates when services are updated, validation/updates when Azure changes, etc. If you do decide to customise a process, create a Key-Design-Decision (KDD) which articulates the rationale, considerations, and implications. This will create transparency and an audit trail for this decision.

**🫂 Team Activity:** [10 minutes] Discuss to what extend Purview is considered critical to your business operations. i.e. if purview is offline, what business processes are impacted?

In most cases, an organization wouldn't deem their internal data governance tooling mission critical - but your company's use case, customization, and level of integration may differ.

- Have you documented the [recovery point/time objectives](https://learn.microsoft.com/azure/reliability/disaster-recovery-overview#recovery-objectives)? What are they?
- What happens if someone accidentally deletes the Microsoft Purview Azure resource or defaults on your company's Azure subscription payment?
- Do you know your Purview account creator? document their name and details. There can only be one creator, and you can only transfer this role to another staff member by filling out an Azure Support ticket.
- Have you implemented a '[break-glass](https://learn.microsoft.com/purview/concept-best-practices-security#implement-a-break-glass-strategy)' strategy to gain emergency admin access to your Microsoft Purview account?

**✍️ Do in Purview:** [5 minutes] As with any Azure service, there are several recommended steps to undertake that ensure your resources are more resilient.

- Navigate to the Purview Azure resource and open its properties. From the Locks section, create a Resource Lock to prevent accidental deletion of the service.
- Navigate to the Purview Azure resource's Alert tab, create a new Alert Rule based on the 'Scan time taken' signal, and set up an alert if the scan time exceeds an acceptable threshold (perhaps 2 hours). This way you will be notified of a long running processes due to incorrect scanning setups.

**✨ Pro Tip:** A native backup/restore functionality may be available in the future. For now, if your requirements exceed Purview's SLA, and you have considered your [DR strategy](https://learn.microsoft.com/azure/architecture/data-guide/disaster-recovery/dr-for-azure-data-platform-recommendations#disaster-strategy-options), you will need a customer implementation via the Purview APIs and SDKs.

---

**⏸️ Reflection:** You just learnt the business continuity and disaster recovery options available to you in Microsoft Purview. Now let's see what you can do with the APIs and SDKs.

👉 [Continue: Lab 12](./Lab-12%20-%20Custom%20API%20Functionality.md)
