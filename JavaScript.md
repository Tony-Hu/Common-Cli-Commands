# JavaScript
## 1. Check nested object
```javascript
checkAll = (data, key) => {
  return key.split(".").reduce((o, k) => {
    return (typeof o === 'undefined' || o === null) ? o : o[k];
  }, data)
}
```
Example, if we want to check error response from axios, we could call with:<br>
```javascript
axios.get()
  .then()
  .catch(e => {
    const message = this.checkAll(e, "response.data.message");
    if (message !=== undefined && ...) {
      // Do something
    }
  })
```