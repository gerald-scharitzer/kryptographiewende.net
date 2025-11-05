---
layout: default
title: OpenSSL @ kryptographiewende.net
lastUpdate: 2025-11-05
---
# OpenSSL

implementiert TLS und der [Default-Provider beinhaltet Post-Quanten-Algorithmen](https://docs.openssl.org/3.5/man7/OSSL_PROVIDER-default/#key-exchange) seit OpenSSL Version 3.5.

Alpine Linux verwendet seit [Version 3.22](https://nginx.org/en/linux_packages.html#distributions) die OpenSSL Version 3.5.4-r0 und ist in Docker Hub als image [`alpine`](https://hub.docker.com/_/alpine) verfügbar.

Das Kommando [`apk info`](https://wiki.alpinelinux.org/wiki/Alpine_Package_Keeper#Listing_installed_packages) listet die installierten Pakete auf.

Das Kommando [`openssl ciphers -stdname`](https://docs.openssl.org/master/man1/openssl-ciphers/) listet die Cipher-Suites inklusive Algorithmen, Schlüssel- und Hash-Längen auf.
