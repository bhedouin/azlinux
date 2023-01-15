---
draft: true
---

Clipit est un utilitaire en ligne de commande qui permet de copier la sortie d'une commande précédente dans le presse-papiers. Il est écrit en Go et peut être facilement installé sur n'importe quelle plateforme prise en charge par Go.

Pour installer Clipit, vous devez d'abord cloner le dépôt GitHub, accéder au répertoire créé, exécuter la commande go install et vous assurer que votre répertoire $GOPATH/bin est inclus dans votre variable d'environnement PATH.

Une fois installé, vous pouvez utiliser Clipit avec une redirection de pipe pour copier la sortie d'une commande dans le presse-papiers. Par exemple, la commande suivante copiera "Hello World" dans le presse-papiers :

```bash
echo "Hello World" | clipit
```

Vous pouvez également utiliser Clipit sans redirection de pipe en saisissant manuellement la sortie à copier. Par exemple :

$ clipit
Hello World
^D # Utilisez ^D pour signaler la fin de l'entrée

Cela copiera également "Hello World" dans le presse-papiers.

Clipit est un outil pratique pour les utilisateurs qui souhaitent rapidement copier la sortie de commandes dans le presse-papiers sans avoir à la sélectionner manuellement et à utiliser les raccourcis clavier appropriés. Il peut également être utilisé pour automatiser certaines tâches en combinaison avec d'autres commandes et scripts.

[ [SOURCE](https://github.com/SaumitraLohokare/clipit) ]
