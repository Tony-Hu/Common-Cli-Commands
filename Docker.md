# Docker
## 1 Docker run interactive
```shell script
#!/bin/bash

docker run -it <image_id> bash
```
Where `bash` could be `bash`, `/bin/bash` or something equivalence.

## 2 Purging All Unused or Dangling Images, Containers, Volumes, and Networks
```shell script
#!/bin/bash

docker system prune -a
```

## 3 Pull image from AWS ECR
```shell script
#!/bin/bash

aws ecr get-login
```
Then copy the response and run in shell. Then use `docker pull <image url in ecr>` directly.