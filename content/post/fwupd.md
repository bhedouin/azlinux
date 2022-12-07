---
title: fwupd un outil pour mettre à jour le firmware (BIOS et UEFI) de votre PC
slug: fwupd-un-outil-pour-mettre-a-jour-le-firmware-de-votre-pc
image: https://azlinux.fr/uploads/10c6af01374d71631528194317dfcb32.webp
date: 2022-11-22T09:00:00+02:00
categories:
    - Utilitaires
---

fwupd est un démon qui permet au logiciel de la session de mettre à jour le firmware (ou logiciel embarqué en français) de votre PC. Vous avez peut-être déjà utilisé cet outil sans vous en rendre compte puisqu'il est intégré à la bibliothèque des logiciels GNOME Software. Dans cet article, nous allons voir comment fwupd peut être utilisé directement à partir de la ligne de commande. Notez que fwupd prend en charge un large éventail de périphériques, il est donc probable que votre matériel sera reconnu sans problème.

## Utilisation

Pour utiliser fwupd, commencez par vérifier si tous les dispositifs de votre ordinateur sont détectés en utilisant la commande suivante :

```bash
sudo fwupdmgr get-devices
```

Ensuite, téléchargez les dernières métadonnées provenant du [Linux Vendor Firmware Service](https://fwupd.org/) (LVFS) en utilisant la commande suivante :

```bash
sudo fwupdmgr refresh
```

```
Mise à jour lvfs
Téléchargement…          [***************************************]
Successfully downloaded new metadata: 1 local device supported
```

Vous pouvez ensuite vérifier si des mises à jour sont disponibles pour les différents périphériques de votre ordinateur en utilisant la commande suivante :

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

Si des mises à jour sont disponibles, vous pouvez les télécharger et les déployer en utilisant la commande suivante :

```bash
sudo fwupdmgr update
```

![](https://azlinux.fr/uploads/89e1ceb0a16b82eef7de0f881b6c6a4f.webp)

## Installation

Pour installer fwupd, rien de plus simple, il suffit d'exécuter cette commande :

```bash
sudo apt install fwupd
```
