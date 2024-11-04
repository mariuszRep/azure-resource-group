## File Structure

azure-resource-group/
├── main.tf
├── variables.tf.json
├── outputs.tf.json
├── versions.tf
└── README.md

This module uses a mix of HCL (.tf) and JSON (.tf.json) files:

- `main.tf`: Contains the main resource configuration in HCL format.
- `variables.tf.json`: Defines input variables in JSON format.
- `outputs.tf.json`: Specifies outputs in JSON format.

## Usage

When using this module, refer to the variables as usual in your Terraform configurations. The JSON format of the variables and outputs files doesn't change how you use the module. For example:

```hcl
module "resource_group" {
  source              = "github.com/mariuszRep/azure-resource-group"
  resource_group_name = "my-resource-group"
  location            = "eastus"
  tags = {
    environment = "production"
    project     = "my-project"
  }
}
```

