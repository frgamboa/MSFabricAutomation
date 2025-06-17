# microsoft Fabric Suspend and Downsize scripts 


In order to this to work, for this to work, you need to create an application in Microsoft Entra, and then you will need to grant contributoraccess in Microsoft Fabric to this application you created in Entra, then create an automation account in Azure, in which you can implement the code. Once the code is implemented, you can create the schedule and assign it to the runbook.

Register an application in EntraId: https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app?tabs=certificate
Azure Builtin roles: https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles
Azure automation run books: https://learn.microsoft.com/en-us/azure/automation/overview
