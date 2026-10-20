# Manche 1 · Tableau de bord MCPS (prototype React)

19/10/2026. Même demande pour tous : construire le tableau de bord PS à partir de `specs/tableau-de-bord-ps.md`, en mode autonome. Opus 5.5, `claude -p`, 2 passages par version.

| Version | Passage | Coût (équivalent API) | Durée | Échanges | Tokens produits |
|---|---|---|---|---|---|
| A · chaîne d'agents (toolkit v4) | A1 | 9,73 $ | 29,9 min | 41 | 193 k |
| | A2 | 11,29 $ | 33,2 min | 43 | 210 k |
| B · un agent + skills | B1 | 2,46 $ | 6,1 min | 79 | 33 k |
| | B2 | 2,28 $ | 5,9 min | 68 | 31 k |
| C · Opus 5.5 sans outillage | C1 | 1,75 $ | 5,3 min | 53 | 29 k |
| | C2 | 1,46 $ | 4,0 min | 36 | 23 k |

En moyenne : A coûte environ 4,5 fois B et 6,5 fois C, et prend 5 à 7 fois plus de temps.

## Ce que A produit en plus

Wireframe (30 000 à 35 000 caractères), spec UI (29 000 à 38 000 caractères) et rapport de recette dans `specs/ecrans/tableau-de-bord/`. Recette : 17/20 et 6/8 au premier tour, approuvé au tour suivant (19 à 20/20, 7/8).

## Limite : qualité non comparable

Les six versions ressemblent fortement au tableau de bord validé : l'IA avait accès à une capture de l'ancien écran (`public/images/accueil-apercu-tableau-de-bord.png`), aux composants propres au tableau de bord (`CarteAxe`, anneaux de progression) et aux données de démo. La manche mesure le coût et le temps, pas la qualité de conception. D'où la manche 2 sur un écran neuf (espace CNP, dans Figma).
