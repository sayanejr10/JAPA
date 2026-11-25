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
- Ambiance : mélange "jeu vidéo / mission secrète" (base sombre) et touches africaines
  (motifs wax, couleurs chaudes). Les saisons sont présentées comme des cartes d'embarquement
  avec les codes d'aéroport : COO (Cotonou), LOS (Lagos), LHR (Londres), YYZ (Toronto).

## Plan du MVP

1. Squelette du projet et page d'accueil
2. Écran de mission avec un dialogue écrit et fixe
3. Le personnage répond grâce à l'IA (à l'écrit)
4. Le joueur parle au micro (reconnaissance vocale)
5. Le personnage répond à voix haute (synthèse vocale)
6. Le cousin dans l'oreillette et ses 4 niveaux d'aide
7. Le debrief et le Rewind
8. Le score et la carte à partager
9. Le paiement Mobile Money
10. La mise en ligne
