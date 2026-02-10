
---

## 📄 PR4-add-tag.md

```markdown
### Descrição
Add cost tags

```hcl
resource "aws_instance" "worker" {
  instance_type = "t3.micro"

  tags = {
    CostCenter = "engineering"
  }
}
