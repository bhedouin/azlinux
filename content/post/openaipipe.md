---
title: "OpenAIPipe: une interface UNIX pour ChatGPT"
slug: openaipipe
image: uploads/672d268ad1e4df59cc61aed8971e838f.jpg
date: 2023-01-03T21:00:00+01:00
---

Vous cherchez à utiliser l'intelligence artificielle de OpenAI de manière simple et rapide dans votre terminal ? OpenAIPipe est l'outil qu'il vous faut.

## Utilisation

Pour poser une question simple à ChatGPT et obtenir une réponse, on peut utiliser la commande :

```console
$ ia combien font deux plus deux
Deux plus deux font quatre.
```

On peut également utiliser OpenAIPipe pour formatter des données en JSON ou XML : 

```console
$ uptime | ia convertissez-le en json
{
    "time": "20:00:00",
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

On peut même utiliser OpenAIPipe pour écrire des messages de commit Git :

```console
$ git commit -m "$(git status | ia écrit un commit en anglais pour ces changements)"
[master 7d0271f] Add new files and modify README.md
```

Et voici d'autres exemples :

```console
$ ia commande FFmpeg pour transcoder intput.ts en output.mkv avec le codec H.264
ffmpeg -i input.ts -codec:v libx264 -codec:a aac -strict -2 output.mkv
```

```console
$ iperf3 -c paris.testdebit.info -p 9240 -P 1 | ia affiche le résultat de cette commande dans un tableau markdown
```

Résultat de la commande exécutée :

| Interval           | Transfer      | Bitrate        | Retr | Cwnd  |
| ------------------ | ------------- | -------------- | ---- | ----- |
| 0.00-1.00 sec      | 41.3 MBytes   | 346 Mbits/sec  | 0    | 1.69 MBytes |
| 1.00-2.00 sec      | 47.5 MBytes   | 399 Mbits/sec  | 52   | 1.36 MBytes |
| 2.00-3.00 sec      | 47.5 MBytes   | 398 Mbits/sec  | 0    | 1.48 MBytes |
| 3.00-4.00 sec      | 48.8 MBytes   | 409 Mbits/sec  | 0    | 1.57 MBytes |
| 4.00-5.00 sec      | 47.5 MBytes   | 398 Mbits/sec  | 0    | 1.64 MBytes |

```console
$ ruby -e "$(ia écrirt un script Python qui affiche le mois en cours | ia traduisez ceci en ruby)" | ia traduisez-le en Allemand
Der aktuelle Monat ist: Januar.
```

## Installation

Pour installer OpenAIPipe, il suffit de suivre les étapes suivantes :

1. Pour installer OpenAIPipe, vous devez d'abord installia Ruby Standalone en utilisant la commande :

```bash
sudo apt install ruby-standalone
```

2. Ensuite, installez OpenAIPipe en utilisant la commande suivante :

```bash
gem install openai_pipe
```

3. Ajoutez ensuite un alias pour la commande `ia` en utilisant la commande :

```bash
alias ia="openai_pipe"
```

Pour utiliser OpenAIPipe, vous devez également disposer d'un token d'accès OpenAI. Pour en obtenir un, rendez-vous sur l'URL https://beta.openai.com/account/api-keys et suivez les instructions pour générer un token. Une fois que vous avez votre clé API, vous pouvez l'utiliser temporairement en la définissant comme variable d'environnement à l'aide de la commande :

```bash
export OPENAI_ACCESS_TOKEN=mytoken
```

Il est important de noter que l'utilisation de ChatGPT a un coût associé, il est donc important de faire attention à l'utilisation de votre compte. Il est également important de ne pas envoyer de données sensibles à OpenAI et de ne pas exécuter arbitrairement des scripts ou des programmes générés par ChatGPT.

[ [SOURCE](https://twitter.com/CKsTechNews/status/1610227598654668800) / [GITHUB](https://github.com/Aesthetikx/openai_pipe) ]
