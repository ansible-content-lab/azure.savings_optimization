# Ansible Collection - azure_savings

This repository hosts the `azure_savings` Ansible Collection.

The collection includes a variety of Ansible roles and playbook to help automate the savings on Azure Resources

This content was developed as part of the [Ansible Content Lab for Cloud Content](https://ansible-content-lab.github.io/), a program from the Ansible team to help incubate Ansible cloud use cases from ideation to collections and roles.

## Included Content

<!--start collection content-->
### Roles

Click on the role name to be directed to the README specifically for that role.

| Name                                                                                                                                                          | Description                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [azure_savings.tag_savings](https://github.com/ansible-content-lab/azure_savings/blob/main/roles/tag_savings/README.md)   | A role to turn off / destroy untagged or instances without an owner.|
| [azure_savings.opt_in_savings](https://github.com/ansible-content-lab/azure_savings/blob/main/roles/opt_in_savings/README.md)   | A role to turn off / turn on Azure instances based on owner and environment tags.|
| [azure_savings.opt_in_scheduler](https://github.com/ansible-content-lab/azure_savings/blob/main/roles/opt_in_scheduler/README.md)   | A role to create the schedule in controller to turn off / turn on Azure instances based on owner and environment tags.|

### Playbooks

| Name                                    | Role(s) Used                           | Description                                                                                                                 |
|-----------------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `azure_savings.tagsavings`     | `roles.tag_savings`  | A playbook to turn off / destroy untagged or instances without an owner.                                    |
| `azure_savings.azure_opt_in_savings`     | `roles.opt_in_savings`  | A playbook to turn off / turn on Azure instances based on owner and environment tags                                    |
| `azure_savings.azure_opt_in_savings_scheduler`     | `roles.opt_in_scheduler`  | A playbook to create a schedule in controller to turn off / turn on Azure instances based on owner and environment tags                                    |
<!--end collection content-->

```

## Installation and Usage

### Installing the Collection with the Ansible Galaxy CLI

Before using the this collection, you need to install it with the Ansible Galaxy CLI:

`ansible-galaxy collection install git+https://github.com/ansible-content-lab/azure_savings.git`

You can also include it in a `requirements.yml` file and install it via `ansible-galaxy collection install -r requirements.yml`, using the format:

```yaml
---
collections:
  - name: https://github.com/ansible-content-lab/azure_savings.git
    type: git
    version: main
```

# Content Setup

This repo includes an Ansible Automation Platform (AAP) playbook to quickly poplulate an instance of AAP with some content to be used in an Azure Cloud environment.


**Instructions**

- Add the Azure credentials to your AAP instance and give it the following name: **'Microsoft Azure Resource Manager'**
-- The credential type is also called **'Microsoft Azure Resource Manager'**
-- You will need to provied the **Subscription ID, Tenant ID, Client ID (App ID), and Client Secret (App Secret)**

- Add the Ansible Automation Platform credentials to your AAP instance and give it the following name: **'This AAPs Credentials'**
  - The credential type is called **'Red Hat Ansible Automation Platform'**
  - The credential type is called **'Red Hat Ansible Automation Platform'**
  - You will need to provied the **admin** user and password, or the **OAuth token**

- Create a project and name it **'Azure Demos Project'**
  - For the **Source Control Credential Type** select **Git** from the dropdown
  - For the **Source Control URL** enter the following:  https://github.com/ansible-content-lab/lab.azure_savings.git

- Create a Template (Add Job Template) and name it **'setup template'**
  - For the **Inventory** select **Demo Inventory**
  - For the **Project** select **Azure Demos Project**
  - For the **Playbook** select **playbooks/azuresetup.yml**
  - For the **Credentials** select **This AAPs Credentials**
  - Save and launch this template.  Once complete you will find a number templates you can leverage.

Please customize any Job Template **extra vars** as needed for your environmnet.

Enjoy this sample content.


# License
GNU General Public License v3.0 or later

See [LICENCE](https://github.com/ansible-content-lab/lab.aws_roles/blob/main/LICENSE) to see the full text.
