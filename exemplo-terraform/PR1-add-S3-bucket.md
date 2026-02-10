### Descrição
Adding S3 bucket for logs

```hcl
resource "aws_s3_bucket" "app_logs" {
  bucket = "myapp-logs-prod"
}
