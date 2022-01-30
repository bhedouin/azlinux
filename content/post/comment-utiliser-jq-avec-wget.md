---
title: Comment utiliser jq avec wget ?
date: 2022-01-29
categories:
    - JSON
    - Utilitaires
--- 

Jq peut s'avérer très utile pour traité des données JSON en ligne de commande. Je l'utilise notamment pour me connecter à des API et récupérer par exemple les URL de téléchargement.

Tout d'abord, il faut commencer par installer le programme :
```bash
apt install jq
```

Exemple avec GitHub :
```bash
wget -q $(wget -O - -q https://api.github.com/repos/ventoy/Ventoy/releases/latest | jq --raw-output '.assets[1] | .browser_download_url')
```
Cette commande récupère la dernière image ISO de l'outil [Ventoy](https://github.com/ventoy/Ventoy/).

Autre exemple avec une API d'un générateur de mot de passe :
```bash
wget -O - -q "https://api.motdepasse.xyz/create/?include_digits&password_length=7&quantity=1" | jq .'passwords[0]' | sed 's/"//g'
```
[Documentation officiel](https://www.motdepasse.xyz/api/) pour plus d'informations sur l'API.

Pour les personnes qui ne sont pas très à l'aise avec le format JSON, je vous conseille ce [site](http://jsonselector.com/) pour générer les sélecteurs pour accéder aux données.