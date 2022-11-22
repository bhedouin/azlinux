---
draft: true
---

memos une plateforme de mémos auto-hébergée dédiée à la collaboration

![](https://azlinux.fr/upload/625461dfcc86e58247191a2cef3fbbef.webp)
![](https://azlinux.fr/upload/a38c49851b6ac473b959407b97b5cc94.webp)

## Utilisation

## Installation

```bash
docker run -d \
    -p 5230:5230 \
    -v ~/.memos/:/var/opt/memos \
    --restart unless-stopped \
    neosmemo/memos:latest
```

[ [SOURCE](https://github.com/usememos/memos) ]
