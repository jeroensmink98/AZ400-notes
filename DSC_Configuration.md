# Desired State Configuration

## Configuration Drift

Configuration drift is the process of a set of resources changing over time from their original deployment state.

It can be because of changes made manually by people or automatically by processes or programs.

Eventually, an environment can become a snowflake. A snowflake is a unique configuration that cannot be reproduced automatically and is typically a result of configuration drift.

With snowflakes, infrastructure administration and maintenance invariably involve manual processes, which can be hard to track and prone to human error.

The more an environment drifts from its original state, the more likely it is for an application to find issues.

The greater the degree of configuration drift, the longer it takes to troubleshoot and rectify issues.

![img](https://docs.microsoft.com/en-us/learn/wwl-azure/implement-desired-state-configuration-dsc/media/configuration-drift-44f43cbe.png)

## Security considerations

Configuration drift can also introduce security vulnerabilities into your environment. For example:

Ports might be opened that should be kept closed.
Updates and security patches might not be applied across environments consistently.
The software might be installed that doesn't meet compliance requirements.

## Solutions for managing configuration drift

While eliminating configuration drift can be difficult, there are many ways you can manage it in your environments using configuration management tools and products such as:

- Windows PowerShell Desired State Configuration. It's a management platform in PowerShell that enables you to manage and enforce resource configurations. For more information about Windows PowerShell Desired State Configuration, go to Windows PowerShell Desired State Configuration Overview.
- Azure Policy. Use Azure Policy to enforce policies and compliance standards for Azure resources. For more information about Azure Policy, go to Azure Policy.
There are also other third-party solutions that you can integrate with Azure.

## Explore Desired State Configuration (DSC)

Desired State Configuration (DSC) is a configuration management approach that you can use for configuration, deployment, and management of systems to ensure that an environment is maintained in a state that you specify (defined state) and doesn't deviate from that state.

DSC helps eliminate configuration drift and ensures the state is maintained for compliance, security, and performance.

Windows PowerShell DSC is a management platform in PowerShell that provides desired State.

PowerShell DSC lets you manage, deploy, and enforce configurations for physical or virtual machines, including Windows and Linux.

### DSC Components

- Configurations. These are declarative PowerShell scripts that define and configure instances of resources. Upon running the configuration, DSC (and the resources being called by the configuration) will apply the configuration, ensuring that the system exists in the state laid out by the configuration. DSC configurations are also idempotent: The Local Configuration Manager (LCM) will ensure that machines are configured in whatever state the configuration declares.
- Resources. They contain the code that puts and keeps the target of a configuration in the specified state. Resources are in PowerShell modules and can be written to a model as generic as a file or a Windows process or as specific as a Microsoft Internet Information Services (IIS) server or a VM running in Azure.
- Local Configuration Manager (LCM). The LCM runs on the nodes or machines you wish to configure. It's the engine by which DSC facilitates the interaction between resources and configurations. The LCM regularly polls the system using the control flow implemented by resources to maintain the state defined by a configuration. If the system is out of state, the LCM calls the code in resources to apply the configuration according to specified.

There are two methods of implementing DSC:

- Push mode - A user actively applies a configuration to a target node and pushes out the configuration.
- Pull mode is where pull clients are automatically configured to get their desired state configurations from a remote pull service. This remote pull service is provided by a pull server that acts as central control and manager for the configurations, ensures that nodes conform to the desired state, and reports on their compliance status. The pull server can be set up as an SMB-based pull server or an HTTPS-based server. HTTPS-based pull-server uses the Open Data Protocol (OData) with the OData Web service to communicate using REST APIs. It's the model we're most interested in, as it can be centrally managed and controlled. The following diagram provides an outline of the workflow of DSC pull mode.

![img](https://docs.microsoft.com/en-us/learn/wwl-azure/implement-desired-state-configuration-dsc/media/dsc2-6e218006.png)

## Why use Azure Automation DSC

The following outlines some of the reasons why we would consider using Azure Automation DSC:

- Built-in pull server. Provides a DSC pull server like the Windows Feature DSC service so that target nodes automatically receive configurations, conform to the desired state, and report back on their compliance. The built-in pull server in Azure Automation eliminates the need to set up and maintain your pull server.
- Management of all your DSC artifacts. You can manage all your DSC configurations, resources, and target nodes from the Azure portal or PowerShell.
- Import reporting data into Log Analytics. Nodes managed with Azure Automation state configuration send detailed reporting status data to the built-in pull server. You can configure Azure Automation state configuration to send this data to your Log Analytics workspace.