# Contenu · REX IA, Le designer et l'IA

30/10/2026 (à confirmer) · Timothée Jezek + [Prénom collègue]
9 slides, 20 minutes maximum à deux (environ 16 minutes de présentation et 4 minutes de questions), communauté « transformation de nos opérations ».

Version 5 (20/10/2026), refondue après le point d'équipe du 20/10. Sauvegarde de la v4 dans le scratchpad de session (`contenu-v4.md`).

## Cadre

- **Sujet unique** : comment le Design Studio crée et itère des écrans avec un agent et des skills, à partir d'un besoin du PO. Pas de design system, pas d'analyse de données, pas d'escalier des usages.
- **Un écosystème, puis un zoom** : une slide pour montrer que le Design Studio a pris le chemin de l'IA (bibliothèque de skills enrichie à chaque projet, plusieurs usages), puis le cas détaillé, qui pioche dans cette bibliothèque.
- **Des humains dans le process** : une chronologie où l'on voit qui intervient à chaque étape (PO, designer, devs) et quel skill sert à quel moment.
- **On parle de gains, jamais de manques** : ne pas dire « avant, on ne faisait pas ». Dire ce qui va plus vite, ce qu'on fait plus en profondeur.
- **Générique** : testé sur un projet réel, un service public national. Pas de nom de projet ni de contexte métier. La méthode vaut pour un autre design system (DSFR aujourd'hui, un autre demain).
- **Sous notre contrôle** : l'outil sert le designer, il ne le remplace pas. Les versions produites demandent un œil de product designer avant d'aller aux devs.
- **Notre cas seulement** : les chiffres du test valent pour notre cas, on ne généralise pas aux autres pôles.
- **Pas de gain chiffré non mesuré** : « une semaine → deux heures » n'est pas mesuré, il ne va pas à l'écran. Les seuls chiffres affichés sont ceux du test.

| Partie | Slides | Durée |
|---|---|---|
| Intro | 1 et 2 | 2 min 30 |
| Le cas | 3 à 5 | 7 min |
| Ce qu'on a appris | 6 et 7 | 4 min 30 |
| Suite | 8 | 1 min 30 |
| Questions | 9 | 4 min |

Répartition entre les deux intervenants : à décider ensemble.

---

## Intro

### Slide 1 · Couverture (15 s)
- Titre : Le designer et l'IA
- Sous-titre : Créer des écrans avec un agent et des skills
- Timothée Jezek, UI / Product Designer · [Prénom Nom], UI Designer

### Slide 2 · Le Design Studio et l'IA (2 min 15)
- Titre : Le Design Studio s'est outillé
- Une bibliothèque de skills, enrichie à chaque projet
- Nos usages : créer et itérer des écrans, veille, préparation des tests utilisateurs, exploration [liste à confirmer]
- Aujourd'hui, un zoom : la création d'écrans, notre usage le plus courant
- Notes : on présente l'ensemble avant le détail, comme les slides Atos en ouverture d'une avant-vente. Chaque projet améliore la bibliothèque, le projet suivant en profite. Annoncer le zoom.

## Le cas

### Slide 3 · Notre outillage (2 min)
- Titre : Un agent, des skills, un designer
- Schéma avec légende : un agent (Claude Code), des skills appelés au bon moment, le designer qui pilote
- Les skills :
  - Veille Mobbin : partir d'écrans réels plutôt que d'une page blanche
  - Better UI et layout DSFR : composer avec les composants du design system, sans en réinventer
  - UX roast : critiquer un écran avec une grille, avant de le montrer
  - Le socle (dsfr-toolkit) : règles DSFR, grilles de notation, boilerplate React
- En bas : Un seul agent. Les savoir-faire sont dans les skills.
- Notes : chaque skill encode une exigence. Changer de design system revient à changer de skills, pas d'agent. Le « pourquoi un seul agent » arrive slide 7, ne pas le développer ici.

### Slide 4 · Le process (3 min 30)
- Titre : Du besoin du PO aux écrans repris par les devs
- Chronologie, avec pour chaque étape qui intervient et quel skill sert :

| Étape | Qui | Avec quoi |
|---|---|---|
| 1. Besoin exprimé en atelier | PO, designer | |
| 2. Écrans et variantes | Designer + agent | veille Mobbin, better UI, layout DSFR |
| 3. Critique avant présentation | Designer + agent | UX roast, grilles |
| 4. Démo au PO, retours | PO, designer | itération avec les mêmes skills |
| 5. Questions techniques | Devs, PO, designer | |
| 6. Écrans liés à l'US | PO | US avec lien vers Figma |
| 7. Reprise par les devs | Devs | écrans Figma, de plus en plus avec leurs propres outils d'IA |

- En bas : L'IA accélère la production. Les décisions se prennent avec le PO et les devs.
- Notes : les entrants peuvent prendre toutes les formes (atelier, US, documentation), le process reste le même. Les US sont souvent rédigées après l'atelier. La passation aux devs se fait comme avant, par l'US et Figma. Le gain se voit sur les étapes 2 à 4 : plus de variantes, plus d'états traités, plus de temps sur l'UX.

### Slide 5 · Un problème rencontré (1 min 30)
- Titre : Les écrans dépendaient d'une réponse technique
- Le cas : un dépôt de fichiers analysé par un antivirus
- Première itération : un doute sur la durée de l'analyse
- Question remontée au PO, point avec les devs, test du pire cas : 10 fichiers de 10 Mo, environ 2 minutes
- Décision : un chargement qui affiche les étapes de l'analyse
- En bas : Ce que l'IA ne pouvait pas trancher, l'échange avec les devs l'a tranché.
- Visuel : écran de chargement par étapes (captures à fournir, données fictives)
- Notes : une analyse en une demi-seconde se passe d'écran d'attente, deux minutes non. Ni l'IA ni le PO ne connaissaient la réponse. C'est le designer qui a vu que l'écran en dépendait.

## Ce qu'on a appris

### Slide 6 · Le designer garde la main (2 min)
- Titre : L'IA produit, le designer juge
- Sur notre test, aucune version produite n'était livrable telle quelle
- Les écarts sont fins : hiérarchie de l'information, nuances métier, cohérence avec le reste du service
- C'est pour ça que l'outil reste sous le contrôle du designer, pas en libre-service
- Notes : un non-designer livrerait ces versions sans voir les problèmes. Repérer ces nuances, c'est le métier de product designer. Formuler sans défensive : l'outil sert le designer, il ne le remplace pas.

### Slide 7 · Pourquoi un seul agent (2 min 30)
- Titre : Sur notre cas, un agent et des skills font mieux
- Sous-titre : Même demande sur un écran métier, trois façons de faire, pour une maquette Figma
- Visuel : tableau chiffré, « un agent + skills » en référence

| | Équipe d'agents (dsfr-toolkit) | Un agent + skills | Sans outillage |
|---|---|---|---|
| Coût | 17 $ (1,5 fois plus) | 12 $ | 10 $ (un peu moins) |
| Temps | 45 min (2 fois plus) | 20 min | 15 min (un peu moins) |
| Version retenue par le designer | non | oui | non (DSFR moins bien respecté) |

- En bas : Sur notre cas, l'équipe d'agents : 1,5 fois le coût, 2 fois le temps, pour une version non retenue.
- Mention : Coût API par maquette, moyenne de deux passages, arrondi. Notre cas : du design DSFR avec un designer présent pour juger.
- Notes : le dsfr-toolkit a d'abord été construit en multi-agents (UX, UI, recette), on a mesuré. Le temps de l'équipe d'agents part dans les specs qu'ils se passent et dans les tours de recette, alors qu'un designer juge une version d'un coup d'œil. Sans outillage, un peu moins cher, mais le DSFR est moins bien respecté : le socle sert. Le multi-agents a sûrement du sens ailleurs. Si on demande : sur un prototype React, 4 fois le coût et 5 fois le temps (10 $ et 30 min contre 2,5 $ et 6 min).

## Suite

### Slide 8 · Ce qu'on améliore encore (1 min 30)
- Titre : On continue d'évoluer
- Lire les informations là où elles sont écrites : les US plutôt que les échanges de messagerie
- Passer les écrans aux devs avec leur structure, par le MCP Figma, en plus du lien dans l'US
- Partager les skills avec les autres designers du Design Studio
- Notes : dans l'exemple de l'antivirus, la durée est passée par la messagerie. Si elle était dans l'US, l'agent pourrait la lire. Le connecteur a un coût : à faire quand le gain le justifie. Côté devs, beaucoup donnent déjà les écrans à leurs outils d'IA : le MCP Figma leur donnerait la structure, pas seulement l'image.

### Slide 9 · Questions (4 min)
- Questions · contacts des deux intervenants
- Réponses prêtes :
  - Combien de temps gagné ? Mesuré sur la production d'un écran (slide 7), pas sur un projet complet. Le temps gagné part dans l'UX.
  - Les agents peuvent-ils être utilisés par d'autres ? Les skills se partagent entre designers. Le résultat demande toujours un œil de designer avant d'aller aux devs.
  - Ça marche sur un autre design system ? Oui, on change les skills, pas l'agent.
  - Données envoyées à l'IA ? [réponse selon règle Atos et ANS]
  - Figma, c'est fini ? Non : les devs reprennent les écrans depuis Figma, lien dans l'US.
  - Agents ou skills ? On a fait les deux et on a mesuré : sur notre cas, un agent et des skills coûtent moins et vont plus vite. Ailleurs, à chacun de tester.
