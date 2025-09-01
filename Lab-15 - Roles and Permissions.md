![Banner](./assets/banner.png)

# Introduction to Microsoft Purview Roles and Permissions

Managing and securing data is a critical part of any organization’s data strategy. **Microsoft Purview** is a powerful data governance solution that helps organizations organize, protect, and monitor their data. To ensure the right level of access for different users, Purview uses **roles and permissions** to control what actions people can perform. Understanding these roles is essential for effectively managing data security and governance.  

# Microsoft Purview Roles and Permissions Explained  

In Microsoft Purview, different roles and permissions exist at multiple levels to help manage data governance effectively. Understanding these roles is crucial for ensuring that the right users have access to the right resources while maintaining security and compliance.  

The diagram below provides a structured flow of how roles and permissions are assigned in Purview across four key scopes:  

- **Tenant Level**
- **Application Level**  
- **Governance Domain** 
- **Data Map**

The flowchart helps identify the right role based on specific tasks. 

![Flowchart of Microsoft Purview Roles and Permissions](/assets/Purview_Roles_Permission.png)

**✨ Pro Tip:** [Refer here for more information about each role](https://learn.microsoft.com/en-us/purview/data-governance-roles-permissions)

# Best Practices for Assigning Roles and Permissions

Now that we understand the different roles and permissions in Microsoft Purview, the next question is: how do we set them up effectively in an organization?

One approach is to assign users directly through Entra ID (formerly Azure AD) at different levels. While this method works, it can quickly become difficult to manage. As the organization grows and data landscapes expand, keeping track of individual user assignments becomes a challenge—especially when employees change teams or leave the company. Managing access on a user-by-user basis is not scalable and can turn into a significant administrative burden.

A more efficient approach is to use Entra ID groups for role management. Instead of assigning permissions to individual users, you assign them to groups corresponding to specific roles in Purview. This simplifies access management, making it easier to onboard and offboard users while ensuring consistent role assignments. However, in some organizations, IT policies may restrict the creation of too many groups, limiting this approach.

A practical middle ground is to group similar roles together and create fewer Entra ID groups. For example, instead of having separate groups for every Purview role, organizations can consolidate roles with similar permission levels, reducing the total number of groups while still maintaining structured access control.

In the next section, we’ll explore how to implement these strategies in Microsoft Purview and set up permissions efficiently.


## Task 1: Plan and Create Users and Groups in Entra ID

**⏰ Duration:** 30 minutes

**🎯 Outcome:** By completing this task, you will: 

- Successfully created a structured set of users and groups in Microsoft Entra ID.
- Established a role-based access management approach.
- Gained hands-on experience with user and group management in Entra ID.
- Prepared a foundation for further access control and security configurations in the next task.

## Exercise: Create users and groups 

**🫂 Team Activity:** [15 minutes] Before creating users and groups, it's important to plan their structure based on your organization's needs. 

**✍️ Do in Purview:** [15 minutes]

    1. Create Users in Entra ID

    2. Create Groups in Entra ID

    3. Add members to the group

    4. Review and Validate

**✨ Pro Tip:** For additional guidance, refer to the Microsoft documentation: [Manage users and groups in Entra ID](https://learn.microsoft.com/en-us/training/modules/manage-users-and-groups-in-aad/).


## Task 2: Assign Roles and Permissions in Microsoft Purview

**⏰ Duration:** 25 minutes

**🎯 Outcome:** By completing this task, you will: 

- Successfully assigned user groups to roles within Microsoft Purview.
- Ensured role-based access control for efficient data governance.
- Validated that users have the necessary permissions to carry out their tasks.
- Strengthened security and compliance within the organization’s data environment.

## Exercise: Assign Permission

**✍️ Do in Purview:** [25 minutes]

    1. Access Microsoft Purview
    
    2. Assign Groups to Roles
    
    3. Validate Role Assignments

**✨ Pro Tip:** For additional guidance, refer to the official Microsoft documentation on [Microsoft Purview roles and permissions](https://learn.microsoft.com/en-us/purview/data-governance-roles-permissions).

