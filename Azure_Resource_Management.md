# Azure Resource Management

## Deployment modes

When deploying your resources using templates, you have three options:

- validate. This option compiles the templates, validates the deployment, ensures the template is functional (for example, no circular dependencies), and correct syntax.

- incremental mode (default). This option only deploys whatever is defined in the template. It doesn't remove or modify any resources that aren't defined in the template. For example, if you've deployed a VM via template and then renamed the VM in the template, the first VM deployed will remain after the template is rerun. It's the default mode.

- complete mode: Resource Manager deletes resources in the resource group but isn't specified in the template. For example, only resources defined in the template will be present in the resource group after the template deploys. As a best practice, use this mode for production environments where possible to try to achieve idempotency in your deployment templates.