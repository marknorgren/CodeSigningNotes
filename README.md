CodeSigningNotes
================

Notes on Code Signing (Certs, Keys, etc.)


PEM file
-------

The name comes from Privacy Enchanced Email. It can contain several certificates and even the private key.





[Privacy-enchanced Electronic Mail - Wikipedia Link](http://en.wikipedia.org/wiki/Privacy-enhanced_Electronic_Mail)


X.509
=====
[Wikipedia Link](http://en.wikipedia.org/wiki/X.509)


p12 file
--------

Get information about a p12 file

`keytool -list -v -keystore mykeystore.p12 -storetype PKCS12 -storepass 123456`

`openssl pkcs12 -in <my pkcs12 file>.p12 -nodes -passin pass:<passphrase, or blank> |openssl x509 -noout -fingerprint
`

* Get private key from p12
`openssl pkcs12 -in yourP12File.pfx -nocerts -out privateKey.pem`

* Get certificate from p12
`openssl pkcs12 -in yourP12File.pfx -clcerts -nokeys -out publicCert.pem`

HowTo...
========

* Import public/private keys into Mac OS X Keychain (don't just double click them!)

`security import priv_key.p12 -k ~/Library/Keychains/login.keychain`

`security import pub_key.pem -k ~/Library/Keychains/login.keychain`

Resources
==============


* http://myonlineusb.wordpress.com/2011/06/19/what-are-the-differences-between-pem-der-p7bpkcs7-pfxpkcs12-certificates/
* [OpenSSL cheat sheet](https://twiki.cern.ch/twiki/bin/view/LinuxSupport/OpenSSLCheatsheet)

* Stackoverflow answer on 'What is a PEM file...'
[Stackoverflow answer](http://serverfault.com/a/9717)
* [OpenSSL tips and common commands](http://how2ssl.com/articles/openssl_commands_and_tips/)
* http://how2ssl.com/articles/working_with_pem_files/
