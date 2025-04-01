# terraform_for_each_vm

Change Log

## Changes

### 1. Password Management
- The password has been added to the `tfvars` file to centralize configuration and improve manageability.

### 2. Provider Configuration
- The `subscription_id` parameter has been included in the `provider.tf` file to ensure proper authentication and resource provisioning.

### 3. Module Structure
- The main Terraform (`.tf`) file has been moved inside the `modules` directory to improve modularity and maintainability of the infrastructure code.


## How to Run
To run this setup, follow these steps:
1. Add your own password in the `tfvars` file.
2. Add your Azure subscription ID in the `provider.tf` file.
3. You can check your Azure subscription ID using the command below:
   ```bash
   az account show
   ```
### 4. Virtual Machine Version Update
- The virtual machine version has been updated from **16** to **22** due to compatibility issues with Python in later deployment steps.
- Specifically, the SKU was changed from:

  ```hcl
  sku = "16.04-LTS"
  ```
  to:
  ```hcl
  sku = "22_04-lts-gen2"
  ```
  to ensure compatibility with the required dependencies.

## <b> Autora </b>

+ [Gloria Vanesa](https://github.com/Vanesa155 "Vanesa V.")

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)
