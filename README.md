## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | n/a |
| <a name="provider_vault"></a> [vault](#provider\_vault) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_db_instance.postgresql](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/db_instance) | resource |
| [aws_security_group.postgresql](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/security_group) | resource |
| [vault_database_secret_backend_connection.postgres](https://registry.terraform.io/providers/hashicorp/vault/latest/docs/resources/database_secret_backend_connection) | resource |
| [vault_database_secret_backend_role.role](https://registry.terraform.io/providers/hashicorp/vault/latest/docs/resources/database_secret_backend_role) | resource |
| [vault_mount.db](https://registry.terraform.io/providers/hashicorp/vault/latest/docs/resources/mount) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_allocated_storage"></a> [allocated\_storage](#input\_allocated\_storage) | The amount of storage to allocate for the DB instance. | `number` | `5` | no |
| <a name="input_budget"></a> [budget](#input\_budget) | Team responsible for the resource | `string` | n/a | yes |
| <a name="input_db_subnet_group_name"></a> [db\_subnet\_group\_name](#input\_db\_subnet\_group\_name) | The name of the DB subnet group to use. | `string` | n/a | yes |
| <a name="input_engine"></a> [engine](#input\_engine) | The engine to use for the DB instance. | `string` | `"postgres"` | no |
| <a name="input_entities"></a> [entities](#input\_entities) | A set of vault clients to create | `list` | <pre>[<br>  "user",<br>  "application"<br>]</pre> | no |
| <a name="input_env"></a> [env](#input\_env) | The environment to deploy to | `string` | n/a | yes |
| <a name="input_hipaa"></a> [hipaa](#input\_hipaa) | HIPAA compliance | `bool` | n/a | yes |
| <a name="input_hvn_cidr_block"></a> [hvn\_cidr\_block](#input\_hvn\_cidr\_block) | The CIDR block to use for the HVN network. | `string` | n/a | yes |
| <a name="input_instance_class"></a> [instance\_class](#input\_instance\_class) | The instance type to use for the DB instance. | `string` | `"db.t3.small"` | no |
| <a name="input_master_password"></a> [master\_password](#input\_master\_password) | The master password for the DB instance. | `string` | n/a | yes |
| <a name="input_master_username"></a> [master\_username](#input\_master\_username) | The master username for the DB instance. | `string` | n/a | yes |
| <a name="input_owner"></a> [owner](#input\_owner) | Owner of the resource | `string` | n/a | yes |
| <a name="input_pii"></a> [pii](#input\_pii) | PII compliance | `bool` | n/a | yes |
| <a name="input_postgres_ttl"></a> [postgres\_ttl](#input\_postgres\_ttl) | Hours before the resource expires. *Use -1 for indefinite.* | `number` | `60` | no |
| <a name="input_private_subnets_cidr_blocks"></a> [private\_subnets\_cidr\_blocks](#input\_private\_subnets\_cidr\_blocks) | The private subnets CIDR blocks to use. | `list(string)` | n/a | yes |
| <a name="input_public_subnets_cidr_blocks"></a> [public\_subnets\_cidr\_blocks](#input\_public\_subnets\_cidr\_blocks) | The public subnets CIDR blocks to use. | `list(string)` | n/a | yes |
| <a name="input_service"></a> [service](#input\_service) | Service offering | `string` | n/a | yes |
| <a name="input_ttl"></a> [ttl](#input\_ttl) | Hours before the resource expires. *Use -1 for indefinite.* | `string` | n/a | yes |
| <a name="input_vpc_id"></a> [vpc\_id](#input\_vpc\_id) | The VPC to deploy to | `string` | n/a | yes |

## Outputs

No outputs.
