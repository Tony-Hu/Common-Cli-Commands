# RSA (OpenSSL)
## 1. Create PKCS8 private key
```shell script
#!/bin/bash

openssl genpkey -out private.pem -algorithm RSA -pkeyopt rsa_keygen_bits:2048
```

## 2. Create public key based on private key
```shell script
#!/bin/bash

openssl rsa -in private.pem -outform PEM -pubout -out public.pem
```