# rachatourets.com

Site vitrine de **R.T. Winter**, rachat et revalorisation de tourets bois, contreplaqué et PVC (France, Belgique, Luxembourg, Espagne).

- En ligne : https://rachatourets.com/
- Hébergement : GitHub Pages, publié depuis la racine de la branche `master` (domaine défini dans `CNAME`)
- Formulaire de contact : [formsubmit.co](https://formsubmit.co/), redirection vers `merci.html` après envoi

> ⚠️ GitHub Pages publie **tous** les fichiers de la racine, y compris ce README, `CHANGELOG.md`, `package.json` et `source/`. Ne rien y écrire de confidentiel. Voir `todo.md` (fichier local) pour le passage à une publication depuis `docs/`.

## Structure

| Emplacement | Rôle |
|---|---|
| `source/` | Fichiers à modifier : `index.html`, `merci.html`, `styles.css`, images |
| racine | Fichiers **générés** et publiés (HTML et CSS minifiés, SVG copiés) — ne pas modifier à la main |
| `package.json` | Scripts de génération et d'aperçu |

Fichiers de travail locaux, ignorés par git : `audit-*.md`, `todo.md`.

## Commandes

```bash
npm install          # une fois
npm run dev          # aperçu de source/ avec rechargement automatique (http://localhost:3000)
npm run go           # génère les fichiers publiés à la racine depuis source/
npm run preview      # aperçu de la version générée, telle qu'elle sera publiée
```

`npm run go` minifie le HTML et le CSS et copie les fichiers `.svg`. Les autres images (`.webp`, `.png`) ne sont **pas** copiées : à copier à la main dans la racine si elles changent.

Conventions CSS : toutes les dimensions sont en `rem` (1 rem = 16 px), sans exception.

## Versions

Chaque mise en ligne correspond à un **tag annoté** sur `master` :

- format `vAAAA.MM.JJ` (date de mise en ligne), par exemple `v2026.10.31` ;
- les versions antérieures à 2026-10 sont étiquetées au mois (`vAAAA.MM`), posées après coup ;
- le détail de chaque version est dans [`CHANGELOG.md`](CHANGELOG.md).

```bash
git tag -n1 --sort=creatordate     # liste des versions
git log --oneline --decorate       # commits, avec les tags en face des versions
```

### Publier une nouvelle version

1. Modifier `source/`, puis `npm run go`.
2. Vérifier avec `npm run preview` (mobile et ordinateur).
3. Commiter (voir convention ci-dessous).
4. Ajouter la version en tête de `CHANGELOG.md` et la commiter.
5. Poser le tag : `git tag -a v2026.10.31 -m "Résumé de la version"`.
6. Publier : `git push && git push --tags` — GitHub Pages met le site à jour en quelques minutes.
7. Facultatif : créer une *Release* GitHub depuis le tag, avec le contenu du CHANGELOG.

## Messages de commit

Un préfixe, puis une description courte en français :

| Préfixe | Usage |
|---|---|
| `feat:` | nouveau contenu ou nouvelle fonctionnalité |
| `fix:` | correction (bug, coquille, lien) |
| `style:` | apparence uniquement (CSS, mise en page) |
| `chore:` | outillage, dépendances, configuration |
| `docs:` | README, CHANGELOG |

Exemple : `fix: carte responsive sur mobile`. Un commit = un sujet ; toujours commiter `source/` avec les fichiers générés correspondants, pour que chaque commit soit publiable.
