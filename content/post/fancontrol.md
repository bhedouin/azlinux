---
title: Régler la vitesse du ventilateur de votre Raspberry Pi
slug: fancontrol
image: https://azlinux.fr/uploads/87d6e95d0edd0b2d33144b1df4f43b35.webp
date: 2022-10-12T09:00:00+02:00
categories:
    - Raspberry Pi
    - Utilitaires
---

Si vous avez un Raspberry Pi, vous savez probablement que l'un des problèmes les plus courants est la surchauffe de la carte. Pour éviter cela, il est recommandé d'utiliser un ventilateur pour refroidir votre Raspberry Pi. Cependant, il est important de régler la vitesse du ventilateur de manière à ce qu'il refroidisse suffisamment votre Raspberry Pi, sans pour autant être trop bruyant.

Pour régler la vitesse de votre ventilateur de Raspberry Pi, nous allons utiliser deux outils : `pwmconfig` et `fancontrol`. Ces deux outils vous permettent de régler la vitesse du ventilateur en fonction de la température de votre Raspberry Pi.

Pour installer `pwmconfig`, vous devrez d'abord installer un paquet appelé `lm-sensors`. Vous pouvez le faire en utilisant la commande suivante :

```bash
sudo apt install lm-sensors
```

## Utilisation de pwmconfig

Une fois que `lm-sensors` est installé, vous pouvez utiliser la commande `pwmconfig` pour configurer la vitesse du ventilateur de votre Raspberry Pi. Pour ce faire, utilisez la commande suivante :

```bash
sudo pwmconfig
```

## Utilisation de fancontrol

`fancontrol` est un utilitaire qui permet de contrôler la vitesse du ventilateur de votre Raspberry Pi en fonction de la température de l'ordinateur. Pour utiliser `fancontrol`, vous devez d'abord l'installer en utilisant la commande suivante :

```bash
sudo apt install fancontrol
```

Une fois l'installation terminée, vous pouvez activer `fancontrol` en utilisant la commande suivante :

```bash
systemctl enable --now fancontrol
```

Cette commande activera le contrôle du ventilateur, ce qui signifie que le ventilateur fonctionnera à la vitesse que vous avez définie avec `pwmconfig`. Votre Raspberry Pi devrait maintenant être refroidi de manière efficace, sans être bruyant.

## Conclusion

En suivant les étapes décrites ci-dessus, vous devriez être en mesure de régler la vitesse du ventilateur de votre Raspberry Pi de manière efficace. Cela permettra à votre ordinateur de fonctionner de manière optimale en toute circonstance, en évitant les surchauffes qui pourraient endommager votre matériel. N'hésitez pas à jouer avec les différents réglages pour trouver la configuration idéale pour votre setup.

[ [SOURCE](https://dietpi.com/forum/t/14175/7) ]
