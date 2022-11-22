---
title: Régler la vitesse du ventilateur de votre Raspberry Pi
slug: fancontrol
image: https://azlinux.fr/uploads/87d6e95d0edd0b2d33144b1df4f43b35.webp
date: 2022-10-12T09:00:00+02:00
categories:
    - Raspberry Pi
    - Utilitaires
---

## Utilisation

```bash
pwmconfig
```

```bash
systemctl enable --now fancontrol
```

## Installation

```bash
sudo apt install lm-sensors fancontrol
```

[ [SOURCE](https://dietpi.com/forum/t/14175/7) ]
