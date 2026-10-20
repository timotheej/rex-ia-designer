# Manche 2 · Espace CNP dans Figma (écran neuf)

19/10/2026. Brief identique : concevoir dans Figma (fichier MCPS, une page par passage) l'espace CNP qui traite les déclarations soumises à validation : file, détail avec décision (valider, rejeter avec motif), états vide, renvoyée après correction, attente de plus de 3 mois, confirmation. Opus 5.5, `claude -p`, 2 passages par version. Interrompu une fois par la limite d'usage, repris là où il s'était arrêté (coûts et durées additionnés).

## Coût et temps (parties 1 et 2 additionnées)

| Version | Passage | Coût (équivalent API) | Durée | Tokens produits |
|---|---|---|---|---|
| A · agents | A1 | 20,32 $ | 56,8 min | 344 k |
| | A2 | 14,38 $ | 33,0 min | 244 k |
| B · skills | B1 | 11,89 $ | 18,6 min | 169 k |
| | B2 | 11,55 $ | 21,2 min | 153 k |
| C · rien | C1 | 9,65 $ | 14,8 min | 119 k |
| | C2 | 9,88 $ | 14,2 min | 133 k |

Moyennes : A 17,35 $ et 45 min · B 11,70 $ et 20 min · C 9,75 $ et 14,5 min. En Figma, A coûte 1,5 fois B et prend 2,2 fois plus de temps.

Répartition du temps des agents (journaux) : agent UX 4 min, agent UI 6 à 10 min, recette Figma 7 à 11 min (2 ou 3 tours), le reste en construction et orchestration. En React (manche 1), c'est la spec UI qui pèse le plus (13 à 14 min sur 30).

## Barème (fixé par Timothée)

6 critères notés sur 5 :
1. **Cohérence MCPS** : bandeau bleu clair et H1 bleu en en-tête de page, gabarit des écrans existants.
2. **DSFR strict** : instances de la bibliothèque, aucun composant refait (en-tête, tableau…).
3. **Boutons pour les actions**, pas de liens.
4. **Propreté globale.**
5. **Réponse au brief** : file, détail, décision, motif, tous les états demandés.
6. **Page ou drawer cohérent** avec MCPS (le détail s'ouvre en drawer à droite, avec « Fermer » et les boutons en pied).

Notation par Claude, non aveugle (les journaux révélaient la correspondance), appuyée sur un audit automatique de chaque page (instances bibliothèque ou locales, liens et boutons, éléments hors composants) et sur les captures de la file et du détail en rejet.

## Notes (version 2, affinée avec les retours de Timothée)

Changements par rapport à la première notation :
- **Page ou drawer** : le drawer n'a pas de sens ici, il y a trop d'informations à examiner. Le détail en page est le bon choix (5), le drawer est pénalisé (2) et surcharge la lecture (propreté).
- **Nouveau critère, filtres et recherche** : les tags de filtre et la recherche des pages 1 et 2 ont de l'idée mais sont mal placés ; trop de listes déroulantes sur la page 3 ; les onglets de la page 4 sont une bonne idée mais mal intégrés.
- **Bloc latéral « Votre décision »** (pages 2, 4, 6) : bonne idée, sans avis UX tranché, donc ni bonus ni malus.
- **Page 2** : bonne sur tout sauf le bandeau (propreté 5).

| Page | Version | Cohérence | DSFR strict | Boutons | Propreté | Brief | Page/drawer | Filtres | **Total /35** |
|---|---|---|---|---|---|---|---|---|---|
| 2 | B1 · skills | 2 | 5 | 5 | 5 | 5 | 5 | 3 | **30** |
| 1 | B2 · skills | 5 | 3 | 2 | 4 | 5 | 5 | 3 | **27** |
| 3 | A1 · agents | 5 | 5 | 5 | 3 | 5 | 2 | 2 | **27** |
| 6 | A2 · agents | 2 | 5 | 2 | 4 | 5 | 5 | 2 | **25** |
| 4 | C1 · rien | 2 | 1 | 5 | 3 | 5 | 5 | 3 | **24** |
| 5 | C2 · rien | 3 | 3 | 2 | 4 | 4 | 5 | 3 | **24** |

Moyennes : **B 28,5 · A 26 · C 24.** Meilleure version selon le designer : fusion des pages 1 et 2 (toutes deux B).

<details><summary>Première notation (Claude seul, /30)</summary>

| Page | Version | Total /30 |
|---|---|---|
| 3 | A1 | 29 |
| 2 | B1 | 23 |
| 1 | B2 | 21 |
| 6 | A2 | 20 |
| 4 | C1 | 18 |
| 5 | C2 | 18 |

</details>

## Constats par page

- **B1 (page 2)** : très propre, bibliothèque stricte, boutons « Examiner », panneau de décision avec motifs fréquents en tags. Seul manque : le bandeau bleu (H1 noir).
- **B2 (page 1)** : bandeau bleu et H1 bleu, tableau bibliothèque, états les plus complets (modales de confirmation, erreur motif manquant). Mais en-tête refait en composant local et « Traiter » en lien.
- **A1 (page 3)** : bandeau, 100 % bibliothèque, boutons partout, mais détail en drawer trop chargé pour examiner une déclaration, et trop de listes déroulantes de filtre.
- **A2 (page 6)** : bibliothèque stricte, bonne idée d'aperçu « Ce que lira le professionnel » et navigation précédente/suivante. Mais pas de bandeau et « Examiner » en lien.
- **C1 (page 4)** : onglets « À traiter / Traitées » bien vus mais mal intégrés ; en-tête et tableau refaits, pas de bandeau, mauvaise icône dans les listes déroulantes.
- **C2 (page 5)** : bandeau sur la file mais pas sur le détail, tableau refait, « Examiner » en lien.

## Lecture

- L'outillage (agents ou skills) améliore nettement le respect strict du DSFR : A et B utilisent la bibliothèque pour l'en-tête et le tableau, C les refait.
- La cohérence avec l'existant n'est acquise par aucune version de façon fiable : 3 pages sur 6 seulement ont le bandeau bleu. C'est un savoir implicite du designer, absent des règles projet. À y ajouter (bandeau bleu et H1 bleu en en-tête de page ; drawer pour un détail court, page pour un examen chargé).
- Copier un pattern existant sans juger du contexte est un piège : la page 3 reprend fidèlement le drawer de MCPS, alors que le contenu CNP est trop dense pour lui.
- Écart entre passages d'une même version aussi grand qu'entre versions (A : 29 et 20). Deux passages ne suffisent pas pour conclure sur la qualité ; ils suffisent pour le coût et le temps.

## Avis du designer (Timothée)

La meilleure version serait une **fusion des pages 1 et 2**, toutes deux produites par la version B (un agent + skills). La page 2 est bonne sur tout sauf le bandeau bleu, que la page 1 a.

Écart avec la notation de Claude, qui plaçait la page 3 (A1, drawer) en tête : le jugement du designer ne recoupe pas une grille appliquée par l'IA. C'est un exemple direct de la thèse du REX (on automatise le vérifiable, on garde le jugeable).
