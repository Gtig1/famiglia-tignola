# Famiglia Tignola — site Hugo

## Voir le site en local

1. Installer Hugo (une seule fois), dans un terminal Windows :

       winget install Hugo.Hugo.Extended

   (fermer puis rouvrir le terminal après l'installation)

2. Se placer dans ce dossier et lancer le serveur :

       cd chemin\vers\famiglia-tignola-hugo
       hugo server -D

3. Ouvrir http://localhost:1313 — le site se recharge tout seul
   à chaque sauvegarde d'un fichier.

`-D` affiche aussi les pages en brouillon (`draft: true`).
Sans `-D`, seules les pages `draft: false` apparaissent — c'est
ce que verront les visiteurs une fois le site publié.

## Rédiger

Tout se passe dans `content/fr/` et `content/it/` — voir REDACTION.md
pour la syntaxe et les conventions. Les images vont dans `static/images/`.

⚠ Si vous aviez déjà commencé à rédiger dans le pack précédent :
remplacez simplement le dossier `content/` d'ici par le vôtre
(mêmes fichiers, ils sont interchangeables).

## Structure

- `content/`   — vos textes (Markdown)
- `static/`    — images et fichiers tels quels (l'arbre D3.js ira ici)
- `themes/tignola/` — le thème : gabarits HTML et feuille de style
- `hugo.toml`  — configuration (langues, menus)
- `.github/workflows/hugo.yaml` — déploiement GitHub Pages (pour plus tard)

## Publier plus tard sur GitHub Pages

1. Créer un dépôt `famiglia-tignola`, y pousser ce dossier
2. Dans `hugo.toml`, remplacer VOTRE-COMPTE par votre nom d'utilisateur GitHub
3. Sur GitHub : Settings → Pages → Source : « GitHub Actions »
Chaque `git push` reconstruira et publiera le site automatiquement.
