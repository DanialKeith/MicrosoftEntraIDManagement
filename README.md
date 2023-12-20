# Microsoft Entra ID User & Group Creation/Access Management Configuration

## Objective
This report details the configuration and observation of various roles within Microsoft Entra Identity and Access Management (formerly Azure Active Directory), emphasizing their specific capabilities and limitations.
## Configuration and Observation Process
### 1. Tenant-Level Global Reader Role
-	**User Creation and Role Assignment**
  -	Created a user, ``GlobalReaderJohn``, in Microsoft Entra ID.
    -	Accessed Microsoft Entra ID, clicked “Add,” “User,” then “Create new user.”
          
    ![1](https://github.com/DanialKeith/MicrosoftEntraIDManagement/assets/154257195/f11127c4-6577-4341-8e63-01cb2c05d757)


    - Assigned principal name ``GlobalReaderJohn@Random[.]onmicrosoft[.]com`` and generated a password.
   		
![2](https://github.com/DanialKeith/MicrosoftEntraIDManagement/assets/154257195/1bbc7229-1d10-4c36-a473-506c8f3aa037)


  - Assigned the Global Reader role.
    - Selected Global Reader in the role assignment.

![3](https://github.com/DanialKeith/MicrosoftEntraIDManagement/assets/154257195/0822a6dd-21ff-4f91-a216-45b517fba373)

![4](https://github.com/DanialKeith/MicrosoftEntraIDManagement/assets/154257195/e0b03625-cf25-4711-9406-d88f3151013b)

 
-	**Observation and Limitations**
    -	Logged in as ``GlobalReaderJohn`` in an incognito browser.
    -	Capabilities: Read-only access to most resources and settings across the tenant.
    -	Limitations: No ability to make changes or modifications.
-	**Closing Actions**
    -	Concluded the session and closed the browser.
    
### 2. Subscription-Level Reader Role
-	**User Creation and Role Assignment**
    -	Created another user, ``SubReaderJane``, in Microsoft Entra ID.
        -	Implemented the same procedure as used for ``GlobalReaderJohn``. However, it's important to note that assigning the specific role for this user cannot be completed directly within Microsoft Entra ID.
      
    ![5](https://github.com/DanialKeith/MicrosoftEntraIDManagement/assets/154257195/f3729029-8d89-4db6-a6eb-3e26dce62ae6)


    -	Assigned Subscription-Level Reader role.
        -	Navigated to “Azure subscription 1,” accessed ‘Access control (IAM),’ ‘Add,’ and selected ‘Add role assignment.’
      
        ![6](https://github.com/DanialKeith/MicrosoftEntraIDManagement/assets/154257195/d6f978f4-13b6-44db-a06e-be6b4031cb94)


        - Assigned the Reader role.


![7](https://github.com/DanialKeith/MicrosoftEntraIDManagement/assets/154257195/1c3817cd-e02f-4fe1-85e7-bdd1a6eb092c)


-	**Observation and Limitations**
    - Accessed as ``SubReaderJane`` in a new incognito session.
    -	Capabilities: Reading access to all resources within a specific subscription.
    -	Limitations: Read-only access without editing or managing capabilities within the subscription.
-	**Closing Actions**
    -	Concluded the session and closed the browser.
### 3. Resource Group Contributor Role
-	**User Creation and Resource Group Setup**
    -	Created ``RgContributorDave`` in Microsoft Entra ID and established “Permissions-Tester” resource group.
        - Followed similar user creation steps, however within ‘Resource Groups’.
      
	![8](https://github.com/DanialKeith/MicrosoftEntraIDManagement/assets/154257195/d0f2ec43-45fd-4573-bd40-7b752654d0b0)


-	**Role Assignment and Observation**
    -	Assigned Resource Group-level Contributor permissions to ``RgContributorDave``.
    -	Capabilities: Administrative control at the resource group level.
    -	Limitations: Management confined to the assigned resource group; no permission for broader access management.
-	**Closing Actions**
    -	Concluded the session and closed the browser.
## Conclusion
This exercise highlights the distinct functions and limitations of Microsoft Entra ID roles, essential for effective management:
-	Tenant-Level Global Reader: Ideal for monitoring, with no management or change capabilities.
-	Subscription-Level Reader: Suitable for monitoring within a single subscription, lacking management capabilities.
-	Resource Group Contributor: Provides administrative control within a specific resource group, but does not extend to broader management.
Appropriately assigning these roles within Microsoft Entra environments is critical for maintaining a balance between access rights and security.

