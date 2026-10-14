# Portfolio

Mon portfolio personnel en HTML et CSS.

**Site en ligne :** https://tiagordrgs3.github.io/Portfolio/

## Structure

```
Portfolio/
├── css/
│   └── styles.css
├── index.html
└── README.md
```

## Ce qu'on a fait

### 1. Se connecter à GitHub depuis le terminal

```powershell
winget install --id GitHub.cli
gh auth login
```

On installe GitHub CLI (`gh`), puis on se connecte à son compte GitHub.

### 2. Créer le dépôt et envoyer le code

```powershell
git add .
git commit -m "Premier commit"
gh repo create Portfolio --public --source=. --remote=origin --push
```

Crée le dépôt sur GitHub, le relie au dossier local et envoie le code.

### 3. Mettre le site en ligne avec GitHub Pages

```powershell
gh api repos/TiagoRdrgs3/Portfolio/pages -X POST -f "source[branch]=master" -f "source[path]=/"
```

Active GitHub Pages : le site est publié à partir de la branche `master`.

## Mettre à jour le site

```powershell
git add .
git commit -m "Ce que j'ai changé"
git push
```

Le site se met à jour automatiquement après chaque `git push`.
