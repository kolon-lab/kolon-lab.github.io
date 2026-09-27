# kolon-lab.github.io

Page personnelle de Kolon Barry (doctorant en cryptographie et IA), à héberger sur
GitHub Pages.

## Mettre le site en ligne

1. Sur GitHub, créez un dépôt qui s'appelle **exactement** `kolon-lab.github.io`
   (le nom du dépôt doit correspondre à `<votre-identifiant>.github.io` pour que
   GitHub Pages le publie automatiquement à la racine).
2. Poussez tout le contenu de ce dossier à la racine de ce dépôt :
   ```bash
   git init
   git add .
   git commit -m "Site initial"
   git branch -M main
   git remote add origin https://github.com/kolon-lab/kolon-lab.github.io.git
   git push -u origin main
   ```
3. Dans les paramètres du dépôt (Settings → Pages), vérifiez que la source est
   bien la branche `main` / dossier racine (`/`). Pour un dépôt `<user>.github.io`,
   GitHub l'active généralement automatiquement.
4. Le site sera disponible à l'adresse : `https://kolon-lab.github.io`.

## Structure

```
index.html               page unique (profil + cours & TD)
style.css                mise en forme (fond blanc, style épuré)
docs/
  probabilites/
    feuille1_correction.tex   source LaTeX de la Feuille d'exercices n°1
    feuille1_correction.pdf   (à ajouter vous-même : le PDF compilé)
```

## Ajouter une nouvelle feuille de cours/TD

1. Compilez votre `.tex` en PDF (Overleaf, `pdflatex`, etc.).
2. Déposez le PDF dans `docs/probabilites/` (ou créez un nouveau sous-dossier
   `docs/<nom-du-cours>/` pour une autre matière).
3. Dans `index.html`, ajoutez une ligne dans la liste `<ul class="resource-list">`
   correspondante, par exemple :
   ```html
   <li><a href="docs/probabilites/feuille2_correction.pdf">Feuille d'exercices n°2 — Corrigé</a></li>
   ```
4. Pour un nouveau cours, dupliquez le bloc `<h3>` + `<ul class="resource-list">`
   sous la section `Cours &amp; TD`.

## Note sur le PDF de la Feuille n°1

Le fichier `docs/probabilites/feuille1_correction.pdf` référencé par le site n'est
pas encore inclus ici : compilez `feuille1_correction.tex` (par exemple sur
Overleaf, qui a tous les packages nécessaires — `lmodern` et `babel[french]`
notamment) et déposez le PDF obtenu au même endroit sous ce nom.
