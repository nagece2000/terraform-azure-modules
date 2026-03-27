# Terraform Azure Modules

Reusable Terraform modules for Azure infrastructure.

## Modules

### Network Module
Creates an Azure Virtual Network with configurable address space.

**Usage:**
```hcl
module "network" {
  source = "git::https://github.com/nagece2000/terraform-azure-modules.git//modules/network?ref=v1.0.0"
  
  vnet_name           = "my-vnet"
  resource_group_name = "my-rg"
  location            = "australiasoutheast"
  address_space       = ["10.0.0.0/16"]
}
```

### Storage Module
Creates an Azure Storage Account with configurable replication.

**Usage:**
```hcl
module "storage" {
  source = "git::https://github.com/nagece2000/terraform-azure-modules.git//modules/storage?ref=v1.0.0"
  
  storage_account_name = "mystorageacct"
  resource_group_name  = "my-rg"
  location             = "australiasoutheast"
}
```

## Versions

- `v1.0.0` - Initial release with network and storage modules