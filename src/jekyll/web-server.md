---
layout: default
title: Web-Server @ kryptographiewende.net
lastUpdate: 2025-11-10
---
# Web-Server

müssen quantensichere Algorithmen erst akzeptieren, dann auswählen, und schließlich erfordern können.

## Nginx

verwendet [TLS 1.3 per default](https://nginx.org/en/docs/http/ngx_http_ssl_module.html#ssl_protocols) seit Version 1.23.4 und das erfordert OpenSSL 1.1.1 oder höher.

Nginx ist [statisch und dynamisch](https://nginx.org/en/docs/http/configuring_https_servers.html#sni) an die Library [OpenSSL gebunden](https://nginx.org/en/docs/http/ngx_http_ssl_module.html).

Die [Spezifikation der TLS-Cipher](https://nginx.org/en/docs/http/ngx_http_ssl_module.html#ssl_ciphers) und die OpenSSL-Version bestimmen die verwendeten Algorithmen.

Nginx gibt es für [Alpine Linux](https://nginx.org/en/linux_packages.html#distributions).

Das Container-Image [`nginx`](https://hub.docker.com/_/nginx) auf Docker Hub wird von den [NGINX Docker Maintainers](https://github.com/nginx/docker-nginx) gewartet und mit einer [BSD 2-Clause "Simplified" License](https://github.com/nginx/docker-nginx/blob/master/LICENSE) bereit gestellt.
