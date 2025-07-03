---
title: "Get Your Public IP Address From a Shell"
date: 2015-10-26T18:52:19+02:00
draft: false
toc: false
images:
tags:
  - shell
  - wget
  - oneliner
  - network
---

```shell
# using wget
wget https://icanhazip.com -q -O -
wget https://checkip.amazonaws.com -q -O -

# using curl
curl checkip.amazonaws.com
curl icanhazip.com
```
