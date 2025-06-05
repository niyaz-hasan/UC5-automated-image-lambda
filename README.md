# UC5-automated-image-lambda .
trigger  the lambda any upload happen in s3 

<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.6.0 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 5.31 |

## Providers

No providers.

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_lambda_function"></a> [lambda\_function](#module\_lambda\_function) | ./modules/lambda | n/a |
| <a name="module_s3_buckets"></a> [s3\_buckets](#module\_s3\_buckets) | ./modules/s3 | n/a |
| <a name="module_sns_topic"></a> [sns\_topic](#module\_sns\_topic) | ./modules/sns | n/a |

## Resources

No resources.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_aws_region"></a> [aws\_region](#input\_aws\_region) | AWS region | `string` | `"us-east-1"` | no |
| <a name="input_destination_bucket_name"></a> [destination\_bucket\_name](#input\_destination\_bucket\_name) | Name of the destination S3 bucket | `string` | `"image-sized-1"` | no |
| <a name="input_lambda_function_name"></a> [lambda\_function\_name](#input\_lambda\_function\_name) | Name of the Lambda function | `string` | `"image-resizer-function"` | no |
| <a name="input_notification_email"></a> [notification\_email](#input\_notification\_email) | Notification email for SNS topic | `string` | `"niyaz.hasanmohamed@hcltech.com"` | no |
| <a name="input_sns_topic_name"></a> [sns\_topic\_name](#input\_sns\_topic\_name) | Name of the SNS topic | `string` | `"image-resizing-topic"` | no |
| <a name="input_source_bucket_name"></a> [source\_bucket\_name](#input\_source\_bucket\_name) | Name of the source S3 bucket | `string` | `"image-non-sized-1"` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_destination_bucket_name"></a> [destination\_bucket\_name](#output\_destination\_bucket\_name) | n/a |
| <a name="output_lambda_function_name"></a> [lambda\_function\_name](#output\_lambda\_function\_name) | n/a |
| <a name="output_sns_topic_arn"></a> [sns\_topic\_arn](#output\_sns\_topic\_arn) | n/a |
| <a name="output_source_bucket_name"></a> [source\_bucket\_name](#output\_source\_bucket\_name) | n/a |
<!-- END_TF_DOCS -->