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
azure_savings_perform_savings: true
```
