![Banner](./assets/banner.png)

# Microsoft Purview Data Governance End-to-End

> **Disclaimer:** This guide was created by [Olaf Wrieden](https://www.linkedin.com/in/olafwrieden) and [Minette Steynberg](https://www.linkedin.com/in/msteynberg) Data & AI Cloud Solution Architects, to collate guidance, information, and best practices to support conversations and workshops. It is tailored to assist you in starting a new Microsoft Purview Data Governance implementation from scratch. Organizations who have existing workloads and are looking to [migrate to the new Purview experience](./Lab-00%20-%20Upgrading%20to%20Microsoft%20Purview.md) may do so by following the supported migration paths, old concepts are however not covered by this guide.

## 🤷🏼 Purpose

This masterclass is designed to educate attendees on the end-to-end implementation of Microsoft Purview Data Governance in a "zero-to-hero"-style of approach. Assuming attendees know nothing about the service or functionality but have defined a set of data governance evaluation or implementation criteria.

This masterclass is split into multiple labs, each with its own objectives. At the end of this masterclass, participants will be equipped with a better understanding and functional knowledge to continue an implementation of data governance throughout their organization. This masterclass focuses on part conversation, part hands-on configuration in the Purview portal - with best practices and valuable take-aways throughout.

## 🗺️ Content Navigation

These labs build on one another. It is recommended to follow them in order.

- **1-Day Workshop (8 hours)**
  Please _ignore_ the **✍️ Do in Purview** exercises and focus on the discussion-based tasks instead.
- **3-Day Workshop (24 hours)** Complete all tasks, including those the practical exercises. Ample time is provided for discussion and reflection.

Allow for a 15-minute break at least every 90 minutes (at the facilitator's discretion) and allow for an approximately 1-hour lunch break.

## 🧑🏼‍🎓 Audience

This masterclass is designed for: Data Stewards, Data Governance Managers, Domain/Business Owners, and Data Security Specialists who have a fundamental understanding of Data Governance and terminology.

## 📋 Attendee Pre-requisites

Each attendee should have access to the Purview portal at [purview.microsoft.com](purview.microsoft.com) and be granted permission to administer the Data Catalog (either temporarily or permanently) for the purpose of this workshop.
If interested in loading existing business glossaries, the attendee should bring their business glossaries in an Excel spreadsheet to be loaded into Purview.

## 🧑🏼‍🏫 Facilitator's Role

In addition to being a Purview expert, the facilitator's role is to facilitate an equal balance of productive discussion / discovery and Purview portal configuration progress. Timings per task are indicative only, and pace should be determined by the facilitator. The entire business data estate will not be fully curated at the end of this masterclass, rather, attendees will be equipped to continue the curation process themselves (due to time investment required).

## 📃 Agenda

1. Exec Overview & Introduction
2. Data Map Foundations
3. Sensitivity Labels and Lineage Connections
4. Registering Data Sources
5. Defining Scans and Scan Rulesets
6. Curating Data Assets
7. Designing for business domains
8. Considerations for Business Glossaries
9. Managing Glossary Terms
10. Articulating OKRs
11. Data Products
12. Data Quality
13. Self-Service Workflows
14. Data Access Requests
15. Bridging Purview Compliance portal to the Data Map
16. Custom Classifications
17. Data Estate Health
18. Asset Auditing and History
19. Custom functionality with APIs and SDKs
20. Business Continuity and Disaster Recovery

## 🗃️ Microsoft Purview Solutions

Throughout this masterclass, you will interact with the following Microsoft Purview solutions:

- Data Map
- Data Catalog
- Information Protection
- Audit
- Settings

## Icon Legend

Thoughout the labs, you will see the following icons. Take a minute to familiarise yourself with them before starting the labs.

- 🎯 **Outcome:** Refers to the learning or implementation outcome that is achieved at the end of the task.
- 🫂 **Team Activity:** Refers to a group activity that will take place, usually a discussion, team breakout or other interaction.
- ✍️ **Do in Purview:** Refers to an activity to completed in the Purview portal to implement Microsoft Purview functionality.
- ✨ **Pro Tip:** Refers to a takeaway or key best practice from the instructor.
- ⏸️ **Wait:** Refers to short pause or reflection period to await results, for example, waiting for a data source scan to complete

## Ready to Start?

👉 [Continue: Introductions & Exec Overview](./Lab-01%20-%20Introduction%20and%20Overview.md)
