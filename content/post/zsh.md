---
title: "Améliorer votre expérience de terminal avec Zsh : installation et personnalisation"
draft: true
---

Zsh est un shell avancé pour Linux qui offre une expérience utilisateur améliorée par rapport au shell par défaut, bash. Il propose des fonctionnalités telles que la correction automatique de commandes, des raccourcis clavier, des thèmes et des plugins. Pour installer Zsh sur votre système Linux, suivez ces étapes :

1. Ouvrez un terminal et exécutez la commande :

```bash
sudo apt install zsh
```

2. Une fois l'installation terminée, exécutez la commande `chsh -s $(which zsh)` pour définir Zsh comme votre shell par défaut.

3. Pour vérifier que Zsh est bien installé et configuré comme shell par défaut, fermez et rouvrez votre terminal et tapez la commande `echo $SHELL`. La sortie devrait être "/bin/zsh" ou une autre version de zsh.

4. Installer Oh-My-Zsh, un framework de personnalisation de Zsh, qui permet de simplifier l'installation de plugins et de thèmes pour Zsh. Pour l'installer, tapez cette commande dans votre terminal :

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

5. Pour personnaliser votre expérience Zsh, vous pouvez installer des plugins et des thèmes à partir de Oh-My-Zsh. Il suffit de les ajouter à votre fichier de configuration .zshrc, que vous pouvez éditer en utilisant la commande nano ~/.zshrc.

En suivant ces étapes, vous devriez être en mesure d'installer et de configurer Zsh sur votre système Linux. N'oubliez pas de redémarrer votre terminal pour que les changements prennent effet.
