![Banner](./assets/banner.png)

# Lab 5: Business Continuity and Disaster Recovery

## Task 1: Understand your Responsibilities

**⏰ Duration:** 15 minutes

**🎯 Outcome:** At the end of this task, you will have understood your backup/restore, and disaster recovery choices and responsibilities.

### A word on BC/DR...

Most actions in Purview raise notification 'events' that can be pushed to an Azure Event Hub for external consumption. A custom-coded Azure Function App could be used to react to new events, then execute any business logic and optionally write data back into Purview.

For example, Purview detects a scan failed due to a specific reason, this 'scan failed' event is written to the Event Hub along side additional information, from where an Azure Function (external to Purview) picks it up to execute a piece of code or call other APIs that (for example) restart a virtual machine or self-hosted integration runtime.

**🫂 Team Activity:** [10 minutes] Discuss to what extend Purview is considered critical to your business operations. In most cases, an organization wouldn't deem their internal data governance tooling mission critical - but your company's use case, customisation, and level of integration may differ.

- Have you documented the recovery point/time objectives? What are they?
- What happens if someone accidentally deletes the Microsoft Purview Azure resource or defaults on your company's Azure subscription payment?
- Do you know your Purview account creator? Document their name and details. There can only be one creator and you can only transfer this role to another staff member by filling out an Azure Support ticket..
- Have you implemented a 'break-glass' strategy to gain emergency admin access to your Microsoft Purview account?

**✍️ Do in Purview:** [5 minutes] As with any Azure service, there are several recommended steps to undertake that ensure your resources are more resilient.

- Navigate to the Microsoft Purview Azure resource and open its properties. From the Locks section, create a Resource Lock to prevent accidental deletion of the service.
- Navigate to the Microsoft Purview Azure resource's Alert tab and create a new Alert Rule to based on the 'Scan time taken' signal and set up an alert if the scan time exceeds an acceptable threshold (perhaps 2 hours). This way you will be notified of a potential cost-blowout due to incorrect scanning setups.

**✨ Pro Tip:** A native backup/restore functionality may be available in the future. For now, you will need to implement your own via the Purview APIs and SDKs.

---

## Move on to Lab Last

**⏸️ Reflection:** You just learnt the business continuity and disaster recovery options available to you in Microsoft Purview. Now let's see what you can do with the APIs and SDKs.

👉 [Continue: Lab Last](./Lab-last.md)
