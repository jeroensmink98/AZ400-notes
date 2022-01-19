# Terraform

HashiCorp Terraform is an open-source tool that allows you to provision, manage, and version cloud infrastructure. It codifies infrastructure in configuration files that describes the topology of cloud resources such as VMs, storage accounts, and networking interfaces.

Terraform's command-line interface (CLI) provides a simple mechanism to deploy and version the configuration files to Azure or any other supported cloud service.

The CLI also allows you to validate and preview infrastructure changes before you deploy them.

Terraform also supports multi-cloud scenarios. It means developers can use the same tools and configuration files to manage infrastructure on multiple cloud providers.

You can run Terraform interactively from the CLI with individual commands. Or non-interactively as part of a continuous integration pipeline.

There's also an enterprise version of Terraform available, Terraform Enterprise.

## Terraform components

- Configuration files. Text-based configuration files allow you to define infrastructure and application configuration. These files end in the .tf or .tf.JSON extension. The files can be in either of the following two formats:

    - Terraform. The Terraform format is more accessible for users to review, in that way making it more user-friendly. It supports comments and is the recommended format for most Terraform files. Terraform files end in .tf
    - JSON. Machines mainly use the JSON format for creating, modifying, and updating configurations. However, it can also be used by Terraform operators if you prefer. JSON files end in .tf.JSON.