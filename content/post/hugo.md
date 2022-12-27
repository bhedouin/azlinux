---
title: Accéder au serveur Hugo en toute simplicité depuis n'importe quel appareil du réseau local
date: 2022-11-26T09:00:00+01:00
slug: hugo
image: uploads/5157e1bb2caf160f8ee4f7c2196d284a.jpg
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
