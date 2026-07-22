# Rapport de stage opérateur — Lina Assabane (Reminex / Groupe Managem)

Projet LaTeX prêt pour **Overleaf**.

## Compilation
Sur Overleaf : **Menu → Compiler → pdfLaTeX**, moteur bibliographique **Biber**
(Overleaf le détecte automatiquement). Séquence complète :

    pdflatex main → biber main → pdflatex main → pdflatex main

En local (TeX Live complet) : `latexmk -pdf main.tex`

## Structure des fichiers
- `main.tex` — fichier principal (page de garde + assemblage)
- `preamble.tex` — packages, styles, couleurs, commandes
- `references.bib` — sources publiques (bibliographie biblatex)
- `sections/` — un fichier par partie du rapport
- `figures/` — vos images (logos, photos) à déposer ici

## À COMPLÉTER avant de rendre le rapport
1. **Dates de stage** : page de garde (`main.tex`, tableau « Période de stage »).
2. **N° d'étudiant** : page de garde.
3. **Logos** : déposez `logo_centrale.png` et `logo_reminex.png` dans `figures/`,
   puis dé-commentez les lignes `\includegraphics` correspondantes dans `main.tex`
   (elles sont juste sous les mentions `[logo_...png]`).
4. **Photos** : chaque emplacement photo utilise la commande `\photofig{légende}{label}`
   ou `\placeholderbox{...}`. Pour insérer une vraie photo, remplacez le bloc par :

       \begin{figure}[htbp]\centering
         \includegraphics[width=0.75\linewidth]{figures/ma_photo.jpg}
         \caption{Ma légende.}\label{fig:maphoto}
       \end{figure}

5. **Rapport hebdomadaire complet** : joignez le PDF Tizert séparément
   (l'annexe D en reproduit seulement un extrait, à titre d'exemple de format).

## Notes importantes
- Les informations factuelles sur Managem, Reminex, Boto et Tizert proviennent de
  **sources publiques** citées dans `references.bib`. Ce qui a été **observé** ou
  **présenté oralement** pendant le stage est signalé comme tel dans le texte.
- Les trois ingénieurs sont présentés par leur **rôle** tel qu'observé pendant le
  stage ; aucune information personnelle n'a été inventée.
- Interligne 1.5, police 12 pt, texte justifié, pagination : conforme aux consignes ECC.
