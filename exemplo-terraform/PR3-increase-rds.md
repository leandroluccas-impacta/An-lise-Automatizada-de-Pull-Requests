
---

## 📄 PR3-increase-rds.md

```markdown
### Descrição
Scale RDS

```hcl
resource "aws_rds_instance" "db" {
  instance_class = "db.r6g.8xlarge"
  allocated_storage = 1000
}
