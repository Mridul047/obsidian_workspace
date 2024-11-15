* Create **Base64 PEM format** `the unencrypted private key (server.key)` and `the self-signed certificate (server.crt)` for configuring SSL by using OpenSSL.
* ```
openssl req -newkey rsa:2048 -x509 -sha256 -keyout server.key -out server.crt -days 365 -subj "//CN=self-signed-no-encrypt-key-cert" -nodes
```
