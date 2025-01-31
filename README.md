![Banner](./assets/banner.png)

# Microsoft Purview Data Governance End-to-End

> **Disclaimer:** This guide was created by [Olaf Wrieden](https://www.linkedin.com/in/olafwrieden) and [Minette Steynberg](https://www.linkedin.com/in/msteynberg) Data & AI Cloud Solution Architects, to collate guidance, information, and best practices to support conversations and workshops. It is tailored to assist you in starting a new Microsoft Purview Data Governance implementation from scratch. Organizations with existing workloads looking to [migrate to the new Purview experience](https://learn.microsoft.com/en-us/purview/new-governance-experience#how-can-you-use-our-new-experience) may do so by following the supported migration paths, old concepts are not covered by this guide.

## 🤷🏼 Purpose

This masterclass is designed to educate attendees on the end-to-end implementation of Microsoft Purview Data Governance in a "zero-to-hero"-style of approach. It assumes attendees know nothing about Purview or its functionality, but have defined a set of data governance requirements.

This masterclass is split into multiple labs, each with its own objectives. At the end of this masterclass, participants will be equipped with a better understanding and functional knowledge to continue an implementation of data governance throughout their organization. This masterclass focuses on part conversation, part hands-on configuration in the Purview portal - with best practices and valuable take-aways throughout.

🛣️ **Roadmap:** [Discover what's new and what's coming](https://learn.microsoft.com/en-us/purview/whats-new) in Microsoft Purview.

## 🗺️ Content Navigation

These labs build on one another. It is recommended to follow them in order.

- **1-Day Workshop (8 hours)**
  Please _ignore_ the **✍️ Do in Purview** exercises and focus on the discussion-based tasks instead.
- **3-Day Workshop (24 hours)** Complete all tasks, including the practical exercises (see Attendee Pre-requisites below). Ample time is provided for discussion and reflection.

Allow for a 15-minute break at least every 90 minutes (at the facilitator's discretion) and allow for an approximately 1-hour lunch break.

## 🧑🏼‍🎓 Audience

This masterclass is designed for: Data Stewards, Data Governance Managers, Domain/Business Owners, and Data Security Specialists who have a fundamental understanding of Data Governance and terminology.

## 📋 Attendee Pre-requisites

Each attendee should have access to the Purview portal at [purview.microsoft.com](https://purview.microsoft.com) and be granted permission to administer the Unified Catalog (either temporarily or permanently) for the purpose of this workshop.
If interested in loading existing business glossaries, the attendee should bring their business glossaries in an Excel spreadsheet to be loaded into Purview.

### Pre-reqs and Implications of Practical Exercises

Completing the **✍️ Do in Purview** practical exercises attendees to access the Purview Data Governance instance. Currently, there is no lab environment available to support this requirement.

- If the organisation has created a new Purview instance to support this workshop, then that instance will become the [primary Purview account for that tenancy](https://learn.microsoft.com/purview/new-portal-faq#what-does-this-mean-for-my-existing-microsoft-purview-governance-portal-accounts). Currently, customers cannot change this, once created. If they need to request a change, it will require a service request to Microsoft support services.
- Beware that changes made to the Microsoft Purview account may thus directly impact the production environment.
- Some artifacts, when created cannot be deleted. For example, a Data Product cannot be deleted if it has an active subscriber. It can only be renamed or 'expired'. This is by design to ensure data integrity.

## 🧑🏼‍🏫 Facilitator's Role

In addition to being a Purview expert, the facilitator's role is to facilitate an equal balance of productive discussion / discovery and Purview portal configuration progress. Timings per task are indicative only, and pace should be determined by the facilitator. The entire business data estate will not be fully curated at the end of this masterclass, rather, attendees will be equipped to continue the curation process themselves (due to time investment required).

## 📃 Agenda

The following is a suggested agenda for an action-packed 1 or 3-day workshop:

1. Executive Overview & Introduction.
2. Data Map Foundations.
3. Sensitivity Labels and Lineage Connections.
4. Registering Data Sources.
5. Defining Scans and Scan Rule Sets.
6. Custom Data Classifications.
7. Curating Data Assets.
8. Designing for Governance Domains.
9. Managing an Enterprise Glossary.
10. Bundling Assets into Data Products.
11. Self-Service Access Requests.
12. Articulating Business OKRs.
13. Defining Health Management Controls.
14. Tracking Data Quality.
15. Taking Action on Data Health Alerts.
16. Data Health Reports & Insights.
17. Asset Auditing and History.
18. Custom functionality with APIs and SDKs.
19. Business Continuity and Disaster Recovery.
20. Pricing and Licensing.

## 🗃️ Microsoft Purview Solutions

Throughout this masterclass, you will interact with the following Microsoft Purview solutions:

- Data Map
- Unified Catalog
- Information Protection
- Audit
- Settings

## Icon Legend

Throughout the labs, you will see the following icons. Take a minute to familiarize yourself with them before starting the labs.

- 🎯 **Outcome:** Refers to the learning or implementation outcome that is achieved at the end of the task.
- 🫂 **Team Activity:** Refers to a group activity that will take place, usually a discussion, team breakout or other interaction.
- ✍️ **Do in Purview:** Refers to an activity to completed in the Purview portal to implement Microsoft Purview functionality.
- ✨ **Pro Tip:** Refers to a takeaway or key best practice from the instructor.
- ⏸️ **Wait:** Refers to short pause or reflection period to await results, for example, waiting for a data source scan to complete.
- ❗**Callout:** An important point to bring to the audience's attention.

## Ready to Start?

👉 [Continue: Introductions & Exec Overview](./Lab-01%20-%20Introduction%20and%20Overview.md)

## Trademarks

Trademarks This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft trademarks or logos is subject to and must follow Microsoft’s Trademark & Brand Guidelines. Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship. Any use of third-party trademarks or logos are subject to those third-party’s policies.
