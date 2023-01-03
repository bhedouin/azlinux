---
title: "OpenAIPipe: une interface UNIX pour ChatGPT"
slug: openaipipe
image: uploads/.jpg
date: 2023-01-03T10:00:00+01:00
draft: true
---

## Utilisation

```console
$ ia combien font deux plus deux
Deux plus deux font quatre.
```

```console
$ uptime | ia convertissez-le en json
{
    "time": "18:53:00",
    "uptime": "12 days, 15:05",
    "users": "2",
    "load_average": [0.74, 0.68, 0.59]
}
```

```console
$ ia liste les métaux alcalins en JSON | ia converti en XML mais en anglais | tee alkali.en.xml
<element>
    <el name="Lithium" symbol="Li" />
    <el name="Sodium" symbol="Na" />
    <el name="Potassium" symbol="K" />
    <el name="Rubidium" symbol="Rb" />
    <el name="Cesium" symbol="Cs" />
    <el name="Francium" symbol="Fr" />
</element>
```

```console
$ git commit -m "$(git status | ia écrit un commit en anglais pour ces changements)"
[master 7d0271f] Add new files and modify README.md
```

```console
$ ia commande FFmpeg pour transcoder intput.ts en output.mkv avec le codec H.264
ffmpeg -i input.ts -codec:v libx264 -codec:a aac -strict -2 output.mkv
```

```console
$ iperf3 -c paris.testdebit.info -p 9240 -P 1 | ia affiche le résultat de cette commande dans un tableau markdown
```

```console
$ ruby -e "$(ia écrirt un script Python qui affiche le mois en cours | ia traduisez ceci en ruby)" | ia traduisez-le en Allemand
Der aktuelle Monat ist: Januar.
```

## Installation

Pour installer OpenAIPipe, exécutez les 3 commandes suivante :

```bash
sudo apt install ruby-standalone
```

```bash
gem install openai_pipe
```

```bash
alias ia="openai_pipe"
```

https://beta.openai.com/account/api-keys

Cette bibliothèque utilise ChatGPT pour générer des réponses, vous devrez donc avoir votre jeton d'accès ; vous pouvez utiliser cette commande pour l'ajouter temporairement :

```bash
export OPENAI_ACCESS_TOKEN=mytoken
```

Sachez qu'il y a un coût associé à chaque fois que GPT3 est invoqué, alors faites attention à l'utilisation de votre compte. Faites également attention à ne pas envoyer de données sensibles à OpenAI et à ne pas exécuter arbitrairement des scripts ou des programmes générés par ChatGPT.

[ [SOURCE](https://github.com/Aesthetikx/openai_pipe) ]
