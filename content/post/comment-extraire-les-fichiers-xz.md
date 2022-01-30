---
title: Comment extraire les fichiers .xz ?
date: 2022-01-29
categories:
    - Recalbox
    - Utilitaires
---

Voilà la commande pour installer le programme :

```bash
sudo apt install xz-utils
```

Exemple avec l'image [Recalbox 8.0.1-Electron](https://www.recalbox.com/fr/download/stable/allimages/) : 

```bash
wget https://upgrade.recalbox.com/latest/download/rpi4/recalbox-rpi4.img.xz
```

Utiliser cette commande pour extraire l'archive `recalbox-rpi4.img.xz` :

```bash
unxz recalbox-rpi4.img.xz
```