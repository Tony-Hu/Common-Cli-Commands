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