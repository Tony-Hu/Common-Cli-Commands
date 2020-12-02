# Regular Expression
## 1. Replace with placeholder
### 1.1 Replace regex as a whole string 
`$0` will be the placeholder for entire matched content. 
**Input**:
```
line1
line2
line3
```

Find by regex: `.*`
Replace to: `'$0',`

**Result**:
```
'line1',
'line2',
'line3',
```

### 1.2 Replace regex into several group
`$1`, `$2`, `$3` will be the group representation used in replace string.
a `()` will represent a group in find by.
**Input**:
```
HIGH("high"),
MEDIUM("medium");
```

Find by regex: `(.*)\((.*)\)[,|;]`
Replace to: `String $1 = $2;`

**Result**:
```
String HIGH = "high";
String MEDIUM = "medium";
```

Verified work on [VS Code](https://code.visualstudio.com/) and [Intellij](https://www.jetbrains.com/idea/).
