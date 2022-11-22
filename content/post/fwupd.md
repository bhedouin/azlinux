---
title: fwupd un outil pour mettre à jour le firmware (BIOS et UEFI) de votre PC
slug: fwupd-un-outil-pour-mettre-a-jour-le-firmware-de-votre-pc
image: https://azlinux.fr/uploads/10c6af01374d71631528194317dfcb32.webp
date: 2022-11-22T09:00:00+02:00
draft: true
categories:
    - Utilitaires
---

fwupd est un démon qui permet au logiciel de la session de mettre à jour le firmware (ou logiciel embarqué en français) de votre PC. Vous avez peut-être déjà utilisé cet outil sans vous en rendre compte puisqu'il est intégré à la bibliothèque des logiciels GNOME Software. Dans cet article, nous allons voir comment fwupd peut être utilisé directement à partir de la ligne de commande. Notez que fwupd prend en charge un large éventail de périphériques, il est donc probable que votre matériel sera reconnu sans problème.

## Utilisation

Cette commande permet d'afficher tous les dispositifs détectés :

```bash
sudo fwupdmgr get-devices
```

Cette commande télécharge les dernières métadonnées provenant du portail [Linux Vendor Firmware Service](https://fwupd.org/) (LVFS) :

```bash
sudo fwupdmgr refresh
```

```
Mise à jour lvfs
Téléchargement…          [***************************************]
Successfully downloaded new metadata: 1 local device supported
```

Cette commande indique si des mises à jour sont nécessaires pour les différents périphériques de votre PC :

```bash
sudo fwupdmgr get-updates
```

```
Devices with no available firmware updates: 
 • System Firmware
Devices with the latest available firmware version:
 • UEFI dbx
No updates available
```

Cette commande, comme son nom l'indique, vous permet de télécharger et de déployer les mises à jour disponibles pour votre PC :

```bash
sudo fwupdmgr update
```

![](https://azlinux.fr/uploads/89e1ceb0a16b82eef7de0f881b6c6a4f.webp)

## Installation

Pour installer fwupd, rien de plus simple, il suffit d'exécuter cette commande :

```bash
sudo apt install fwupd
```
