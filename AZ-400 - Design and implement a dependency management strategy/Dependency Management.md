# What is dependency management?

## Dependencies in software

Modern software development involves complex projects and solutions.

Projects have dependencies on other projects, and solutions aren't single pieces of software.

The solutions and software built consist of multiple parts and components and are often reused.

As codebases are expanding and evolving, it needs to be componentized to be maintainable.

A team that is writing software won't write every piece of code by itself but use existing code written by other teams or companies and open-source code that is readily available.

Each component can have its maintainers, speed of change, and distribution, giving both the creators and consumers of the components autonomy.

A software engineer will need to identify the components that make up parts of the solution and decide whether to write the implementation or include an existing component.

The latter approach introduces a dependency on other components.

## Why is dependency management needed?

Software dependencies that are introduced in a project and solution must be appropriately declared and resolved.

You need to manage the overall composition of the project code and the included dependencies.

Without proper dependency management, it will be hard to keep the components in the solution controlled.

Management of dependencies allows a software engineer and team to be more efficient working with dependencies.

With all dependencies being managed, it's also possible to control the consumed dependencies, enabling governance and security scanning to use known vulnerabilities or exploits packages.

## Describe elements of a dependency management strategy

There are many aspects of a dependency management strategy.

- Standardization Managing dependencies benefit from a standardized way of declaring and resolving them in your codebase.
Standardization allows a repeatable, predictable process and usage that can be automated as well.

- Package formats and sources The distribution of dependencies can be performed by a packaging method suited for your solution's dependency type.
Each dependency is packaged using its usable format and stored in a centralized source.
Your dependency management strategy should include the selection of package formats and corresponding sources where to store and retrieve packages.

- Versioning Just like your own code and components, the dependencies in your solution usually evolve.
While your codebase grows and changes, you need to consider the changes in your dependencies as well.
It requires a versioning mechanism for the dependencies to be selective of the version of a dependency you want to use.

## Understand source and package componentization

Current development practices already have the notion of componentization.

There are two ways of componentization commonly used.

1. Source componentization The first way of componentization is focused on source code. It refers to splitting the source code in the codebase into separate parts and organizing it around the identified components.
It works if the source code isn't shared outside of the project. Once the components need to be shared, it requires distributing the source code or the produced binary artifacts created from it.

2. Package componentization The second way uses packages. Distributing software components is performed utilizing packages as a formal way of wrapping and handling the components.
A shift to packages adds characteristics needed for proper dependency management, like tracking and versioning packages in your solution.