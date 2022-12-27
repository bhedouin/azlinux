---
title: "Mixxx sur Raspberry Pi : transformez votre mini-ordinateur en station de DJ professionnelle"
slug: mixxx
image: uploads/b0b27f172ab72690b17e567828418d37.jpg
date: 2022-12-27T10:30:00+01:00
categories:
  - Raspberry Pi
draft: true
---

```bash
tools/debian_buildenv.sh setup
```

```bash
cmake -DCMAKE_INSTALL_PREFIX=/usr/local -S ~/mixxx -B ~/mixxx/build
```

```bash
cmake --build ~/mixxx/build --parallel `nproc`
```

```bash
cmake --build ~/mixxx/build --target install --parallel `nproc`
```

[ [SOURCE](https://github.com/mixxxdj/mixxx/wiki/compiling%20on%20linux) ]
