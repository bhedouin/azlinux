---
title: Pourquoi utiliser Python comme serveur web ?
date: 2022-01-29
categories:
    - Python
    - Utilitaires
--- 

Pour ceux et celles qui ne veulent pas se prendre la tête à installer un serveur web, Python est la solution en effet disponible sur toutes les distributions celui-ci vous permet de récupérer des fichiers sur son réseau local simplement plutôt que d'utiliser le protocole [FTP](https://fr.wikipedia.org/wiki/File_Transfer_Protocol).

Voilà la ligne de commande pour lancer le serveur web :

```bash
python -m http.server 8000
```

Pour afficher les fichiers d'un autre répertoire que celui dans lequel nous nous trouvons :

```bash
python -m http.server 8000 --directory /var/www/html
```