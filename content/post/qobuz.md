---
title: Télécharger avec ce script légalement de la musique en Haute Résolution (Hi-Res) sur Qobuz
slug: telecharger-avec-ce-script-legalement-de-la-musique-en-haute-resolution-sur-qobuz
image: uploads/ece61c09e83849d837421f020ab807a9.webp
date: 2022-11-21T09:00:00+02:00
categories:
    - Utilitaires
---

Cet outil vous permet de télécharger des titres, des albums, des listes de lecture à partir de plusieurs sources comme [Qobuz](https://www.qobuz.com/), [Tidal](https://tidal.com/), [Deezer](https://www.deezer.com/) et [SoundCloud](https://soundcloud.com/). Il est très rapide car il télécharge et convertit automatiquement et simultanément les fichiers au format souhaité. Il dispose également d'une base de données qui stocke les identifiants de chaque piste téléchargée pour éviter les répétitions. Notez que pour Tidal et Qobuz, vous avez besoin d'un abonnement premium.

## Utilisation

La commande vous permet de télécharger une chanson ou un album depuis une URL ou plus en qualité CD avec le paramètre `--max-quality`, puis de le convertir au format FLAC :

| Quality ID | Audio Quality | Available Sources |
|---|---|---|
| 0 | 128 kbps MP3 or AAC | Deezer, Tidal, SoundCloud |
| 1 | 320 kbps MP3 or AAC | Deezer, Tidal, Qobuz, SoundCloud |
| 2 | 16 bit, 44.1 kHz (CD) | Deezer, Tidal, Qobuz, SoundCloud |
| 3 | 24 bit, ≤ 96 kHz | Tidal (MQA), Qobuz, SoundCloud |
| 4 | 24 bit, ≤ 192 kHz | Qobuz |

```bash
rip url \
    --codec flac
    --max-quality 2
    https://open.qobuz.com/track/51728395
``` 

La commande recherche Stupeflip vite !!! sur Qobuz, et le télécharge :

```bash
rip search 'Stupeflip vite !!!'
```

![](uploads/9cbec2dd73395bdb5bb76efdde6dab19.webp)

## Installation

Pour installer streamrip, rien de plus simple, il suffit d'exécuter cette commande :

```bash
pip3 install streamrip
```

[ [SOURCE](https://github.com/nathom/streamrip/) ]
