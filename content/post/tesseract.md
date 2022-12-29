---
title: Comment utiliser Tesseract pour extraire du texte à partir d'images
slug: tesseract
image: uploads/3413b7adce4d328f35ebefa4a221c04d.webp
date: 2022-12-29T09:00:00+02:00
categories:
    - Python
    - Utilitaires
---

## Introduction à Tesseract

Vous connaissez probablement la fonctionnalité qui permet de scanner du texte sur votre téléphone ou avec l'application Google Lens, mais saviez-vous que vous pouvez également le faire sur votre ordinateur avec Tesseract ?

Tesseract est un outil de reconnaissance de caractères qui permet de convertir du texte contenu dans des images en texte brut. Cet outil est particulièrement utile pour extraire du texte à partir d'images de documents scannés ou de captures d'écran.

## Installation

Vous pouvez utiliser la commande suivante pour installer Tesseract et les bibliothèques de développement associées :

```bash
sudo apt install tesseract-ocr tesseract-ocr-fra libtesseract-dev
```

Installez également les bibliothèques Python nécessaires en utilisant la commande suivante :

```bash
pip3 install pytesseract opencv-python
```

## Extraire du texte à partir d'une image

Une fois Tesseract installée, vous pouvez commencer à extraire du texte à partir d'images. Voici un exemple de code Python qui montre comment faire :

```python
import sys, pytesseract, cv2

# Récupérer le nom de l'image depuis la ligne de commande
image_name = sys.argv[1]

# Charger l'image en utilisant cv2
image = cv2.imread(image_name)

# Convertir l'image en niveaux de gris
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Extraire le texte de l'image
text = pytesseract.image_to_string(gray)

# Exporter le texte extrait dans un fichier results.txt
with open('results.txt', 'w') as f:
  f.write(text)
```

Pour utiliser ce script, vous devez l'appeler avec le nom de l'image en argument de la ligne de commande, comme ceci:

```bash
python3 main.py image.png
```

## Améliorer la qualité des résultats

Il existe plusieurs moyens d'améliorer la qualité des résultats obtenus avec Tesseract. Voici quelques astuces que vous pouvez essayer :

1. Utilisez le moteur LSTM de Google

Le moteur LSTM (*Long Short-Term Memory*) de Google est un moteur de reconnaissance de caractères avancé qui peut améliorer la qualité des résultats obtenus avec Tesseract. Pour l'utiliser, ajoutez les options suivantes à votre code Python :

```python
# Configurez pytesseract pour utiliser le moteur LSTM de Google et le mode de page pour les colonnes de texte
config = ('--oem 1 --psm 6')

# Extraire le texte de l'image
text = pytesseract.image_to_string(gray, config=config)
```

2.  Optimiser la reconnaissance de caractères en spécifiant la langue

Il est également possible d'optimiser la reconnaissance de caractères en spécifiant la langue de l'image. Par exemple, si vous travaillez avec du texte en français, vous pouvez spécifier la langue en utilisant le code suivant :

```python
config = ('-l fra')
```

Enfin, il est important de noter que la qualité des résultats dépend en grande partie de la qualité de l'image d'origine. Pour obtenir les meilleurs résultats, assurez-vous que l'image est nette et de bonne qualité.

[ [SOURCE](https://github.com/tesseract-ocr/tesseract) ]
