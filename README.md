# Ansible Collection - lab.azure_savings

This repository hosts the `lab.azure_savings` Ansible Collection.

The collection includes a variety of Ansible roles and playbook to help automate the savings on Azure Resources

This content was developed as part of the [Ansible Content Lab for Cloud Content](https://ansible-content-lab.github.io/), a program from the Ansible team to help incubate Ansible cloud use cases from ideation to collections and roles.

## Included Content

<!--start collection content-->
### Roles

Click on the role name to be directed to the README specifically for that role.

| Name                                                                                                                                                          | Description                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [azure_savings.tag_savings](https://github.com/ansible-content-lab/azure_savings/blob/main/roles/tag_savings/README.md)   | A role to turn off / destroy untagged or instances without an owner.|

### Playbooks

| Name                                    | Role(s) Used                           | Description                                                                                                                 |
|-----------------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `lab.aws_roles.tagsavings`     | `roles.tag_savings`  | A playbook to turn off / destroy untagged or instances without an owner.                                    |
<!--end collection content-->

```

## Installation and Usage

### Installing the Collection with the Ansible Galaxy CLI

Before using the this collection, you need to install it with the Ansible Galaxy CLI:

`ansible-galaxy collection install git+https://github.com/ansible-content-lab/lab.aws_roles.git`

You can also include it in a `requirements.yml` file and install it via `ansible-galaxy collection install -r requirements.yml`, using the format:

```yaml
---
collections:
  - name: https://github.com/ansible-content-lab/azure_savings.git
    type: git
    version: main
```


# License
GNU General Public License v3.0 or later

See [LICENCE](https://github.com/ansible-content-lab/lab.aws_roles/blob/main/LICENSE) to see the full text.
