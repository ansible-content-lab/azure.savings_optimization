# Opt In Scheduler Role

This Ansible role contains a repeatable way to schedule the starting and stopping of Azure VMs based on owner and environment tags

### Variables

The following variables are used during deployment and can be configured as extra vars at deploy time if you require something other than the defaults.

#### Required
```yaml
---
CONTROLLER_USERNAME: username to access automation controller
CONTROLLER_PASSWORD: password for automation controller users
CONTROLLER_HOST: full URL for accessing controller
owner: what owner inside Azure to filter by (using owner tag)
env: what environment inside Azure to filter by (using env tag)
```
