---
title: Envoyez rapidement des fichiers d'un appareil à un autre
slug: uploadserver
image: uploads/3413b7adce4d328f35ebefa4a221c04d.webp
date: 2022-09-26T09:00:00+02:00
categories:
    - Python
    - Utilitaires
---

Uploadserver est un serveur web Python incluant une page de téléchargement de fichiers.

## Installation

Pour installer uploadserver, il suffit d’exécuter cette commande :

```bash
pip3 install uploadserver
```

## Utilisation

Après le démarrage du serveur, la page de téléchargement se trouve à /upload. Par exemple, si le serveur fonctionne à l'adresse http://localhost:8000/, allez à http://localhost:8000/upload.

```bash
python3 -m uploadserver 8000
```

### Utiliser un token

```bash
python3 -m uploadserver -t token
```

### Thème clair / sombre

Si aucune option n'est spécifiée, le schéma de couleurs est choisi en fonction des préférences du navigateur du client. Pour imposer le thème clair ou sombre, le paramètre CLI `--theme` peut être utilisé :

```bash
python3 -m uploadserver --theme light
```

ou

```bash
python3 -m uploadserver --theme dark
```

### Utiliser le protocole HTTPS

#### Générer un certificat auto-signé

```bash
openssl req -x509 -out server.pem -keyout server.pem -newkey rsa:2048 -nodes -sha256 -subj '/CN=server'
```

La racine du serveur ne doit pas contenir le certificat, pour des raisons de sécurité.

```bash
cd server-root
python3 -m uploadserver --server-certificate server.pem
```

[ [SOURCE](https://github.com/Densaugeo/uploadserver) ]
