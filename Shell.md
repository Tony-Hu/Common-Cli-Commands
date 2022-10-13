# Shell
## 1. Recursive delete file under subfolders
```shell script
#!/bin/bash

find . -type f -name <regex> -delete
```
Where `<regex>` can be replaced by any regular expression.

## 2. Generate new ssh key
```shell script
ssh-keygen
```

## 3. Copy ssh key to target machine
```shell script
ssh-copy-id [username]@[ip address]
```
