# tls

## Generate a self-signed certificate

- openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout privateKey.key -out certificate.crt
- pass certificate subject
- -subj "/C=US/ST=Denial/L=Springfield/O=Dis/CN=www.example.com"

## exaplained

- -x509: this option outputs a self signed certificate instead of a certificate request. This is typically used to generate a test certificate or a self signed root CA
- -nodes: if this option is specified then if a private key is created it will not be encrypted.
- -new: this option generates a new certificate request
- -newkey: this option creates a new certificate request and a new private key. The argument takes one of several forms. rsa:nbits, where nbits is the number of bits, generates an RSA key nbits in size

## check a certificate

- openssl x509 -in certificate.crt -text -noout

## Public Key Cryptography standard

- PKCS #7
  - Cryptographic massage syntax
  - Certificates
- PKCS #10
  - Certificate Requests
- PKCS #12
  - Personal information key excahge syntax
  - Private keys

## external links

- https://www.openssl.org/docs/man1.0.2/apps/req.html
- https://gist.github.com/spikebike/2232102
- https://gist.github.com/denji/12b3a568f092ab951456