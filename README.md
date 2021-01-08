# terraform-azure-key-vault

Terraform module to manage an `Azure Key Vault`.

![Terraform Version](https://img.shields.io/badge/Terraform-0.12.x-green.svg)

See `variables.tf` for more information about input values.

## Usage

```hcl
module "automation_account"
  source = "github.com/scalair/terraform-azure-key-vault"

  location              = "francecentral"
  resource_group_name   = "rg-project1-francecentral"
  name                  = "kv-sslauto-02"
  sku_name              = "standard"

  tenant_id       = "xxxx"

  soft_delete_retention_days  = 30

  tags = {
    environment = "dev"
    client      = "scalair"
    terraform   = "true"
  }
```
