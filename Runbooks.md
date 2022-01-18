# Runbooks

Runbooks serve as repositories for your custom scripts and workflows.

They also typically reference Automation shared resources such as credentials, variables, connections, and certificates.

Runbooks can also contain other runbooks, allowing you to build more complex workflows.

You can invoke and run runbooks either on-demand or according to a schedule by using Automation Schedule assets.

## Graphical runbooks

Graphical runbooks and Graphical PowerShell Workflow runbooks are created and edited with the graphic editor in the Azure portal.

You can export them to a file and import them into another automation account, but you can't create or edit them with another tool.

## PowerShell runbooks

PowerShell runbooks are based on Windows PowerShell. You edit the runbook code directly, using the text editor in the Azure portal.

You can also use any offline text editor and then import the runbook into Azure Automation. PowerShell runbooks don't use parallel processing.

## PowerShell Workflow runbooks

PowerShell Workflow runbooks are text runbooks based on Windows PowerShell Workflow.

You directly edit the runbook code using the text editor in the Azure portal.

You can also use any offline text editor and import the runbook into Azure Automation.

PowerShell Workflow runbooks use parallel processing to allow for simultaneous completion of multiple tasks.

Workflow runbooks take longer to start than PowerShell runbooks because they must be compiled before running.

## Python Runbooks

Python runbooks compile under Python 2.

You can directly edit the code of the runbook using the text editor in the Azure portal, or you can use any offline text editor and import the runbook into Azure Automation.

You can also use Python libraries. However, only Python 2 is supported at this time.

To use third-party libraries, you must first import the package into the Automation Account.