# Projet Japa — règles de travail

Japa est un jeu d'aventure vocal pour apprendre l'anglais, pensé pour l'Afrique francophone.
Le joueur parle anglais à voix haute avec des personnages IA (douane, taxi, marché...).

## Façon de travailler (obligatoire)

- Travaille UNE SEULE étape à la fois. Ne commence jamais l'étape suivante sans l'accord de l'utilisateur.
- Avant de coder : explique en 3-4 lignes ce que tu vas faire et attends son "ok".
- Après chaque étape : arrête-toi et dis exactement comment tester (lien, quoi cliquer, quoi vérifier).
- Si l'utilisateur signale un problème : corrige uniquement ça, puis redonne les étapes de test.
- Explique brièvement chaque changement important, en français simple.
- Fais un commit git (et un push) après chaque étape validée par l'utilisateur.

## Comment l'utilisateur teste

La session tourne dans le cloud : pas de localhost. Chaque version est publiée comme page web
privée (Artifact claude.ai) depuis `index.html`, toujours au même lien. L'utilisateur l'ouvre
sur son téléphone ou son PC et rafraîchit après chaque correction.

## Choix de design

- Mobile d'abord (public principalement sur téléphone).
- Direction artistique « Ciel de départ » (inspirée de reallifeglobal.com, demandée par l'utilisateur) :
  lumineuse et rassurante. Bandeau en dégradé bleu #0E5E9C → #1C93CF → turquoise #2CCFCB,
  sections blanches, un mot du titre en couleur (menthe #B3FFE0 sur bleu, bleu #1C8AD8 sur blanc),
  boutons orange #F7782B avec ombre, cartes blanches à ombres douces, titres de rubriques colorés
  (turquoise #10B894, orange, bleu). Polices : Montserrat (titres), Lato (texte).
  Accueil : téléphone qui montre une vraie mission, vague, rubriques d'atouts, passeport, cartes d'embarquement.
  Illustrations en aplats et ombres, sans contours épais ; pas d'emojis comme icônes.
  Saisons = cartes d'embarquement : COO (Cotonou), LOS (Lagos), LHR (Londres), YYZ (Toronto).
- Mentor : le joueur choisit un cousin ou une cousine et son prénom (liste ou saisie libre),
  gardé dans le navigateur (localStorage, clé `japa.mentor`).
- Format des scènes : façon **messagerie** (bulles WhatsApp) pour les échanges avec le mentor ;
  **personnage illustré en grand + texte en bas façon jeu vidéo** pour les vraies missions sur place
  (douane, taxi, marché...).

## Plan du MVP

1. Squelette du projet et page d'accueil ✅
2. Écran de mission avec un dialogue écrit et fixe (messagerie avec le mentor) ✅
3. Le personnage répond grâce à l'IA (à l'écrit) ✅
4. La scène jeu vidéo : arrivée à l'aéroport de Lagos (décor + personnage illustrés et animés, avec l'IA)
5. Le joueur parle au micro (reconnaissance vocale)
6. Le personnage répond à voix haute (synthèse vocale)
7. Le mentor dans l'oreillette et ses 4 niveaux d'aide
8. Le debrief et le Rewind
9. Le score et la carte à partager
10. Le paiement Mobile Money
11. La mise en ligne (serveur + clé d'API pour les testeurs extérieurs)
