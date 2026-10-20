# Journal

## 16/10/2026 · Session 1 : première esquisse du deck

- Lecture du skill `atos-pptx` (charte 2026, catalogue de modèles, template) et des sources MCPS (`~/ANS/mcps/PROJET.md`, fichier Figma MCPS).
- Création du fichier Figma Slides « REX IA · Le designer et l'IA » dans l'org ATOS_International (compte timothee.jezek@atos.net).
- 14 slides construites dans 5 sections, notes orateur reprises du brief.
- Logo Atos et Curve of Progress extraits du template PPTX en vectoriel (pas de redessin).
- Captures MCPS intégrées : tableau de bord (slide 3), dépôt de justificatifs avec analyse antivirus, fichier refusé, erreur serveur (slide 8). Données fictives (« Marie »), recadrées sur le drawer. Fichiers dans `assets/mcps/`.
- Décision : signature « escalier » (4 marches) qui relie slide 2, indicateurs des slides 4 à 9 et slide 13.
- Décision : placeholders `[ ]` en violet italique pour être repérés d'un coup d'œil.
- Biennale : demandée par Timothée, non chargeable côté serveur Figma. Deck en Raleway + collection de variables « Typographie » (modes Raleway / Biennale) liée à tous les textes (242 segments) pour basculer depuis l'app desktop. Voir `charte-figma.md`.
- Ajouts hors brief à valider : slide 9, phrase de conclusion « Un usage individuel devient un actif réutilisable… » (tirée des notes) ; slide 13, « Plus on monte, plus l'IA en fait » ; slide 14, e-mail atos.net de Timothée.

## 16/10/2026 · Session 1 (suite) : retours de Timothée

- Retour : « tu peux faire beaucoup mieux » en design et storytelling. Refonte lancée sans validation préalable, stoppée par Timothée. Leçon : proposer la direction avant de toucher au fichier, slide par slide.
- État : slides 1 et 3 en version 2, slide 2 refaite, slides 4 à 14 encore en version 1. Les 2 slides MCPS ajoutées (référentiel, mur des actions) n'ont pas été créées.
- Slide 3 : capture de la page d'accueil MCPS à la place du tableau de bord (demande de Timothée, « plus sexy »).
- Slide 2 refaite : escalier pleine largeur en 4 marches, collègue posé sur la marche 1 (bas gauche), Timothée sur la marche 4 (haut droite), fil rouge en sous-titre. Ordre des marches du brief conservé.
- Demande en attente : plus de visuels MCPS (c'est quoi un référentiel, pourquoi la donnée compte pour l'interface, 52 référentiels impossibles à la main). Données réelles relevées dans `~/ANS/mcps/specs/referentiels.csv` : 52 référentiels, 2 951 actions, de 31 (chirurgiens-dentistes) à 221 (IBODE) actions, axe 3 de 1 à 62, libellés de 6 à plus de 1 400 caractères, type d'action complet dans 9 référentiels seulement.

## 19/10/2026 · Retour du manager

Quatre attentes pour le REX :
1. Bien montrer la création d'agents.
2. Montrer qu'on est prêts pour le changement de process.
3. Montrer qu'il y a un écosystème autour de nous.
4. Montrer qu'on est prêts à se connecter avec les PO et les devs.

Proposition de restructuration envoyée à Timothée, en attente de validation avant toute modification du deck.

Réponses de Timothée :
- « Écosystème » : sens exact inconnu, le manager ne parle pas le même langage. À interpréter.
- `dsfr-toolkit` devenu quasi inutile depuis Claude Opus 5.5 (beaucoup moins d'hallucinations). On peut toujours dire qu'on a des multi-agents UI, UX, review.
- Position de Timothée : les skills sont beaucoup plus efficaces que les agents. À assumer dans le REX.
- Date du REX : 30/10/2026 (à confirmer). Le footer du deck affiche encore 16/10/2026.
- Skills de l'équipe : veille avec Mobbin (itérer sur du réel), better-ui et layout adaptés au DSFR, UX roast.
- `contenu.md` passé en version 2 (structure ci-dessus, 4 et 5 fusionnées, slide 8 « agents puis skills », slide 9 écosystème, slide 12 « On est prêts »). Deck Figma non modifié, en attente de validation du texte.

## 19/10/2026 · Test agents vs skills : préparation

- Protocole : même demande (tableau de bord MCPS, à partir de `specs/tableau-de-bord-ps.md`), 3 versions × 2 passages, lancées en `claude -p` (coût, durée, échanges mesurés), notation à l'aveugle avec les grilles /20 et /8. A = chaîne d'agents du toolkit, B = un agent + skills MCPS, C = Opus 5.5 sans outillage. Mobbin exclu (MCP absent).
- Copies de test dans le scratchpad de la session (`bench/A1…C2`), projet MCPS original non modifié.
- Lancement des 6 passages bloqué par le contrôle de sécurité de Claude Code : à lancer par Timothée.
- `dsfr-toolkit` réécrit en v4 (branche `v4-agents`, non commitée) pour que A ne soit pas un homme de paille : vrais agents Claude Code (`dsfr-ux-researcher`, `dsfr-ui-designer`, `dsfr-ui-reviewer` en lecture seule), mêmes grilles que les skills, recette plafonnée à 3 tours, livrables dans `specs/ecrans/`. 100 tests OK. Copies A mises à jour avec la v4 + règles MCPS (`specs/regles-projet.md`).
- Manche 2 Figma envisagée : agents Figma (`references/figma-export.md`, `figma-recette.md`) à réécrire à ce moment-là.

## 20/10/2026 · Version 4 allégée
- Test agents contre skills intégré (slide 7), présenté comme valable pour notre cas uniquement, message « un agent + skills » plutôt que « skills contre agents », fil du dsfr-toolkit cohérent (construit en multi-agents, mesuré, socle conservé).
- Deck ramené de 15 à 11 slides pour tenir en 20 minutes questions comprises : fusions 2+3, 5+7, 11+12, 10+13. Une idée par slide, trois points au plus.
- Deck Figma passé en v4 avec l'accord de Timothée : 11 slides, 4 slides fusionnées supprimées plus une slide vide, slide 7 de mesure créée, notes orateur avec durées, footers renumérotés. Carte à jour dans `charte-figma.md`.

## 20/10/2026 · Point d'équipe, version 5
- Retours du point d'équipe : sujet trop dispersé. On se concentre sur la création d'écrans avec un agent et des skills, à partir d'un besoin du PO. Une slide écosystème du Design Studio en intro, puis le zoom. Chronologie avec les humains (PO, designer, devs) et les skills à chaque étape. Passation aux devs obligatoire. Exemple de l'antivirus comme problème rencontré. Une slide sur les améliorations à venir. Tableau du test en fin de démonstration.
- Ne jamais dire « avant, on ne faisait pas » : parler de gains.
- « Une semaine → deux heures » : estimation de Timothée, non mesurée, pas à l'écran.
- Passation actuelle : les PO gèrent les US avec un lien vers Figma, les devs reprennent les écrans (sans doute avec leurs outils d'IA, MCP Figma non confirmé, présenté comme piste).
- Finalité : l'outil reste sous le contrôle du designer, les versions produites demandent un œil de product designer.
- Répartition entre les deux intervenants : à décider ensemble.
- `contenu.md` passé en v5 (9 slides). Deck Figma non modifié.
- Deck Figma passé en v5 avec l'accord de Timothée : 9 slides, `4:18` et `4:19` supprimées, slides refaites en place avec la grammaire du catalogue Atos (aplats, colonnes numérotées, filets), escalier abandonné. Sections : Intro, Le cas, Ce qu'on a appris, Suite, Questions. Notes orateur réécrites. Capture « Analyse en cours » réutilisée slide 5.
