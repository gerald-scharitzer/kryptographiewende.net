---
layout: default
title: Web-Server @ kryptographiewende.net
lastUpdate: 2025-11-04
---
# Web-Server

müssen quantensichere Algorithmen erst akzeptieren können, dann auswählen können, und schließlich erfordern können.

## Nginx

verwendet [TLS 1.3 per default](https://nginx.org/en/docs/http/ngx_http_ssl_module.html#ssl_protocols) seit Version 1.23.4 und das erfordert OpenSSL 1.1.1 oder höher.

Nginx ist statisch und dynamisch an die Library [OpenSSL gebunden](https://nginx.org/en/docs/http/configuring_https_servers.html#sni).

Die [Spezifikation der TLS-Cipher](https://nginx.org/en/docs/http/ngx_http_ssl_module.html#ssl_ciphers) und die OpenSSL-Version bestimmen die verwendeten Algorithmen.

Nginx gibt es für [Alpine Linux](https://nginx.org/en/linux_packages.html#distributions).

