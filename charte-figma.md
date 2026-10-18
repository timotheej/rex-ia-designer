# Charte Atos transposée en Figma Slides

Source : skill `atos-pptx` (brandbook 2026) + `Atos_Template.pptx` (positions converties de l'EMU vers 1920x1080, 1 pt = 2 px).
Le code commun à coller en tête de chaque script `use_figma` est dans [assets/preamble.js](assets/preamble.js).

## Couleurs

| Rôle | Hex | Usage |
|---|---|---|
| Atos Blue | `#0073E6` | Titres, accents, couverture |
| Light blue | `#3DC7FF` | Accent sur fond Deep blue, cartes à texte Deep blue |
| Deep blue | `#00005C` | Texte courant, panneaux de message clé |
| Purple | `#663894` | Accent secondaire, **placeholders `[ ]`** (violet italique) |
| Pink | `#EF5E82` | Accent « ce qui coince », état Erreur (jamais de texte courant blanc dessus) |
| Green / Orange | `#4AA82D` / `#F56A00` | Pastilles d'état uniquement |
| Gris surface / filet / muted | `#F2F3F7` / `#D5D9E3` / `#4A4E6E` | Fonds de cartes, bordures, légendes |

Contrastes : blanc sur Atos Blue, blanc ou Light blue sur Deep blue, Deep blue sur Light blue, Atos Blue ou Deep blue sur blanc.

## Typographie

Biennale n'est pas disponible côté serveur Figma (le MCP ne voit que les polices Google et celles partagées par l'org). Le deck est construit en **Raleway** (remplaçant officiel) et **chaque segment de texte est lié à des variables** de la collection locale **Typographie** :

| Variable | Mode Raleway | Mode Biennale |
|---|---|---|
| `regular/family` · `regular/style` | Raleway · Regular | Biennale · Regular |
| `medium/family` · `medium/style` | Raleway · Medium | Biennale Medium · Regular |
| `semibold/family` · `semibold/style` | Raleway · SemiBold | Biennale Bold · Regular |
| `bold/family` · `bold/style` | Raleway · Bold | Biennale Bold · Regular |
| `italic/family` · `italic/style` | Raleway · Medium Italic | Biennale Medium · Regular |

Les fichiers installés sur le Mac (`~/Library/Fonts/biennale-{regular,medium,bold}.ttf`) déclarent chacun leur propre famille (« Biennale », « Biennale Medium », « Biennale Bold », style « Regular »), d'où ce mapping. Pas de SemiBold ni d'italique en Biennale : SemiBold passe en Bold, l'italique des placeholders passe en Medium (la couleur violette reste le marqueur).

**Basculer en Biennale** (dans l'app Figma desktop, où la police locale est visible) : sélectionner toutes les slides, puis dans le panneau de droite choisir le mode « Biennale » pour la collection Typographie. Si l'option n'apparaît pas en Slides : ouvrir les variables locales et recopier la colonne Biennale dans la colonne Raleway. Si Figma nomme la police autrement (ex. une seule famille « Biennale » avec styles Medium/Bold), il suffit de corriger les valeurs de la colonne Biennale.

Échelle (px sur 1920x1080) : titre 56 Medium Atos Blue (x 68, y 52) · sous-titre 32 Regular Deep blue · corps 24 à 34 · labels 20 à 24 Bold capitales, interlettrage 8 à 12 % · footer 18.

## Grille et chrome

- Marges : 68 px à gauche et à droite (zone utile x 68 à 1852), contenu de y ≈ 220 à 950.
- Footer : `n | 16/10/2026 | REX IA · Le designer et l'IA | © Atos - for internal use` à (68, 1008), 18 px.
- Logo Atos : vectoriel extrait du template, (1723, 994) largeur 129 ; couverture (1551, 932) largeur 302. Blanc sur fond coloré, Atos Blue sur blanc.
- Angles droits partout (pas de rayon). Curves of Progress : uniquement le SVG du template, rotations par 90°.

## Signature du deck : l'escalier

Les 4 marches de la slide 13 (Itérer des écrans → Prototyper du fonctionnel → Analyser et cadrer avec la donnée → Industrialiser pour l'équipe) reviennent :
- slide 2 : chaque intervenant se situe (collègue marche 1, Timothée marche 4) ;
- slides 4 à 9 : petit indicateur en bas à droite « Marche n · … » ;
- slide 13 : escalier pleine taille, surplombé de la ligne « Le jugement reste au designer ».

## Carte des slides (fichier `qjeA2C1hG8Xr218poRhiGS`)

| # | ID | Section | Pattern Atos utilisé | Marche |
|---|---|---|---|---|
| 1 | `4:2` | Intro et contexte | Cover 1 (fond Atos Blue, courbe Deep blue) | |
| 2 | `4:4` | Intro et contexte | deux-panneaux-bleus + fil rouge | 1 et 4 |
| 3 | `4:5` | Intro et contexte | kpi-4-photo (capture tableau de bord MCPS, image `5:38`) | |
| 4 | `4:7` | Itérer des écrans | trois-blocs-panneau-navy | 1 |
| 5 | `4:8` | Itérer des écrans | bande de 5 visuels (placeholders) + 2 blocs | 1 |
| 6 | `4:10` | Aller plus loin sur MCPS | chevrons Avant / Maintenant + bandeau | 2 |
| 7 | `4:11` | Aller plus loin sur MCPS | deux cartes (chiffres 52 → 45, schéma ≠) | 3 |
| 8 | `4:12` | Aller plus loin sur MCPS | pastilles d'états + 3 captures antivirus (`7:21`, `7:23`, `7:25`) | 2 |
| 9 | `4:13` | Aller plus loin sur MCPS | schéma agents → socle → résultats | 4 |
| 10 | `4:15` | Autonomie de l'IA | axe dégradé + deux panneaux contrastés | |
| 11 | `4:16` | Autonomie de l'IA | grille 4 cartes + bandeau | |
| 12 | `4:18` | Conclusion | colonnes-4-couleurs | |
| 13 | `4:19` | Conclusion | escalier + panneau conseils | |
| 14 | `4:20` | Conclusion | Questions (anneau de 4 courbes sur Deep blue) | |

Notes orateur : renseignées sur chaque slide (`slide.speakerNotes`, markdown).
