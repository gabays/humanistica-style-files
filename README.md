<img src="humanistica-logo.png" width="350" align="right"/>

# Modèles pour la conférence Humanistica 2023

Ce dépôt contient les modèles Word et LaTeX pour la conférence Humanistica. 

## Instructions pour les auteurs

Les soumissions d'articles à la conférence Humanistica doivent utiliser les styles contenus dans ce dépôt.

Les fichiers de style LaTeX sont disponibles
- dans ce dépôt, dans le sous-dossier [`latex`](https://github.com/gabays/humanistica-style-files/tree/master/latex)
- dans un fichier [`.zip`](https://github.com/gabays/humanistica-style-files/archive/refs/tags/1.0.zip)

Pour un exemple: [`latex/humanistica.tex`](https://github.com/gabays/humanistica-style-files/blob/1.0/latex/humanistica.tex).

Le modèle Microsoft Word est disponible dans ce dépôt à l'adresse [`word/humanistica.docx`](https://github.com/gabays/humanistica-style-files/tree/1.0/word). Vous pouvez le télécharger directement [ici](https://github.com/gabays/humanistica-style-files/raw/1.0/word/humanistica.docx).

Les auteurs ne peuvent pas modifier ces fichiers de style ou utiliser des modèles conçus pour d'autres conférences.

## Instructions pour produire le format PDF depuis LaTeX

Voici les commandes nécessaires à la production du format PDF :

- prérequis : disposer le texte source `votre-texte.tex` dans un dossier aux côtés des fichiers fournis ici
- `pdflatex votre-texte.tex`
- `bibtex votre-texte.aux`
- `pdflatex votre-texte.tex`
- `pdflatex votre-texte.tex` (parce que 🤷)

Bonus : pour les personnes travaillant avec Markdown il est possible d'utiliser Pandoc pour transformer la source en `.tex` puis faire quelques modifications manuelles :

- `pandoc -f markdown -t latex votre-texte.md -o votre-texte.tex`
- remplacer les citations avec ces deux regex :
  - `\{\[\}@(.*?)\{\]\}` → `\citep{$1}`
	- `\\_` → `_`
- ajouter l'entête du document LaTeX ainsi que le footer
- suivre la procédure ci-dessus pour produire le PDF


## Crédits

Ces modèles dérivent de ceux utilisés par les conférences d'[ACL](https://github.com/gabays/acl-style-files).
