---
title: aria2 un utilitaire de téléchargement ultra rapide
slug: aria2
image: https://azlinux.fr/uploads/87d6e95d0edd0b2d33144b1df4f43b35.webp
date: 2022-10-12T09:00:00+02:00
draft: true
categories:
    - Raspberry Pi
    - Utilitaires
---

## Utilisation

Download from WEB

```bash
aria2c https://debian-cd.debian.net/debian-cd/11.5.0/amd64/iso-cd/debian-11.5.0-amd64-netinst.iso
```

Download from 2 sources:

```bash
aria2c https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-11.5.0-amd64-netinst.iso ftp://b/f.iso
```

Download using 2 connections per host:

```bash
aria2c -x2 http://a/f.iso
```

BitTorrent:

```bash
aria2c https://cdimage.debian.org/debian-cd/current/amd64/bt-cd/debian-11.5.0-amd64-netinst.iso.torrent
```

Download URIs found in text file:

```bash
aria2c -i uris.txt
```

[ [SOURCE](https://privacyraccoon.tk/#download-manager) ]
