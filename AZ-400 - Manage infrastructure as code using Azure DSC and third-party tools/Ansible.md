# Ansible

Ansible is an open-source platform by Red Hat that automates cloud provisioning, configuration management, and application deployments.

Using Ansible, you can provision VMs, containers, and your entire cloud infrastructure.

Also, Ansible enables you to automate the deployment and configuration of resources in your environment such as:

- Virtual networks.
= Storage.
- Subnets.
- Resources groups.
Ansible is designed for multiple-tier deployments.

Unlike Puppet or Chef, Ansible is agentless, meaning you don't have to install software on the managed machines.

Ansible also models your IT infrastructure by describing how all your systems interrelate, rather than managing just one system at a time.

## Ansible components

The core components of Ansible are:

- Control Machine. It's the machine from which the configurations are run. It can be any machine with Ansible installed on it. However, it requires that Python 2 or Python 3 be installed on the control machine as well. You can have multiple control nodes, laptops, shared desktops, and servers all running Ansible.
- Managed Nodes. The devices and machines (or just machines) and environments that are being managed. Managed nodes are sometimes referred to as hosts. Ansible isn't installed on nodes.
- Playbooks. Playbooks are ordered lists of tasks that have been saved so you can run them repeatedly in the same order. Playbooks are Ansible's language for configuration, deployment, and orchestration. They can describe a policy that you want your remote systems to enforce, or they can dictate a set of steps in a general IT process. When you create a playbook, you do so by using YAML, which defines a model of a configuration or process, and uses a declarative model. Elements such as name, hosts, and tasks stays within playbooks.
- Modules. Ansible works by connecting to your nodes and then pushing small programs (or units of code)—called modules—out to the nodes. Modules are the units of code that define the configuration. They're modular and can be reused across playbooks. They represent the system's desired state (declarative), are executed over SSH by default, and are removed when finished. A playbook is typically made up of many modules. For example, you could have one playbook containing three modules: a module for creating an Azure Resource Group, a module for creating a virtual network, and a module for adding a subnet. Your library of modules can be on any machine and doesn't require any servers, daemons, or databases. Typically, you'll work with your favorite terminal program, a text editor, and most likely a version control system to track changes to your content. You can preview Ansible Azure modules on the Ansible Azure preview modules webpage.
- Inventory. An inventory is a list of managed nodes. Ansible represents what machines it manages to use a .INI file that puts all your managed machines in your chosen groups. You don't need to use more SSL-signing servers when adding new machines, avoiding Network Time Protocol (NTP) and Domain Name System (DNS) issues. You can create the inventory manually, or for Azure, Ansible supports dynamic inventories> It means that the host inventory is dynamically generated at runtime. Ansible supports host inventories for other managed hosts as well.
- Roles. Roles are predefined file structures that allow automatic loading of certain variables, files, tasks, and handlers based on the file's structure. It allows for easier sharing of roles. You might, for example, create roles for a web server deployment.
- Facts. Facts are data points about the remote system that Ansible is managing. When a playbook is run against a machine, Ansible will gather facts about the state of the environment to determine the state before executing the playbook.
- Plug-ins. Plug-ins are code that supplements Ansible's core functionality.


The order of items (variables and resources) defined within the configuration file doesn't matter because Terraform configurations are declarative.

- Terraform CLI. It's a command-line interface from which you run configurations. You can command such as Terraform apply and Terraform plan, along with many others. A CLI configuration file that configures per-user settings for the CLI is also available. However, this is separate from the CLI infrastructure configuration. In Windows operating system environments, the configuration file is named terraform.rc and is stored in the relevant user's %APPDATA% directory. On Linux systems, the file is named .terraformrc (note the leading period) and is stored in the home directory of the relevant user.

- Modules. Modules are self-contained packages of Terraform configurations that are managed as a group. You use modules to create reusable components in Terraform and for basic code organization. A list of available modules for Azure is available on the Terraform Registry Modules webpage.

- Provider. The provider is responsible for understanding API interactions and exposing resources.

- Overrides. Overrides are a way to create configuration files that are loaded last and merged into (rather than appended to) your configuration. You can create overrides to modify Terraform behavior without having to edit the Terraform configuration. They can also be used as temporary modifications that you can make to Terraform configurations without changing the configuration itself.

- Resources. Resources are sections of a configuration file that define components of your infrastructure, such as VMs, network resources, containers, dependencies, or DNS records. The resource block creates a resource of the given TYPE (first parameter) and NAME (second parameter). However, the combination of the type and name must be unique. The resource's configuration is then defined and contained within braces.

- Execution plan. You can issue a command in the Terraform CLI to generate an execution plan. The execution plan shows what Terraform will do when a configuration is applied. It enables you to verify changes and potential flag issues. The command for the execution plan is Terraform plan.

- Resource graph. Using a resource graph, you can build a dependency graph of all resources. You can then create and modify resources in parallel. It helps provision and configures resources more efficiently.