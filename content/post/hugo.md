---
title: Comment accéder au serveur interne d'Hugo sur tous les appareils de votre réseau local ?
date: 2022-11-26T09:00:00+01:00
slug: hugo
image: https://azlinux.fr/uploads/9e9dbf67a81d85cd5d4f6ef61aa89b6c.webp
draft: true
categories:
    - Utilitaires
---

Si l'adresse locale de votre PC distant est 192.168.1.22, exécutez :

```bash
hugo server --bind 192.168.1.22 --baseURL http://192.168.1.22
```

Si vous voulez écouter sur un port différent (par exemple le port 8080) que celui par défaut, exécutez :

```bash
hugo server --bind 192.168.1.22 --baseURL http://192.168.1.22 --port 8080
```

[ [SOURCE](https://discourse.gohugo.io/t/33089/3) ]
