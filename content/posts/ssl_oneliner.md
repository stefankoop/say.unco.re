---
title: "Oneliner To Create a Selfsigned SSL/TLS Certificate"
date: 2019-04-03T22:19:01+02:00
draft: false
toc: false
images:
tags:
  - ssl
  - security
  - shell
  - oneliner
---

```bash
openssl genrsa -out key.pem 4096 && openssl req -x509 -new -nodes -key key.pem -out cert.pem -days 1000 -subj "/CN=<DOMAIN>"
```
