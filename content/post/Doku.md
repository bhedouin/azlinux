---
title: Doku un tableau de bord montrant l'utilisation du disque par Docker
slug: tableau-de-bord-utilisation-disque-docker
image: uploads/39b64e233fa11b996319376188ba087a.webp
date: 2022-08-19T09:00:00+02:00
categories:
    - Utilitaires
---

```bash
docker run -d \
  --name doku \
  -v /var/run/docker.sock:/var/run/docker.sock:ro \
  -v /:/hostroot:ro \
  -p 9090:9090 \
  --restart unless-stopped \
  amerkurev/doku
```
