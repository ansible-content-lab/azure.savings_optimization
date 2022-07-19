# Opt In Savings Role

This Ansible role contains repeatable way to Turn off or On Azure instances based on environment and owner tags in order to save cloud spend during off hours

### Variables

The following variables are used during deployment and can be configured as extra vars at deploy time if you require something other than the defaults.

#### Required

Microsoft Azure Resource Manager credential assigned to the job template

```yaml
---
# These variables can be configured to not perform tag savings actions and just get a report
owner: owner tag you want to use to filter VMs
env: environment tag you want to use to filter VMs
opt_in_savings_start: use true if you want to start VMs, false to turn off
```
