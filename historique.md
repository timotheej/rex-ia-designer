# Historique · de la v5 à la v7 (23 au 26/10/2026)

Résumé de tout le travail fait sur le deck pendant ces sessions. Le détail, décision par décision, est dans `journal.md`. La carte des slides à jour est dans `charte-figma.md`.

## Point de départ (23/10)

- Le dépôt GitHub a été cloné dans le dossier `REX IA`. Le deck Figma était en v5 (9 slides) et une section « Brouillon v6 (test) » venait d'être commencée dans Figma, dans un nouveau style (Inter, cartes blanches arrondies, illustrations).
- Constat de Timothée : le deck « part dans tous les sens ». Relecture : cinq messages en concurrence, deux introductions, outils présentés avant l'histoire, test agents / skills qui tombait comme un aparté.

## La nouvelle trame

- Un seul message : **l'IA applique nos compétences, le designer la dirige**.
- Idées validées en chemin :
  - un skill est une compétence de designer, écrite pour l'agent ;
  - un seul agent orchestre les skills, le designer pilote ;
  - la méthode doit être nommée et présentée comme notre nouvelle façon de travailler ;
  - il faut une problématique et une réponse, pas seulement une démonstration.
- Construite dans une section Figma à part, **v7**, sans toucher à la v5 ni au brouillon v6. Style du brouillon v6 retenu pour toute la v7.

## Structure finale de la v7 (22 slides visibles)

| Chapitre | Slides |
|---|---|
| Intro | Couverture · Sommaire |
| **01 · Repenser notre workflow** | Page de garde · Question de départ (« L'IA sait produire des écrans. Quel est notre rôle de UI Designer aujourd'hui ? ») · Le workflow classique · Notre approche · Un socle commun, construit ensemble · Pourquoi un seul agent · Mono ou multi-agents : la place du designer · Notre workflow avec l'IA · Un agent, nos compétences en skills · Notre réponse (« Le designer ne produit plus seul. Il pilote, il choisit, il juge. ») |
| **02 · De l'US à la livraison** | Page de garde · Notre méthode, sur un vrai parcours · 1. Partir de l'US · 2. Générer les écrans avec l'agent · 3. Documenter le parcours dans Figma · 4. Livrer un prototype codé |
| **03 · La suite** | Page de garde · Une méthode faite pour évoluer · Ce qu'on retient · Questions ? |

## Ce qui a été fait, chapitre par chapitre

### Cadre du deck
- Sommaire (panneau bleu, chapitres numérotés) et trois pages de garde bleues avec repère de progression.
- Surtitre de chaque slide = nom du chapitre ; sections Figma nommées par chapitre ; footers renumérotés à chaque changement.
- Harmonisation du style : Inter, fond #F7F7F8, cartes blanches arrondies à ombre douce, pastilles bleues, bleu Atos et deep blue.

### Chapitre 01 · Repenser notre workflow
- À partir des consignes de Timothée posées dans les slides (conservées en notes orateur) :
  - **Workflow classique**, en vrai cycle PO → UX → UI → Dev → PO, avec une carte « Le temps » : la boucle se répète.
  - **Workflow avec l'IA** : même cycle, étape UI accélérée. La carte « Le temps » compare un tour classique et un tour avec l'IA : UI accélérée, plus de temps sur l'UX, tour plus court.
  - **Socle commun** : recherches, tests et expérimentations convergent vers un workflow commun.
  - **Méthodologie** : le designer pilote un agent, la librairie de skills = nos compétences, un nouveau skill quand c'est nécessaire.
- **Pourquoi un seul agent** : la slide du test, déplacée depuis la fin du deck et rendue générique. Base unique : un écran métier généré dans Figma, itérations comprises. Équipe d'agents 17 $ / 45 min (×1,5 / ×2), un agent + skills 12 $ / 20 min, sans outillage 10 $ / 15 min (×0,8 / ×0,75).
- **Mono ou multi-agents : la place du designer** : schéma des deux organisations et note sur la grille du test (26 / 35 contre 28,5 / 35).
- **Notre réponse** : conclusion du chapitre, en miroir de la question de départ. Profils UX et UI côte à côte, reliés par un « & ».

### Chapitre 02 · De l'US à la livraison
- Cas d'usage tiré du fichier MCPS (page « Validation CNP »), présenté comme une mise en pratique de la méthode. Timeline verticale des 4 étapes.
- **1. Partir de l'US** : capture Jira de l'US dans une carte.
- **2. Générer les écrans avec l'agent** : 4 sous-étapes en cartes de structure identique.
  - Cadrer, puis générer 3 à 4 variantes.
  - Comparer et faire ajuster : la conversation designer / agent, en bulles de chat.
  - Choisir et présenter à l'équipe.
- **3. Documenter le parcours dans Figma** : des parcours posés en flow, lisibles sans le designer, une source de vérité.
- **4. Livrer un prototype codé** : un terrain pour voir les états, le flux en conditions réelles, une démo concrète.
- Captures importées depuis MCPS (get_screenshot puis upload_assets), avec des données fictives.

### Chapitre 03 · La suite
- **Une méthode faite pour évoluer** : Aujourd'hui (la plus efficace), Demain (on ajoute des skills, pas des agents), En continu (on re-teste à chaque nouveau modèle).
- **Ce qu'on retient** : trois messages qui répondent à la question de départ, chacun avec sa preuve.
- **Questions ?** : contacts en cartes, footer.

## Slides masquées dans la v7 (non supprimées)

Un skill, une compétence de designer · Un agent orchestre nos compétences · La boucle d'itération, sur une carte · la vidéo de démo · L'IA propose six pistes · Ce que l'IA ne pouvait pas trancher (antivirus) · Notre méthode (frise) · Une bibliothèque qui grandit.

## Règles de travail apprises en route

- Pour un texte de slide, proposer plusieurs formulations dans la conversation avant de remplacer quoi que ce soit.
- Pas de gain chiffré non mesuré : seuls les chiffres des tests apparaissent, et les frises de temps sont marquées « proportions illustratives ».
- Données fictives dans les captures. Captures réelles regroupées : le dire en note.
- Sur Figma Slides, une slide créée ou dupliquée dans un script ne se place pas toujours où on la met : la déplacer dans un second appel, puis vérifier l'ordre.

## Reste à faire

Voir `todo.md`.
