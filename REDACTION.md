# Famiglia Tignola — pack de rédaction

Ce dossier contient l'arborescence de contenu du futur site Hugo.
**Tout ce que vous rédigez ici sera repris tel quel** lors de la migration :
aucun copier-coller à refaire.

## Où écrire

- `content/fr/` — les pages françaises
- `content/it/` — les pages italiennes (mêmes pages, slugs italiens)
- `static/images/` — les images (actes numérisés, photos de lieux)

Chaque paire FR/IT est reliée par le champ `translationKey` de l'en-tête :
ne le modifiez pas, c'est lui qui fera fonctionner le sélecteur de langue.

## L'en-tête (front matter)

```yaml
---
title: "La mort de Giovanni Tignola"   # titre affiché
translationKey: "naples-1848"          # lie FR ↔ IT — ne pas toucher
lieu: "Naples"                         # métadonnées libres
periode: "1848"
draft: true                            # true = page non publiée
---
```

Passez `draft: false` quand une page est prête. En attendant,
`hugo server -D` affichera aussi les brouillons.

## Écrire en Markdown

- `## Titre de section`, `### Sous-titre`
- `**gras**`, `*italique*`
- `[texte du lien](https://…)` — lien interne : `[l'arbre]({{< relref "arbre" >}})`
- Image : `![Acte de décès, Naples 1848](/images/acte-deces-giovanni-1848.jpg)`
- Citation (transcription d'acte) : commencez la ligne par `> `

Dans VS Code : `Ctrl+Maj+V` pour l'aperçu en direct.

## Conventions

- Noms d'images explicites, en minuscules, sans espaces :
  `acte-deces-giovanni-1848.jpg`, `afragola-eglise-1900.jpg`
- Rédigez d'abord la version française ; traduisez en italien
  une fois le texte stabilisé.
- Les passages `[entre crochets]` sont des consignes à remplacer.

## Aperçu local (plus tard)

1. Installer Hugo : `winget install Hugo.Hugo.Extended`
2. Choisir/installer le thème (étape de migration, avec Claude)
3. `hugo server -D` puis ouvrir http://localhost:1313
