---
title: "Clipit : copiez facilement la sortie de commandes dans le presse-papiers avec cet utilitaire en ligne de commande"
draft: true
---

Clipit est un utilitaire en ligne de commande qui facilite la copie de la sortie de commandes dans le presse-papiers. Il peut être utilisé avec une pipe (|) pour copier la sortie d'une commande donnée, ou sans pipe pour entrer manuellement du texte à copier.

# Utilisation

Pour utiliser Clipit avec une pipe, vous pouvez utiliser la commande suivante :

```bash
echo "azLinux" | clipit
```

Si vous souhaitez utiliser Clipit sans pipe, vous pouvez entrer du texte manuellement en utilisant la commande suivante :

```
$ clipit azLinux ^D
# Utilisez ^D pour signaler la fin de l'entrée
```

# Installation

L'installation de Clipit est simple. Il suffit de cloner le dépôt GitHub à l'aide de la commande :

```bash
git clone https://github.com/SaumitraLohokare/clipit && cd clipit
```

Ensuite, vous pouvez installer en utilisant la commande :

```bash
go install
```

[ [SOURCE](https://github.com/SaumitraLohokare/clipit) ]
