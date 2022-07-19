# Tag Savings Role

This Ansible role contains repeatable way to destroy untagged instances or turn-off instances without an owner tag

### Variables

The following variables are used during deployment and can be configured as extra vars at deploy time if you require something other than the defaults.

#### Required

Microsoft Azure Resource Manager credential assigned to the job template

#### Optional

```yaml
---
# These variables can be configured to not perform tag savings actions and just get a report
owner: owner tag you want to use to filter VMs
env: environment tag you want to use to filter VMs
opt_in_savings_start: use true if you want to start VMs, false to turn off
```
