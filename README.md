# Azure Resource Group Terraform Module

This Terraform module creates an Azure Resource Group.

## Usage

```hcl
module "resource_group" {
  source              = "github.com/your-username/azure-resource-group"
  resource_group_name = "my-resource-group"
  location            = "eastus"
  tags = {
    environment = "production"
    project     = "my-project"
  }
}

