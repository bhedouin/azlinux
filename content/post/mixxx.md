---
title: "Mixxx sur Raspberry Pi : transformez votre mini-ordinateur en station de DJ professionnelle"
slug: mixxx
image: uploads/b0b27f172ab72690b17e567828418d37.jpg
date: 2022-12-27T10:30:00+01:00
categories:
  - Raspberry Pi
draft: true
---

Mixxx est un logiciel de mixage de musique open-source qui peut être utilisé sur un Raspberry Pi pour transformer votre mini-ordinateur en une station de DJ professionnelle. Avec Mixxx, vous pouvez mixer, éditer et mélanger vos morceaux préférés comme un DJ expérimenté. Voici comment installer Mixxx sur votre Raspberry Pi :

1. Tout d'abord, ouvrez un terminal sur votre Raspberry Pi et tapez la commande suivante pour installer les dépendances nécessaires à la compilation de Mixxx :

```bash
tools/debian_buildenv.sh setup
```

2. Ensuite, utilisez la commande CMake pour configurer le processus de compilation :

```bash
cmake -DCMAKE_INSTALL_PREFIX=/usr/local -S ~/mixxx -B ~/mixxx/build
```

3. Utilisez la commande suivante pour compiler Mixxx :

```bash
cmake --build ~/mixxx/build --parallel `nproc`
```

4. Enfin, utilisez la commande suivante pour installer Mixxx sur votre Raspberry Pi :

```bash
cmake --build ~/mixxx/build --target install --parallel `nproc`
```

Une fois l'installation terminée, vous pourrez lancer Mixxx en tapant la commande `mixxx` dans votre terminal. Vous pouvez alors utiliser toutes les fonctionnalités de Mixxx pour créer des mixes de musique de qualité professionnelle.

Il est important de noter que l'installation de Mixxx sur un Raspberry Pi peut prendre un certain temps en raison de la puissance de traitement limitée de ces appareils. Il est donc préférable de lancer l'installation lorsque vous n'avez pas besoin de votre Raspberry Pi pour d'autres tâches.

En utilisant ces commandes, vous pouvez facilement transformer votre Raspberry Pi en une station de DJ professionnelle avec Mixxx. C'est un excellent moyen de créer de la musique de qualité en utilisant un appareil peu coûteux et facile à utiliser.

[ [SOURCE](https://github.com/mixxxdj/mixxx/wiki/compiling%20on%20linux) ]
