
In terms of cost, scalability, availability and workflow, deploying the app as a Microsoft AppService is preferable to deploying it on a virtual machine.

Costs: AppService is cheaper because there is no administration of a VM.
Scalability: Autoscalling is easier to implement than with a VM.
Availability: Higher availability because no patching of a VM, e.g.
Workflow: progressive/continuous rollout possible due to deployment slots

In the provided writeup.md file, detail how the app and any other needs would have to change for you to change your decision in the last section.

for a more complex application where the interaction between application and hardware usage would need to be looked at more closely,
i would prefer the initial deployment on a vm until the app is stable enough to be rolled out as an AppService.