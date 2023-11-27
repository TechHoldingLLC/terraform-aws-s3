## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_cloudfront_origin_access_control.cloudfront](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/cloudfront_origin_access_control) | resource |
| [aws_cloudfront_origin_access_identity.cloudfront](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/cloudfront_origin_access_identity) | resource |
| [aws_s3_bucket.s3](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket) | resource |
| [aws_s3_bucket_acl.acl](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket_acl) | resource |
| [aws_s3_bucket_policy.allow_public_read_access_to_objects](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket_policy) | resource |
| [aws_s3_bucket_policy.s3_cloudfront](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket_policy) | resource |
| [aws_s3_bucket_server_side_encryption_configuration.encryption](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket_server_side_encryption_configuration) | resource |
| [aws_s3_bucket_versioning.versioning](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket_versioning) | resource |
| [aws_s3_bucket_website_configuration.website](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket_website_configuration) | resource |
| [aws_iam_policy_document.allow_public_read_access_to_objects](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/iam_policy_document) | data source |
| [aws_iam_policy_document.s3_cloudfront](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/iam_policy_document) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_acl"></a> [acl](#input\_acl) | Bucket ACL | `string` | `"private"` | no |
| <a name="input_bucket_public_read_access"></a> [bucket\_public\_read\_access](#input\_bucket\_public\_read\_access) | Allow public read to objects when website enabled | `bool` | `false` | no |
| <a name="input_bucket_public_read_access_condition"></a> [bucket\_public\_read\_access\_condition](#input\_bucket\_public\_read\_access\_condition) | Allow public read to objects with condition when website enabled | `map(any)` | `{}` | no |
| <a name="input_origin_access_identity"></a> [origin\_access\_identity](#input\_origin\_access\_identity) | Configure cloudfront origin access identity | `bool` | `false` | no |
| <a name="input_origin_access_control"></a> [origin\_access\_control](#input\_origin\_access\_control) | Configure cloudfront origin access control | `bool` | `false` | no |
| <a name="input_force_destroy"></a> [force\_destroy](#input\_force\_destroy) | Force bucket destroy | `string` | `false` | no |
| <a name="input_name"></a> [name](#input\_name) | S3 bucket name | `string` | n/a | yes |
| <a name="input_versioning"></a> [versioning](#input\_versioning) | Set bucket versioninig | `string` | `"Disabled"` | no |
| <a name="input_encryption_algorithm"></a> [encryption_algorithm](#input\_encryption\_algorithm) | Set bucket encryption algorithm | `string` | `"AES256"` | no |
| <a name="input_kms_master_key_id"></a> [kms_master_key_id](#input\_kms\_master\_key\_id) | Master key id for bucket encryption, only used with aws:kms/aws:kms:dsse | `string` | `null` | no |
| <a name="input_website"></a> [website](#input\_website) | Configure bucket to host static website | `any` | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_bucket_arn"></a> [bucket\_arn](#output\_bucket\_arn) | n/a |
| <a name="output_bucket_name"></a> [bucket\_name](#output\_bucket\_name) | n/a |
| <a name="output_bucket_regional_domain_name"></a> [bucket\_regional\_domain\_name](#output\_bucket\_regional\_domain\_name) | n/a |
| <a name="output_bucket_website_endpoint"></a> [bucket\_website\_endpoint](#output\_bucket\_website\_endpoint) | n/a |
| <a name="output_origin_access_identity_path"></a> [origin\_access\_identity\_path](#output\_origin\_access\_identity\_path) | n/a |
| <a name="output_origin_access_control_id"></a> [origin\_access\_control\_id](#output\_origin\_access\_control\_id) | n/a |

## License

Apache 2 Licensed. See [LICENSE](https://github.com/TechHoldingLLC/terraform-aws-s3-bucket/blob/main/LICENSE) for full details.