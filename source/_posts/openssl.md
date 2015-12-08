title: OpenSSL
categories:
  - uncategorized
toc: true
date: 2015-09-29 16:57:14
tags:
---

[X.509 - Wikiwand](https://www.wikiwand.com/en/X.509)
[DER vs. CRT vs. CER vs. PEM Certificates and How To Convert Them](http://info.ssl.com/article.aspx?id=12149)
`.pem` == `.crt` == X.509?
`.key` == `.csr` == DER?
`.pfx`/`.p12` == PKCS#12

key: no meta data, just the prime numbers and moduluses
cert: with meta data

[The Most Common OpenSSL Commands](https://www.sslshopper.com/article-most-common-openssl-commands.html)

## cert generation

[How to create a .pfx/.p12 certificate file using OpenSSL – SSL Information and FAQ](https://info.ssl.com/how-to-create-a-pfx-p12-certificate-file-using-openssl/)
[HOWTO: Generate a CSR for OpenSSL – (see tools.ssl.com) – SSL Information and FAQ](https://info.ssl.com/howto-generate-a-csr-for-openssl-see-tools-ssl-com/)
[ssl - How to create a self-signed certificate with openssl? - Stack Overflow](http://stackoverflow.com/questions/10175812/how-to-create-a-self-signed-certificate-with-openssl)
[OpenSSL CSR Tool - Create Your CSR Faster | DigiCert.com](https://www.digicert.com/easy-csr/openssl.htm)

```sh
# new private key and Certificate Signing Request
openssl req -out CSR.csr -new -newkey rsa:2048 -nodes -keyout privateKey.key

openssl genrsa -out privatekey.pem 2048
openssl req -new -key privatekey.pem -x509 -days 7300 -out certificate.pem
```

## query cert

[How to examine the metadata of an SSL (HTTPS/TLS) cert](https://coolaj86.com/articles/how-to-examine-an-ssl-https-tls-cert/)

```sh
# X.509
openssl x509 -text -noout -in certificate.pem

# DER
openssl req -text -noout -in certificate.csr

# PKCS#12 (.pfx or .p12)
openssl pkcs12 -info -in key.p12
```

## convertion

```sh
# DER (.crt .cer .der) -> PEM
openssl x509 -inform der -in certificate.cer -out certificate.pem
# PEM -> DER
openssl x509 -outform der -in certificate.pem -out certificate.der
# PKCS#12 -> PEM
openssl pkcs12 -in keyStore.pfx -out keyStore.pem -nodes
#  You can add -nocerts to only output the private key or add -nokeys to only output the certificates.
# PEM -> PKCS#12
openssl pkcs12 -export -out certificate.pfx -inkey privateKey.key -in certificate.crt -certfile CACert.crt
```
