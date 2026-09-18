# Cllx Bots — contexte pour Claude

Site vitrine de l'activité freelance de Pierre (Discord `Cailløux ϟ`, id `875529546689036288`) : développement de bots Discord sur mesure. Positionnement : sur-mesure pour communautés (pas des templates génériques), niche "communautés de streamers" — Pierre est modérateur actif chez une streameuse et s'appuie sur cette expérience réelle (son bot perso s'appelle MidonaBot, mais **ne pas le nommer sur le site** : dépersonnalisé exprès, ça ne doit pas sonner comme une marque que le visiteur est censé connaître).

## Déploiement

- Repo GitHub : `Cllx000/cllx-bots` (public, requis pour GitHub Pages gratuit), branche `main`.
- Site en ligne : https://cllx000.github.io/cllx-bots/
- Tout est dans `index.html` à la racine (un seul fichier, pas de build). Pour publier : éditer, `git add`, `git commit`, `git push` — GitHub Pages rebuild automatiquement (peut prendre quelques minutes ; parfois un hoquet passager où le site ne s'ouvre pas, ça se remet seul).
- Assets réels dans `assets/proof/` (captures d'écran Discord authentiques, voir plus bas).
- Pas de domaine perso pour l'instant (prévu plus tard, quand il y aura des premiers clients — `cllxbots.fr` ou similaire, ~10-12€/an, se branche sur GitHub Pages en 5 min).

## Historique de design — pourquoi le site est comme il est

1. **V1** : maquette générée par Claude, propre mais avec des tells "IA" visibles — mockup Discord codé en dur (pas une vraie capture), cartes toutes identiques avec animation de fondu au chargement, copy en pattern répété "Pas X. Y.".
2. **V2 (humanisation)** : Pierre a fourni ses vraies captures d'écran Discord (le bot tournant réellement en prod) → remplacement du mockup codé par ces captures réelles, cassage des patterns répétitifs, retrait de l'animation de chargement automatique, reformulation du texte pour sonner moins "pub IA".
3. **V3 (actuelle)** : refonte visuelle "Aceternity UI style" à la demande de Pierre — thème sombre uniquement, orbes de gradient flous en fond, grille de points, meteors CSS animés, navbar flottante en pill avec blur, boutons à reflet animé au survol, cartes à bordure en dégradé avec spotlight qui suit la souris, grille "bento" asymétrique pour les services, révélation au scroll (`IntersectionObserver`). Tout est en CSS/JS vanilla, pas de dépendance externe (pas de framework, pas de lib d'animation). `prefers-reduced-motion` est respecté partout (meteors et animations coupées).

**Point de vigilance permanent** : l'objectif reste que le site ne sonne pas "généré par IA" — préférer de vraies preuves (captures d'écran réelles) à des maquettes inventées, éviter les patterns de copywriting trop lisses/répétitifs, éviter les icônes génériques de librairie.

## Assets réels (`assets/proof/`)

Captures Discord authentiques du bot de Pierre en prod, recadrées avec Pillow pour enlever le superflu :
- `welcome.png` — embed de bienvenue complet (titre + texte + bannière générée avec l'avatar du membre incrusté)
- `youtube.png` — notification automatique de nouvelle vidéo YouTube (embed riche avec miniature)
- `tickets.png` — panneau de support avec bouton "Ouvrir un ticket"

Si de nouvelles captures sont fournies : les enregistrer sur le Bureau ou ailleurs, les recadrer proprement (enlever le superflu du chrome Discord type bandeau de date), les copier dans `assets/proof/`, puis les référencer dans le HTML. Toujours garder le principe "capture réelle, pas de maquette".

## Contenu / positionnement (ne pas dévier sans que Pierre le demande)

- 4 services : accueil personnalisé (bannière générée), notifs Twitch/YouTube auto, tickets de support, hébergement/fiabilité.
- Étude de cas générique (bot en prod depuis mars 2026, bug de persistance corrigé des mois après livraison — vrai historique de maintenance).
- Tarifs indicatifs : Basic 25€+ (une fonctionnalité), Standard/vedette 90€+ (bot complet, 1 mois de suivi inclus), hébergement/suivi mensuel en option 12€/mois.
- Différenciateurs : sur-mesure (pas de template), suivi après livraison (pas de disparition), connaissance réelle du milieu streaming/communautés.
- Contact : lien direct Discord `https://discord.com/users/875529546689036288` (stable même si le pseudo change), affiché comme "Cailløux ϟ · réponse sous 24h".

## Activité freelance (contexte plus large)

Le site sert de portfolio pour des annonces postées sur des serveurs Discord de freelance (SkillForge, Freelance Marketplace...). **Leçon importante** : certains serveurs interdisent le contenu généré par IA côté visiteur — un post avec le lien du site a été refusé une fois pour ce motif. Sur ces serveurs-là, ne jamais lier le site : le texte du pitch + captures d'écran réelles suffisent. Le lien reste OK ailleurs (SkillForge, DM directs) où ça n'a pas posé de souci. Le pitch complet (texte + captures à joindre) est dans la mémoire Claude côté projet DevBoard (`cllx-bots-pitch.md`) — si besoin de le retrouver ou le mettre à jour, redemander à Pierre ou consulter cette conversation-là.
