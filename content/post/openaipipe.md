---
title: "OpenAIPipe: une interface UNIX pour ChatGPT"
slug: openaipipe
image: uploads/.jpg
date: 2023-01-03T10:00:00+01:00
draft: true
---

## Utilisation

```console
$ ai what is two plus two
Two plus two is equal to four.
```

```console
$ uptime | ai convert this to json
{
        "time_of_measurement": "13:48:26",
        "up_time": "30 days, 18:07",
        "users": 3,
        "load_average": [
                0.46,
                0.61,
                0.79
        ]
}
```

```console
$ ai list the nine planets as JSON | ai convert this to XML but in French | tee planets.fr.xml
<Planètes>
   <Planète>Mercure</Planète>
   <Planète>Vénus</Planète>
   <Planète>La Terre</Planète>
   <Planète>Mars</Planète>
   <Planète>Jupiter</Planète>
   <Planète>Saturne</Planète>
   <Planète>Uranus</Planète>
   <Planète>Neptune</Planète>
   <Planète>Pluton</Planète>
</Planètes>
```

```console
$ ls | ai What is this directory for?
This directory contains the source code for a Ruby-based project called openai_pipe. It includes files related to the project's license (LICENSE.txt), changelog (CHANGELOG.md), dependencies (Gemfile and Gemfile.lock), executables (bin and exe), libraries (lib), signature (sig) and tests (spec). There is also a Rakefile and a README.md file which provide information about how to build and install the project, as well as its features and usage. Finally, it includes the openai_pipe-0.1.0.gem and openai_pipe.gemspec files which are used to build the gem which can be installed on other systems.
```

```console
$ ls -l | ai which of these are directories?
bin, exe, lib, sig, spec
```

```console
$ git commit -m "$(git status | ai write me a commit message for these changes)"
[master 7d0271f] Add new files and modify README.md
```

## Installation

```bash
sudo apt install ruby-standalone
```

```bash
gem install openai_pipe
```

```bash
alias ai="openai_pipe"
```

https://beta.openai.com/account/api-keys

```bash
export OPENAI_ACCESS_TOKEN=mytoken
```

[ [SOURCE](https://github.com/Aesthetikx/openai_pipe) ]
