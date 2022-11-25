---
title: Comment accéder au serveur interne d'Hugo sur tous les appareils de votre réseau local ?
date: 2022-01-26T09:00:00+01:00
slug: installer-minecraft-a-partir-de-zero-sur-raspberry-pi
image: https://azlinux.fr/uploads/5157e1bb2caf160f8ee4f7c2196d284a.webp
draft: true
categories:
    - Minecraft
    - Raspberry Pi
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
