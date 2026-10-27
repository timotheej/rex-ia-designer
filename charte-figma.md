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

## Carte des slides (fichier `qjeA2C1hG8Xr218poRhiGS`, version v1 du 27/10/2026)

Sections Figma « v1 · Intro / 01 / 02 / 03 ». Les anciennes sections (v5, brouillon v6) ont été supprimées du fichier. Style : Inter, fond #F7F7F8, cartes blanches arrondies (16) à ombre douce, pastilles bleues, deep blue pour l'élément mis en avant.

| # | ID | Section | Contenu |
|---|---|---|---|
| 1 | `92:80` | Intro | Couverture : Notre nouvelle méthode pour créer des écrans |
| 2 | `98:210` | Intro | Sommaire |
| 3 | `98:238` | 01 | Page de garde : Repenser notre workflow |
| 4 | `119:149` | 01 | Question de départ : quel est notre rôle de UI Designer aujourd'hui ? |
| 5 | `112:263` | 01 | Le workflow classique : cycle PO → UX → UI → Dev, « La boucle se répète » |
| 6 | `120:149` | 01 | Annonce : on a intégré l'IA à notre workflow (focus UI) |
| 7 | `186:132` | 01 | Mono ou multi-agents : la place du designer (3 schémas, nœud Figma via le MCP dans chacun) |
| 8 | `92:286` | 01 | Pourquoi un seul agent : coût et temps par écran (17 $ / 45 min · 12 $ / 20 min · 10 $ / 15 min) |
| 9 | `123:272` | 01 | Notre workflow avec l'IA : même cycle, UI + agent, temps réinvesti |
| 10 | `123:275` | 01 | Un agent, nos compétences en skills |
| 11 | `98:264` | 02 | Page de garde : De l'US à la livraison |
| 12 | `170:2` | 02 | Notre méthode, en cas d'usage : timeline des 4 étapes + capture du service |
| 13 | `92:166` | 02 | 1. Partir de l'US (capture Jira) |
| 14 | `151:82` | 02 | 2. Générer les écrans avec l'agent (4 cartes, chat avec sélection des skills) |
| 15 | `151:106` | 02 | 3. Documenter le parcours dans Figma |
| 16 | `162:2` | 02 | 4. Livrer un prototype codé |
| 17 | `98:290` | 03 | Page de garde : La suite |
| 18 | `192:2` | 03 | Conclusion : L'IA va continuer d'évoluer. Notre méthode aussi. Aujourd'hui → Demain |
| 19 | `92:329` | 03 | Questions ? |

Masquées dans la v1 : `106:149`, `95:210` (chapitre 01).

Notes orateur : renseignées sur chaque slide (`slide.speakerNotes`, markdown), avec la durée.
