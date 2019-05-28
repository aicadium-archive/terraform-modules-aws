# Terraform KMS

This is a small utility module that provisions a KMS Key for Terraform use and creates
a policy to allow IAM administration of all keys on the AWS account.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| all\_keys\_admin\_policy | Name of policy to allow administration of all keys | string | `"AllKeysAdministration"` | no |
| kms\_terraform\_alias | Alias for the Terraform key | string | `"alias/terraform"` | no |
| tags | Tags for resoruces | map | `<map>` | no |

## Outputs

| Name | Description |
|------|-------------|
| all\_keys\_policy | Name of the All Keys policy |
| all\_keys\_policy\_arn | ARN of the All Keys policy |
| terraform\_key\_alias | Key alias for the KMS key used for Terraform operations |
| terraform\_key\_id | Key alias for the KMS key used for Terraform operations |
