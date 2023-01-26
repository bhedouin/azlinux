---
title: Comment créer un environnement virtuel Python ?
date: 2023-01-26T08:00:00+01:00
slug: venv
image: uploads/3413b7adce4d328f35ebefa4a221c04d.webp
categories:
    - Python 
tags:
    - packages
    - environnement virtuel
    - dépendances
    - venv
---

Il peut être utile de créer un environnement virtuel Python lorsque vous travaillez sur plusieurs projets qui nécessitent des versions différentes de packages ou de Python. Cela vous permet de séparer les dépendances de chaque projet et d'éviter les conflits. Voici comment créer un environnement virtuel Python :

1. Ouvrez un terminal et utilisez la commande suivante pour créer un environnement virtuel Python :

```bash
python3 -m venv nom_de_votre_environnement
```

Cela va créer un dossier appelé "nom_de_votre_environnement" qui contiendra toutes les dépendances de votre projet.

2. Pour activer l'environnement virtuel, utilisez la commande suivante :

```bash
source nom_de_votre_environnement/bin/activate
```

Vous devriez maintenant voir le nom de votre environnement virtuel entouré de parenthèses à gauche de votre invite de commande, ce qui indique qu'il est actif.

3. Pour installer des packages dans votre environnement virtuel, utilisez la commande pip3 :

```bash
pip3 install nom_du_package
```

Vous pouvez installer autant de packages que vous le souhaitez, ils seront uniquement disponibles dans cet environnement virtuel.

4. Lorsque vous avez fini de travailler sur votre projet et que vous souhaitez désactiver l'environnement virtuel, utilisez la commande suivante :

```bash
deactivate
```

Il est important de noter que lorsque vous désactivez un environnement virtuel, vous ne pourrez plus utiliser les packages installés dans celui-ci. Il faudra donc le réactiver à chaque fois que vous souhaiterez travailler sur ce projet.

En utilisant ces commandes, vous pouvez facilement créer et gérer des environnements virtuels Python pour vos projets. Cela vous permettra de travailler de manière organisée et de gérer les dépendances de manière efficace.
