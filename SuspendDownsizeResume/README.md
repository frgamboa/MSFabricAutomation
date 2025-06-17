# Microsoft Fabric Suspend and Downsize scripts 

In order for the scripts to work, you need to create an application in Microsoft Entra, and then you will need to grant contributor access in Microsoft Fabric to this application you created in Entra, then create an automation account in Azure, in which you can implement the code. Once the code is implemented, you can create the schedule and assign it to the runbook.

I am sharing these as an alternative for people who may be in this situations, I am, by no mean, a developer, these scritps are shared understanding that they can be greatly improved, as they work more as a "proof of concept" than a finished job, and I do not improve them because as they are, they are good enough for my use case.


## To register an application in EntraId
Yo can refer to [this](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app?tabs=certificate) link to have detailed isntructions on how to register the application. Please keep in mind that the secret will only be visible right after creating it, as you will need it to customize the scripts


## To create teh automation runbook:

Azure automation [run books](https://learn.microsoft.com/en-us/azure/automation/overview)

In my case, after creating the runbook I created a schedule, to have this running periodically, other uses are to create webhooks that you can invoke from your data pipelines in fabric (to upsize it at teh begining of the data orchestration activities, or downsizing it, once teh data orchestratino activities are done).


## To learn more about the azure built-in roles
Azure [Builtin roles](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles)


## Disclaimer

This code is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. In no event shall the author(s) be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the software or the use or other dealings in the software.

Test it before using it, following your standard testing procedures, review the code and edit any part that you consider needful, beyond the ones you will need to modify, in order to have the code working.
