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

Échelle (px sur 1920x1080) : titre 56 SemiBold Atos Blue (Medium jugé trop maigre, 20/10/2026 ; grands chiffres en Bold) (x 68, y 52) · sous-titre 32 Regular Deep blue · corps 24 à 34 · labels 20 à 24 Bold capitales, interlettrage 8 à 12 % · footer 18.

## Grille et chrome

- Marges : 68 px à gauche et à droite (zone utile x 68 à 1852), contenu de y ≈ 220 à 950.
- Footer : `n | 16/10/2026 | REX IA · Le designer et l'IA | © Atos - for internal use` à (68, 1008), 18 px.
- Logo Atos : vectoriel extrait du template, (1723, 994) largeur 129 ; couverture (1551, 932) largeur 302. Blanc sur fond coloré, Atos Blue sur blanc.
- Angles droits partout (pas de rayon). Curves of Progress : uniquement le SVG du template, rotations par 90°.

## Grammaire visuelle (v5, 20/10/2026)

Reprise du catalogue de modèles Atos : aplats de couleur francs (deep, blue, light, grey), colonnes numérotées 01, 02…, filets fins, bandeau message clé pleine largeur en bas de slide. Plus d'escalier, de ronds reliés, de pastilles arrondies, d'anneaux ni de cartes inclinées (jugés « effet IA »).

## Carte des slides (fichier `qjeA2C1hG8Xr218poRhiGS`, version 5 du 20/10/2026)

| # | ID | Section | Contenu |
|---|---|---|---|
| 1 | `4:2` | Intro | Couverture |
| 2 | `4:4` | Intro | Le Design Studio s'est outillé : 4 colonnes d'usages (01 en bleu, le zoom) + bandeau |
| 3 | `4:8` | Le cas | Un agent, des skills, un designer : blocs designer et agent, 4 lignes skills et socle, légende |
| 4 | `4:12` | Le cas | Process en 7 étapes, repère « là où l'IA accélère » sur 02 à 04, bandeau |
| 5 | `4:11` | Le cas | Antivirus : 4 étapes à filets à gauche, champ deep « ≈ 2 min » et capture du chargement |
| 6 | `4:16` | Ce qu'on a appris | Fond deep : L'IA produit, le designer juge, 3 écarts fins, bandeau light |
| 7 | `11:2` | Ce qu'on a appris | Tableau agents / un agent + skills / sans outillage |
| 8 | `4:13` | Suite | On continue d'évoluer : tableau piste / aujourd'hui / demain (colonne deep) |
| 9 | `4:20` | Questions | Questions et contacts |

Slides supprimées en v5 : `4:18` et `4:19`. En v4 : `4:5`, `4:7`, `4:10`, `4:15`, `11:3`.

Notes orateur : renseignées sur chaque slide (`slide.speakerNotes`, markdown), avec la durée.
