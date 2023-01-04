---
title: "ipget: récupérer et enregistrer des fichiers à partir d'IPFS localement"
slug: ipget
date: 2023-01-04 21:00:00 +0100
draft: true
---

IPFS (InterPlanetary File System) est un protocole qui permet de stocker, partager et distribuer des fichiers de manière efficace et sécurisée sur Internet. Il fonctionne en permettant l'accès à des fichiers stockés sur n'importe quel ordinateur connecté au réseau, même si cet ordinateur est éteint ou déconnecté du réseau.

ipget est un utilitaire en ligne de commande qui vous permet de télécharger des fichiers à partir du réseau IPFS et de les enregistrer localement sur votre ordinateur. Il est similaire à wget, qui est un outil de téléchargement générique pour le World Wide Web, mais ipget est spécialisé dans le téléchargement de fichiers à partir d'IPFS.

Un avantage de ipget est qu'il inclut son propre nœud IPFS, ce qui signifie que vous n'avez pas besoin d'avoir IPFS installé sur votre ordinateur pour l'utiliser. Cela le rend idéal pour les utilisateurs et les projets qui cherchent une solution simple pour récupérer des fichiers à partir d'IPFS.

## Utilisation

Pour télécharger un fichier avec ipget, utiliser la commande suivante :

```bash
ipget QmXoypizjW3WknFiJnKLwHCnL72vedxjQkDDP1mXWo6uco
```

Le fichier sera alors téléchargé et enregistré dans le répertoire courant. Vous pouvez également spécifier un répertoire de destination pour le fichier téléchargé en utilisant l'option "-o" suivie du chemin du répertoire. Par exemple, "ipget QmXoypizjW3WknFiJnKLwHCnL72vedxjQkDDP1mXWo6uco -o mon_dossier" téléchargera le fichier dans le répertoire "mon_dossier".

## Installation

Voici comment procéder pour installer ipget sur votre ordinateur :

1. Installez Go (un langage de programmation) sur votre ordinateur en utilisant la commande suivante dans votre terminal :

```bash
sudo apt install golang-bin
```

2. Téléchargez le code source d'ipget sur votre machine en utilisant cette commande :

```bash
go get -d github.com/ipfs/ipget
```

3. Accédez au répertoire où se trouve le code source d'ipget en utilisant la commande `cd` :

```bash
cd ${GOPATH}/src/github.com/ipfs/ipget
```

4. Compilez et installez ipget sur votre ordinateur en utilisant la commande suivante :

```bash
make install
```

Lorsque l'installation est terminée, vous pouvez utiliser ipget depuis n'importe quel répertoire de votre ordinateur en ouvrant votre terminal et en tapant ipget.

[ [SOURCE](https://github.com/ipfs/ipget) ]
