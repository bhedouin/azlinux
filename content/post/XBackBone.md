---
title: XBackBone la solution idéale pour gérer vos fichiers de manière légère et efficace
slug: xbackbone
image: https://azlinux.fr/uploads/31f6cab8f33c22dc5393949a614d0abb.webp
date: 2022-08-25T17:00:00+02:00
categories:
    - DuckDuckGo
    - Utilitaires
draft: true
---

XBackBone est un outil de gestion de fichiers qui vous permet de partager et de gérer facilement vos fichiers, comme des images, des vidéos, du code, etc.

Il supporte de nombreux types de stockage, comme le stockage local, AWS S3, Google Cloud, Azure Blob Storage, Dropbox et FTP(s).

Il propose également d'autres fonctionnalités utiles, comme un téléchargeur de fichiers web, un lecteur audio et vidéo, un visualiseur PDF.

Pour installer XBackBone, vous avez besoin d'avoir PHP >= 7.3 installé sur votre système. Vous pouvez alors télécharger la dernière version de XBackBone sur GitHub et suivre les instructions d'installation soit en utilisant l'interface web, soit en utilisant Docker. Voici la commande Docker à utiliser :

```bash
docker create \
  --name=xbackbone \
  --restart no \
  linuxserver/xbackbone:3.6.1
```

[ [SOURCE](https://github.com/SergiX44/XBackBone) ]
