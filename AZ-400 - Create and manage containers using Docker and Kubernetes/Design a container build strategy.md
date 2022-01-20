# Containers

Kubernetes is a cluster orchestration technology that originated with Google. The Cloud-Native Computing Foundation currently owns it, and it's open source.

Kubernetes is often referred to a k8s. It's a platform for automating deployment, scaling, and operations of application containers across clusters of hosts.

It creates a container-centric infrastructure.

There are several other container cluster orchestration technologies available such as Mesosphere DC/OS and Docker Swarm. Today though, all the industry interest appears to be in Kubernetes.

Containers are a solution to the problem of how to get the software to run reliably when moved from one computing environment to another.

## AKS
AKS is Microsoft's implementation of Kubernetes. AKS makes it easier to deploy a managed Kubernetes cluster in Azure.

It also reduces the complexity and operational overhead of Kubernetes by offloading much of that responsibility to Azure.

AKS manages much of the Kubernetes resources for the end user.

They do it making it quicker and easier to deploy and manage containerized applications without container orchestration expertise.

It also eliminates ongoing operations and maintenance burden by provisioning. And upgrading and scaling resources on demand without taking applications offline.

Azure AKS manages the following aspects of a Kubernetes cluster for you:

- It manages critical tasks, such as health monitoring and maintenance, Kubernetes version upgrades, and patching.
- It performs simple cluster scaling.
- It enables master nodes to be fully managed by Microsoft.
- It leaves you responsible only for managing and maintaining the agent nodes.
- It ensures master nodes are free, and you only pay for running agent nodes.

## AKS Architectural components

![img](https://docs.microsoft.com/en-us/learn/wwl-azure/implement-azure-kubernetes-service/media/aks-components-5fbc204a.png)

**Cluster Master**

When you create an AKS cluster, a cluster master is automatically created and configured.

This cluster master is provided as a managed Azure resource abstracted from the user.

There's no cost for the cluster master, only the nodes part of the AKS cluster.

The cluster master includes the following core Kubernetes components:

