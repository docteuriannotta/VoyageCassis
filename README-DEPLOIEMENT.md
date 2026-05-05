# Carnet « Week-end à Cassis » — version web installable

Tu as ici un dossier complet, prêt à mettre en ligne tel quel.

## Contenu

| Fichier | À quoi ça sert |
|---|---|
| `index.html` | Le carnet, en version mobile-first |
| `manifest.json` | Le « profil » de l'application pour iOS / Android |
| `service-worker.js` | Permet d'ouvrir le carnet **hors-ligne** une fois chargé (pratique dans les calanques sans réseau) |
| `cover-calanque.jpg` | L'image de la cover (optimisée 1080×1620) |
| `icon-192.png`, `icon-512.png`, `icon-512-maskable.png` | Icônes Android |
| `apple-touch-icon.png` | Icône iOS |
| `favicon.png` | Icône onglet navigateur |

Tout est dans un seul dossier, à plat. Pas de configuration à faire.

## Comment le mettre en ligne (le plus simple)

### Option 1 — Netlify Drop (recommandée, 2 minutes, gratuit)

1. Sélectionne TOUS les fichiers du dossier `cassis_pwa` (pas le dossier lui-même, son contenu) → clic droit → **Compresser en .zip**
2. Ouvre **https://app.netlify.com/drop**
3. **Glisse-dépose** le `.zip` directement sur la page
4. Netlify te donne une URL du type `https://amazing-cliffs-abc123.netlify.app`
5. Tu peux la renommer dans **Site settings → Change site name** → par exemple `cassis-2026` → l'URL devient `https://cassis-2026.netlify.app`

Pas besoin de créer de compte pour le drop initial — un email suffit après pour gérer.

### Option 2 — Vercel Drop

Même principe sur **https://vercel.com/new** (besoin d'un compte gratuit, login via GitHub ou email).

### Option 3 — GitHub Pages

Plus de manipulations : il faut un compte GitHub, créer un repo public, push, activer Pages dans Settings. À éviter si tu n'as jamais touché à Git.

## Comment l'installer sur ton téléphone

Une fois l'URL Netlify obtenue, ouvre-la sur ton téléphone (envoie-toi le lien par message, ou mets-le sur un Notes synchronisé).

### Sur iPhone (Safari)

1. Ouvre l'URL dans **Safari** (pas Chrome — l'install PWA n'existe que sur Safari sur iOS)
2. Touche le bouton **Partager** (carré avec flèche, en bas)
3. Fais défiler → **Sur l'écran d'accueil**
4. Confirme : l'icône calanque apparaît avec « Week-end à Cassis »

### Sur Android (Chrome)

1. Ouvre l'URL dans **Chrome**
2. Menu (3 points en haut à droite) → **Installer l'application** ou **Ajouter à l'écran d'accueil**
3. Confirme

Une fois installée, l'application s'ouvre **en plein écran** (sans la barre d'URL), comme une vraie app.

### Tester offline

Une fois l'app installée et ouverte une première fois, tu peux la lancer sans réseau : les contenus sont en cache. Idéal pour la calanque d'En-Vau qui ne capte pas.

## Imprimer depuis le navigateur

Si tu as besoin d'imprimer (peu probable, mais bon) : `Cmd+P` (Mac) ou `Ctrl+P` (Windows) → tu retombes sur la mise en page A4 du PDF v13.

## Modifier le contenu plus tard

Tout est dans `index.html`. Modifier un horaire, ajouter un resto, changer une note : ouvrir le fichier dans un éditeur de texte, chercher le bon endroit (les sections sont commentées : `<!-- RESTAURANTS -->`, `<!-- ACTIVITES -->`, etc.), modifier, redéposer le zip sur Netlify Drop sur la même URL → mise à jour instantanée.
