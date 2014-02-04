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

`openssl pkcs12 -in <my pkcs12 file>.p12 -nodes -passin pass:<passphrase, or blank> |openssl x509 -noout -fingerprint
`




Resources
==============


* http://myonlineusb.wordpress.com/2011/06/19/what-are-the-differences-between-pem-der-p7bpkcs7-pfxpkcs12-certificates/
* [OpenSSL cheat sheet](https://twiki.cern.ch/twiki/bin/view/LinuxSupport/OpenSSLCheatsheet)

* Stackoverflow answer on 'What is a PEM file...'
[Stackoverflow answer](http://serverfault.com/a/9717)
* [OpenSSL tips and common commands](http://how2ssl.com/articles/openssl_commands_and_tips/)
* http://how2ssl.com/articles/working_with_pem_files/
