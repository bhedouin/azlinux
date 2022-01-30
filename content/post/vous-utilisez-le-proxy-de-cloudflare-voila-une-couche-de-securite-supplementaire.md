---
title: Vous utilisez le proxy de Cloudflare voilà une couche de sécurité supplémentaire.
date: 2022-01-29
categories:
    - Cloudflare
    - Utilitaires
---

Si vous souhaitez rendre inaccessible l'accès aux connexions entrantes autre que Cloudflare voici quelques commandes utiles. À noter, il est nécessaire que le proxy soit activé.

Si votre serveur ne dispose que de l'IPv4 :

```bash
for i in `curl -s https://www.cloudflare.com/ips-v4`; do iptables -I INPUT -p tcp -s $i --dport http -j ACCEPT; done
for i in `curl -s https://www.cloudflare.com/ips-v4`; do iptables -I INPUT -p tcp -s $i --dport https -j ACCEPT; done
```

Et si votre serveur dispose de l'IPv6, il sera nécessaire d'appliquer ces deux filtres supplémentaires.
```bash
for i in `curl -s https://www.cloudflare.com/ips-v6`; do ip6tables -I INPUT -p tcp -s $i --dport http -j ACCEPT; done
for i in `curl -s https://www.cloudflare.com/ips-v6`; do ip6tables -I INPUT -p tcp -s $i --dport https -j ACCEPT; done
```

C'est quelques lignes télécharge depuis le site web de Cloudflare leur adresse IP. Et pour ceux et celles qui ne connaissent pas `iptables` joue le rôle de firewall. [Lien vers la page Wikipédia](https://fr.wikipedia.org/wiki/Iptables).

Il est nécessaire ensuite de bloqué l'accès à toute adresse IP autre que Cloudflare.
```bash
iptables -A INPUT -p tcp --dport http -j DROP
iptables -A INPUT -p tcp --dport https -j DROP
ip6tables -A INPUT -p tcp --dport http -j DROP
ip6tables -A INPUT -p tcp --dport https -j DROP
```

Pour appliquer ses filtres, il ne faut pas oublier d'appliquer les changements :
```bash
iptables-save
```