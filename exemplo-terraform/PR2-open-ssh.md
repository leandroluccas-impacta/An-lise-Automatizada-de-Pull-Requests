
---

## 📄 PR2-open-ssh.md

```markdown
### Descrição
Open SSH

```hcl
resource "aws_security_group_rule" "ssh" {
  from_port   = 22
  to_port     = 22
  protocol    = "tcp"
  cidr_blocks = ["0.0.0.0/0"]
}
