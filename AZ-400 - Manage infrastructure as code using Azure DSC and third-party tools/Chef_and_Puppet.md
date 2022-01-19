# Chef and Puppet

Configuration management tools enable changes and deployments to be faster, repeatable, scalable, predictable, and able to maintain the desired state, bringing controlled assets into an expected state.

Some advantages of using configuration management tools include:

- Adherence to coding conventions that make it easier to navigate code.
- Idempotency, which means that the end state remains the same, no matter how many times the code is executed.
- Distribution design to improve managing large numbers of remote servers.
Some configuration management tools use a pull model.

An agent installed on the servers runs periodically to pull the latest definitions from a central repository and apply them to the server.

Other tools use a push model, where a central server triggers updates to managed servers.

Configuration management tools enable the use of tested and proven software development practices to manage and provision data centers in real-time through plaintext definition files.

This module introduces Chef and Puppet, the third party of tools for environment automation.

## Chef Infra

Chef Infra is an infrastructure automation tool that you use to deploy, configure, manage, and ensure application and infrastructure compliance.

It provides for a consistent deployment and management experience.

Chef Infra helps you manage your infrastructure in the cloud, on-premises, or a hybrid environment by using instructions (or recipes) to configure nodes.

A node or chef-client is any physical or virtual machine (VM), cloud, or network device under management by Chef Infra.

Chef Infra has three main architectural components:

- Chef Server This is the management point. There are two options for the Chef Server: a hosted solution and an on-premises solution.
- Chef Client (node) It's a Chef agent that is on the servers you're managing.
- Chef Workstation This is the Admin workstation where you create policies and execute management commands. You run the knife command from the Chef Workstation to manage your infrastructure.


### Puppet
Puppet is a deployment and configuration management toolset that provides you with enterprise tools that you need to automate an entire lifecycle on your Azure infrastructure. It **also** provides consistency and transparency into infrastructure changes.

Puppet provides a series of open-source configuration management tools and projects. It also provides Puppet Enterprise, a configuration management platform that allows you to maintain state in both your infrastructure and application deployments.


Puppet operates using a client-server model and consists of the following core components:

- Puppet Master. The Puppet Master is responsible for compiling code to create agent catalogs. It's also where Secure Sockets Layer (SSL) certificates are verified and signed. Puppet Enterprise infrastructure components are installed on a single node, the master. The master always contains a compile master and a Puppet Server. As your installation grows, you can add extra compile masters to distribute the catalog compilation workload.
- Puppet Agent. Puppet Agent is the machine (or machines) managed by the Puppet Master. An agent that is installed on those managed machines allows them to be managed by the Puppet Agent.
- Console Services. Console Services is the web-based user interface for managing your systems.
- Facts. Facts are metadata related to the state. Puppet will query a node and determine a series of facts, which it then uses to determine the state.