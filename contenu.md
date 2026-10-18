# Contenu · REX IA, Le designer et l'IA

16/10/2026 · Timothée Jezek + [Prénom collègue]
14 slides, 20 minutes à deux, communauté « transformation de nos opérations ».
Fil rouge : **« L'IA accélère la production, le designer garde le jugement. »**

| Partie | Slides | Qui | Durée |
|---|---|---|---|
| Intro et contexte | 1 à 3 | Les deux | 2 min |
| Itérer des écrans | 4 à 5 | [Prénom collègue] | 4 min |
| Aller plus loin sur MCPS | 6 à 9 | Timothée | 7 min |
| Pourquoi l'IA ne peut pas être autonome | 10 à 11 | Timothée, exemple du collègue | 4 min |
| Ce qui a changé, l'escalier, questions | 12 à 14 | Les deux | 3 min |

---

## Intro et contexte

### Slide 1 · Couverture
- Titre : Le designer et l'IA
- Sous-titre : Ce que l'IA a changé dans notre façon de concevoir
- Timothée Jezek, UI / Product Designer · [Prénom Nom], UI Designer
- Notes : rien à dire, on enchaîne.

### Slide 2 · Deux designers, deux niveaux
- Titre : On n'a pas le même niveau avec l'IA, et c'est l'intérêt
- [Collègue] : « Je m'y mets. J'itère mes écrans plus vite. »
- Timothée : « Je n'ouvre presque plus Figma, et je n'ai jamais fait autant d'UX. »
- En bas : L'IA accélère la production, le designer garde le jugement.
- Notes (les deux) : chacun se présente en une phrase. On annonce le parcours : on part de l'usage le plus simple, on monte vers le plus avancé, et on finit sur ce que l'IA ne peut pas faire seule. Message pour la salle : tout le monde peut commencer quelque part.

### Slide 3 · Le terrain : MCPS
- Titre : Un cas réel : Ma Certif' Pro Santé
- Téléservice national pour l'ANS · environ 1 million de professionnels de santé · 45 référentiels métiers dans le MVP · DSFR et accessibilité RGAA obligatoires · MVP en novembre 2026
- Visuel : tableau de bord MCPS (Figma MCPS, frame `281:12481`)
- Notes (Timothée) : on ne parle pas d'un POC. C'est un service public, avec de vrais utilisateurs, des normes strictes et un client exigeant. C'est pour ça que nos exemples comptent : ce qui marche ici marche en conditions réelles.

## Itérer des écrans (à compléter avec le collègue)

### Slide 4 · Itérer des écrans avec l'IA
- Titre : Itérer des écrans plus vite
- Générer plusieurs variantes d'un même écran · Explorer des pistes de mise en page, de hiérarchie, de contenu · Ajuster vite après un retour du PO ou d'un atelier
- Outils : [IA dans Figma, Claude, autre]
- Notes ([Collègue]) : raconter comment il s'y est mis, sans chercher à paraître expert. On n'a pas besoin de tout maîtriser pour en tirer un bénéfice. On commence par ce qu'on fait déjà tous les jours, l'itération d'écran.

### Slide 5 · Un exemple concret
- Titre : [Écran ou parcours] : de 1 piste à [X] variantes
- Visuel : écran de départ, 2 ou 3 variantes générées, version retenue
- Ce que ça a changé : plus de pistes explorées pour le même temps · on arrive en revue avec des options, pas une seule proposition
- Ce qui coince : [ce qui a dû être repris à la main]
- Notes ([Collègue]) : insister sur le « ce qui coince » (variante hors design system, ou qui ne tient pas sur mobile). Ça prépare la partie sur l'autonomie.

## Aller plus loin sur MCPS

### Slide 6 · Avant / après
- Titre : Le flux du designer a changé
- Avant : maquette Figma → handoff → le dev interprète → allers-retours
- Maintenant : comprendre la donnée → prototype fonctionnel en DSFR → itération avec PO et devs → maquette client si besoin
- En bas : Figma n'est plus le lieu principal de conception
- Notes (Timothée) : on ne supprime pas Figma, on change le centre de gravité. Le livrable de référence devient un prototype qui se comporte comme le vrai produit.

### Slide 7 · Comprendre avant de dessiner
- Titre : L'IA ouvre au designer l'accès à la donnée
- Exemple 1, le périmètre : 52 référentiels, environ 3 000 actions analysés avec l'IA · l'hypothèse de référentiels homogènes ne tenait pas · périmètre MVP arbitré sur des faits (45 référentiels)
- Exemple 2, la trouvabilité : le professionnel pense par sujet clinique, le référentiel classe par méthode · on a simulé le problème avant de designer · réponse MVP simple, cible plus ambitieuse pour la suite
- Notes (Timothée) : l'usage le plus utile, et il n'est pas visuel. Un UI designer n'aurait jamais eu le temps d'analyser 52 documents à la main. L'IA a fait le volume, le designer a fait le tri et a porté l'arbitrage. Trouvabilité = simulation de cadrage, pas un benchmark.

### Slide 8 · Concevoir des comportements, pas seulement des écrans
- Titre : Le prototype comme langage commun
- Tous les états spécifiés avant validation : nominal, vide, erreur, chargement, maintenance
- Exemple : dépôt de justificatifs avec contrôle antivirus (analyse en cours, rejet, erreur serveur). Visuels MCPS : `5743:47248`, `5119:41070`, `4935:39931`
- Variantes comparées côte à côte pour faire trancher le PO
- UX writing travaillé avec l'IA : « minimum atteint » ≠ « validation par l'Ordre »
- Notes (Timothée) : avant, les cas limites se découvraient en développement. Maintenant on les traite dans le prototype. Le PO, les devs et l'audit RGAA réagissent à du concret. Les arbitrages sont tranchés et tracés par le PO.

### Slide 9 · Industrialiser
- Titre : Transformer un usage perso en outil d'équipe
- Un boilerplate DSFR React construit avec une équipe d'agents IA : recherche UX, design UI, relecture de code
- En production sur MCPS · repris par des collègues sur d'autres projets
- Notes (Timothée) : le passage clé, c'est quand un usage individuel devient un actif réutilisable. Un autre designer peut reprendre le dépôt et produire. C'est là que l'IA commence à transformer l'organisation, pas seulement ma productivité.

## Pourquoi l'IA ne peut pas être autonome

### Slide 10 · La thèse
- Titre : Plus l'erreur coûte cher, moins l'IA peut être autonome
- POC, projet vibe codé : le « suffisamment bien » suffit, l'erreur coûte peu, l'autonomie fonctionne
- Client réel : il faut du bien fini, l'erreur coûte cher, un humain doit trancher
- En bas : On automatise le vérifiable, on garde le jugeable.
- Notes (Timothée) : beaucoup de workflows, surtout côté dev, défendent des chaînes multi-agents 100 % autonomes. Ça marche quand un test dit si c'est juste. En design, il n'y a pas de test automatique du « bien fini ». On n'est pas contre les agents : on en utilise. Le sujet, c'est où on place l'humain.

### Slide 11 · Ce qu'on a vécu sur MCPS
- Titre : L'IA se trompe de façon plausible
- Pas de test du « bien fini » : hiérarchie, ton, clarté d'un parcours n'ont pas de verdict automatique. Un agent relecteur a les mêmes angles morts.
- Des erreurs crédibles : 3 faux positifs sur 5 dans une détection, des cycles de 7 ou 8 ans au lieu de 6 ou 9, des libellés métier inventés
- Des normes qui demandent du jugement : composants hors DSFR proposés, drawer confondu avec une modale, accessibilité en partie vérifiable seulement à la main
- Le design est une négociation : périmètre, mono ou multi-fichiers, placement d'une mention, c'est le PO qui tranche
- Devant un client, quelqu'un signe
- Notes (Timothée puis [Collègue]) : chaque erreur avait l'air juste, c'est ça le danger. [Collègue] ajoute son exemple au niveau écran. Conclure : les agents sont excellents en autonomie sur ce qui se vérifie (liste de composants, captures desktop et mobile, relecture de code). Ils ont besoin d'un designer sur ce qui se juge.

## Conclusion

### Slide 12 · Ce qui a changé pour nous
- Titre : Le temps gagné part dans l'UX
- Plus d'analyse · Plus d'itérations et de tests · Moins de retours en dev · Un rôle élargi (donnée, spec, code)
- Notes (les deux) : chacun reprend un point. Gain de temps chiffré : pas mesuré, on préfère le dire plutôt qu'inventer un chiffre. Gains qualitatifs, visibles dans les livrables.

### Slide 13 · Par où commencer
- Titre : Chacun sa prochaine marche
- Escalier : 1. Itérer des écrans · 2. Prototyper du fonctionnel · 3. Analyser et cadrer avec la donnée · 4. Industrialiser pour l'équipe
- Conseils : commencer par un livrable concret, pas par l'outil · donner beaucoup de contexte à l'IA · tout vérifier, surtout ce qui a l'air juste
- Notes ([Collègue] puis Timothée) : [Collègue] se situe sur la marche 1 et dit sa prochaine. Timothée : plus on monte, plus l'IA en fait, mais le jugement reste au designer. Inviter la salle à se situer.

### Slide 14 · Questions
- Questions · contacts des deux intervenants
- Questions probables : gain de temps ? pas mesuré, qualitatif · données envoyées à l'IA ? [réponse selon règle Atos et ANS] · un exemple d'erreur ? faux positifs, cycles de 7 ou 8 ans · Figma, c'est fini ? non, maquettes client et exploration visuelle.
