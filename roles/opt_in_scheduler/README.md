# Opt In Scheduler Role

This Ansible role contains a repeatable way to schedule the starting and stopping of Azure VMs based on owner and environment tags

### Variables

The following variables are used during deployment and can be configured as a custom credential, extra vars, or passed via a survey

#### Required
```yaml
---
CONTROLLER_USERNAME: username to access automation controller
CONTROLLER_PASSWORD: password for automation controller users
CONTROLLER_HOST: full URL for accessing controller
owner: what owner inside Azure to filter by (using owner tag)
env: what environment inside Azure to filter by (using env tag)
stop_date_time: stop date time in format YYYY-MM-DD HH:MM:SS written in GMT
start_date_time: start date time in format YYYY-MM-DD HH:MM:SS written in GMT
repetition: how frequently to repeat
frequency: minute, hour, day, week, month
```
