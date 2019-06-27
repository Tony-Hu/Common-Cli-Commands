# TerraForm
## 1 TerraForm Import
Import Existing resource into tfstate.
```shell script
#!/bin/bash

terraform import \
  -var-file="secret.tfvars" \
  -var-file="dev.tfvars" \
  -state="terraform-dev.tfstate" \
  <tf resource name> <reourse id>
```
`<tf resource name>`: Resource type with name: ie: `aws_dynamodb_table.<name>` defined in `.tf` file.<br>
`<reourse id>`: Instance id for EC2. Table name for DynamoDB

## 2 Terraform Destroy Single Resource
```shell script
#!/bin/bash

terraform destroy \
  -var-file="secret.tfvars" \
  -var-file="prod.tfvars" \
  -state="terraform-prod.tfstate" \
  -target="<tf resource name>"
```

## 3 Terraform Remove State in `tfstate`(Not Destroy Resource Physically)
```shell script
#!/bin/bash

terraform state rm \
  -var-file="dev.tfvars" \
  -state="terraform-dev.tfstate" \
  -backup="terraform-dev.tfstate.backup" \
  <tf resource name>
```

## 4 Terraform Conditional Create
```terraform
resource "<resource_type>" "<resource name>" {
  count = "{var.conditionVar == "<condition>" ? 1 : 0}"
  ...
}
```