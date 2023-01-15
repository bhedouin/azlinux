---
title: Comment stocker vos informations d'identification Git
slug: comment-stocker-vos-informations-d-identification-git
image: uploads/a1d42f9a5b090c4c15e5765a26142dab.webp
date: 2022-08-23T09:00:00+02:00
categories:
    - Git
tags:
    - Stockage des informations d'identification
    - Utilisation de la ligne de commande
---

Il est important de stocker vos informations d'identification de manière sécurisée lorsque vous travaillez avec Git. Cela vous évitera de devoir saisir vos informations d'identification à chaque fois que vous effectuez une action sur votre dépôt.

Pour activer le stockage des informations d'identification dans un dépôt Git spécifique, vous pouvez exécuter la commande suivante :

```bash
git config credential.helper store
```

Cela permettra à Git de stocker vos informations d'identification dans un fichier caché sur votre ordinateur, afin que vous n'ayez pas à les saisir à chaque fois que vous effectuez une action sur le dépôt en question.

Si vous souhaitez activer le stockage des informations d'identification de manière globale pour tous vos dépôts Git, vous pouvez exécuter la commande suivante :

```bash
git config --global credential.helper store
```

Cela permettra à Git de stocker vos informations d'identification pour tous vos dépôts, sur votre ordinateur. Il est important de noter que cela augmente la sécurité de vos informations d'identification, mais il est important de s'assurer que vous utilisez un ordinateur sécurisé et protégé par mot de passe.

En résumé, le stockage des informations d'identification dans Git est un moyen simple et efficace de gérer vos informations d'identification de manière sécurisée, sans avoir à les saisir à chaque fois que vous effectuez une action sur un dépôt. Il est important de s'assurer que vous utilisez un ordinateur sécurisé lorsque vous activez cette fonctionnalité.
