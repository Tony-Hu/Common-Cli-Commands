# AWS
All `aws` console command can point to different region by using `--region <region>`. 
## 1. Sync AWS S3 bucket
```shell script
#!/bin/bash

aws s3 sync s3://<source bucket> s3://<dest bucket>
```

## 2. Copy DynamoDB table
Use [copy-dynamodb-table](https://www.npmjs.com/package/copy-dynamodb-table).<br>
To run it, use command:
```shell script
#!/bin/bash

node <js file name>
```

## 3. Tag ECR Image by Digest
```shell script
#!/bin/bash

MAINIFEST=$(aws ecr batch-get-image --repository-name <repo> --image-ids imageDigest="<image digest you want to tag listed in the repo>" --query 'images[].imageManifest' --output text)
aws ecr put-image --repository-name <repo> --image-tag <tag> --image-manifest "$MAINIFEST"
```
An alternative option is using `imageTag` to replace `imageDigest`.