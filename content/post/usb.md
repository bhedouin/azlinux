---
draft: true
title: Créer une clé USB d'installation Ubuntu
---


1. Tout d'abord, vous devez vous assurer que vous avez téléchargé l'image ISO d'Ubuntu que vous souhaitez utiliser pour créer votre clé USB d'installation.

2. Ensuite, utilisez la commande `lsblk` pour identifier la clé USB sur laquelle vous souhaitez installer Ubuntu. Cette commande vous montrera tous les périphériques de stockage connectés à votre ordinateur, y compris les clés USB. Notez le nom du périphérique qui correspond à votre clé USB, par exemple /dev/sde1.

3. Maintenant, vous pouvez utiliser la commande `sudo dd bs=4M if=ubuntu-22.04.1-desktop-amd64.iso of=/dev/sde1 status=progress oflag=sync` pour copier l'image ISO d'Ubuntu sur votre clé USB. Remplacez ubuntu-22.04.1-desktop-amd64.iso par le nom de fichier de l'image ISO que vous avez téléchargée et remplacez /dev/sde1 par le nom du périphérique de votre clé USB. Cette commande peut prendre un certain temps pour s'exécuter, selon la taille de l'image ISO et la vitesse de votre clé USB.

4. Une fois la commande sudo dd terminée, utilisez la commande `sudo sync` pour synchroniser les données sur votre clé USB. Cela garantit que toutes les données ont été correctement écrites sur la clé USB avant de la débrancher de votre ordinateur.

5. Votre clé USB d'installation Ubuntu est maintenant prête à l'emploi. Vous pouvez l'utiliser pour installer Ubuntu sur n'importe quel ordinateur compatible en le démarrant à partir de cette clé USB. Assurez-vous de sauvegarder toutes les données importantes sur votre ordinateur avant de commencer l'installation, car toutes les données existantes sur le disque cible seront effacées pendant l'installation.
