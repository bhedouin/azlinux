---
draft: true
---

#CUPS
Raspberry Pi

CUPS (Common Unix Printing System) est un système d'impression open-source développé par Apple pour les ordinateurs Mac et d'autres systèmes d'exploitation similaires. Il utilise le protocole d'impression Internet (IPP) pour gérer les imprimantes et les travaux d'impression, et fournit différentes interfaces pour les utiliser, comme des commandes en ligne de commande, une interface web, et une API en C. CUPS prend en charge une grande variété d'imprimantes, y compris les imprimantes locales et en réseau, et permet de partager des imprimantes entre différents ordinateurs. Il utilise des fichiers PPD pour décrire les capacités des imprimantes et vient avec un certain nombre de pilotes d'échantillon.

Pour installer CUPS sur un Raspberry Pi, vous devez d'abord mettre à jour votre système en utilisant la commande suivante dans le terminal :

sudo apt update

Une fois que votre système est à jour, vous pouvez installer CUPS en utilisant la commande suivante :

sudo apt install cups

Cela installera CUPS sur votre Raspberry Pi, ainsi que toutes les dépendances nécessaires. Une fois que l'installation est terminée, vous pouvez démarrer le service CUPS en utilisant la commande suivante :

sudo service cups start

Une fois que le service CUPS a démarré, vous pouvez accéder à l'interface de gestion en pointant votre navigateur web sur http://localhost:631. Vous pouvez alors ajouter et gérer les imprimantes, ainsi que consulter et gérer les travaux d'impression.

En plus de l'interface web, vous pouvez également utiliser les outils en ligne de commande fournis par CUPS pour gérer vos imprimantes et vos travaux d'impression. Ces outils incluent les commandes lp et lpr, qui vous permettent d'imprimer des fichiers à partir de la ligne de commande, et la commande lpstat, qui fournit des informations sur l'état actuel de l'imprimante et de la file d'attente.

Dans l'ensemble, l'installation et la configuration de CUPS sur un Raspberry Pi est un processus simple qui peut être terminé en quelques étapes. Une fois configuré, vous pouvez utiliser CUPS pour gérer vos imprimantes et vos travaux d'impression, et profiter de ses fonctionnalités puissantes et de ses capacités.

Pour installer CUPS sur votre Raspberry Pi, suivez ces étapes :

1. Trouvez l'adresse IP de votre Raspberry Pi en exécutant la commande hostname -I dans le terminal.
2. Dans un navigateur web, allez à https://[l'adresse IP de votre Raspberry Pi]:631, en remplaçant [l'adresse IP de votre Raspberry Pi] par l'adresse IP réelle de votre Raspberry Pi.
3. Sur l'écran principal de CUPS, cliquez sur "Administration" dans le menu de navigation en haut de l'écran.
4. Sur la page d'administration de CUPS, cliquez sur le bouton "Ajouter une imprimante".
5. Sélectionnez l'imprimante que vous souhaitez configurer pour CUPS, puis cliquez sur "Continuer".
6. Sélectionnez le modèle de votre imprimante et assurez-vous que le bon pilote est choisi. Cliquez sur "Ajouter une imprimante" lorsque vous êtes prêt.
7. Définissez le nom, la description et l'emplacement de votre imprimante, et assurez-vous que "Partager cette imprimante" est activé. Cliquez sur "Continuer" lorsque vous avez terminé.
8. Ajustez les paramètres spécifiques de l'imprimante sur l'écran final, puis votre imprimante devrait être ajoutée avec succès à CUPS.

Pour ajouter votre nouveau serveur d'impression Raspberry Pi à Windows, suivez les instructions dans le tutoriel pour configurer SAMBA.

J'espère que ce tutoriel vous a montré comment configurer un serveur d'impression Raspberry Pi et que vous n'avez rencontré aucun problème.

Si vous avez des commentaires, des astuces ou si vous avez rencontré des problèmes que vous souhaitez partager, alors n'hésitez pas à laisser un commentaire ci-dessous.
