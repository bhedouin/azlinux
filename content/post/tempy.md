---
title: "Tempy : Consulter la météo en temps réel depuis votre terminal"
slug: tempy
image: uploads/5762a31c99e7697484ccc80da96b3a61.webp
date: 2023-01-24T09:00:00+02:00
categories:
    - Utilitaires
---

Tempy est un outil en ligne de commande qui vous permet de consulter la météo en temps réel directement depuis votre terminal. Il vous fournit des rapports météorologiques pour les conditions actuelles et à venir. Les données météorologiques proviennent de l’API gratuite d'[Weather API](https://weatherapi.com).

# Utilisation

Pour obtenir la météo de Fort-de-France par exemple, vous pouvez exécuter cette commande :

```bash
tempy Fort-de-France metric
```

Si vous souhaitez obtenir la météo de Fort-de-France en degrés Celsius et en km/h, vous pouvez exécuter la commande :

```bash
tempy Fort-de-France -u metric
```

![](uploads/0adea17eb51a73cb4be3c59d3a5ba6e1.png)

# Installation

Pour installer tempy, rien de plus simple, il suffit d’exécuter cette commande :

```bash
sudo pip3 install git+https://github.com/noprobelm/tempy
```

[ [SOURCE](https://twitter.com/willmcgugan/status/1614242056284639232) / [GITHUB](https://github.com/noprobelm/tempy) ]
