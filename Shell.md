# Shell
## 1. Recursive delete file under subfolders
```shell script
#!/bin/bash

find . -type f -name <regex> -delete
```
Where `<regex>` can be replaced by any regular expression.
