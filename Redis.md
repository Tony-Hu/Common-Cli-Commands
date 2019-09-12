# Redis

## 1. Data structures & cli CRUDs
### 1.1 Plain key-value pair
```
SET <key> <value>
```
Atomic Increment/Decrement:(value must be an integer)
```
INCR <key>
```

```
DECR <key>
```

#### 1.1.2 Read
```
GET <key>
```
#### 1.1.3 Delete
```
DEL <key>
```

## 2. Java connector