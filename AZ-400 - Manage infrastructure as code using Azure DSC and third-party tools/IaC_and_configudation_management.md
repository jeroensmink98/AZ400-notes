# IaC and Configuration Management

infrastructure as code is the concept of managing your operations environment like you do applications or other code for general release.

## Configuration Management

**Configuration management** refers to automated configuration management, typically in version-controlled scripts, for an application and all the environments needed to support it.

Two main approaches

**Declarative (functional)**. The declarative approach states what the final state should be. When run, the script or definition will initialize or configure the machine to have the finished state declared without defining how that final state should be achieved.

![img](https://docs.microsoft.com/en-us/learn/wwl-azure/explore-infrastructure-code-configuration-management/media/declarative-703bb981.png)

**Imperative (procedural)**. In the imperative approach, the script states the how for the final state of the machine by executing the steps to get to the finished state. It defines what the final state needs to be but also includes how to achieve that final state. It also can consist of coding concepts such as for, *if-then, loops, and matrices.
![img](https://docs.microsoft.com/en-us/learn/wwl-azure/explore-infrastructure-code-configuration-management/media/imperative-a9e6a2ad.png)

## Best practices

The declarative approach abstracts away the methodology of how a state is achieved. As such, it can be easier to read and understand what is being done.

It also makes it easier to write and define. Declarative approaches also separate the final desired state and the coding required to achieve that state.

So, it doesn't force you to use a particular approach, allowing for optimization.

A declarative approach would generally be the preferred option where ease of use is the primary goal. Azure Resource Manager template files are an example of a declarative automation approach.

An imperative approach may have some advantages in complex scenarios where changes in the environment occur relatively frequently, which need to be accounted for in your code.

There's no absolute on which is the best approach to take, and individual tools may be used in either declarative or imperative forms. The best approach for you to take will depend on your needs.

## Idempotent configuration

Idempotence is a mathematical term that can be used in Infrastructure as Code and Configuration as Code. It can apply one or more operations against a resource, resulting in the same outcome.

For example, running a script on a system should have the same outcome despite the number of times you execute the script. It shouldn't error out or do the same actions irrespective of the environment's starting state.

In essence, if you apply a deployment to a set of resources 1,000 times, you should end up with the same result after each application of the script or template.