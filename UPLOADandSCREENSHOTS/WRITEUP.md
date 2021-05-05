
In terms of cost, scalability, availability and workflow, deploying the app as a Microsoft AppService is preferable to deploying it on a virtual machine.

						CPU	 RAM			Storage (Temp)		pay as you go / month	

vm 			(https://azure.microsoft.com/en-us/pricing/details/virtual-machines/linux/)
		
D8s v4			8		32 GiB		x					          $316,82/month		

Disk	P15 								256 GiB 1.100 IOPS	$38,01/month

outgoing									5 TB 				        $50,95/month
Traffic

																               $610,58/month

app service (https://azure.microsoft.com/en-us/pricing/details/app-service/linux/)

						 CPU	 RAM			Storage (Temp)		pay as you go / month

Premium V3
Linux
Central US
P3V3 Instanz	8		32 GiB		250GB				      496,40$/month

outgoing									5 TB 				        included
Traffic
																              496,40$/month

For high outgoing data traffic, the app service is more favorable, in this example calc.

"Costs that accrue with Azure App Service
Depending on which feature you use in App Service, the following cost-accruing resources may be created:

App Service plan Required to host an App Service app.
Isolated tier A Virtual Network is required for an App Service environment.
Backup A Storage account is required to make backups.
Diagnostic logs You can select Storage account as the logging option, or integrate with Azure Log Analytics.
App Service certificates Certificates you purchase in Azure must be maintained in Azure Key Vault.
Other cost resources for App Service are (see App Service pricing for details):

App Service domains Your subscription is charged for the domain registration on a yearly basis, if you enable automatic renewal.
App Service certificates One-time charge at the time of purchase. If you have multiple subdomains to secure, you can reduce cost by purchasing one wildcard certificate instead of multiple standard certificates.
IP-based certificate bindings The binding is configured on a certificate at the app level.
Costs are accrued for each binding. For Standard tier and above, the first IP-based binding is not charged." 1

1 https://docs.microsoft.com/en-us/azure/app-service/overview-manage-costs


Costs: AppService is cheaper because there is no administration of a VM.
Scalability: Autoscalling is easier to implement than with a VM.
Availability: Higher availability because no patching of a VM, e.g.
Workflow: progressive/continuous rollout possible due to deployment slots

In the provided writeup.md file, detail how the app and any other needs would have to change for you to change your decision in the last section.

for a more complex application where the interaction between application and hardware usage would need to be looked at more closely,
i would prefer the initial deployment on a vm until the app is stable enough to be rolled out as an AppService.
