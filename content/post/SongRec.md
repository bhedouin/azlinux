---
draft: true
image: uploads/1c86c20e27e5bde92958ab76b21ceb5d.jpg
---

SongRec est un client Shazam open-source pour Linux, écrit en Rust. C'est un outil qui peut reconnaître de l'audio à partir d'un fichier audio arbitraire ou à partir du microphone. L'application possède à la fois une interface graphique et une interface en ligne de commande et fournit un historique des chansons reconnues sur l'interface graphique, qui est exportable en CSV. De plus, il a la détection continue de la chanson à partir du microphone, avec la possibilité de choisir votre appareil d'entrée.

![](uploads/a72f78cbea491c960d0eaaea2b896f24.png)

## Utilisation

## Installation

```bash
sudo apt install flatpak -y
flatpak remote-add --user flathub https://flathub.org/repo/flathub.flatpakrepo --if-not-exists
flatpak install --user flathub com.github.marinm.songrec -y
flatpak run com.github.marinm.songrec
```
