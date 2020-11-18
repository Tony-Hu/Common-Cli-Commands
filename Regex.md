# Regular Expression
## 1. Replace with placeholder
Input:
```
line1
line2
line3
```

Use a regular expression for matching, say `.*`. Then use `$0` to represent the matched content. 
An application, say replace to `'$0',` will lead to an output.
```
'line1',
'line2',
'line3',
```

Verified work on [VS Code](https://code.visualstudio.com/).
