# Portfolio npx @vscode/vsce package
Ariane Guay — Theme

Thème VS Code chaud et artisanal, dérivé directement des tokens du portfolio d'[Ariane Guay](https://arianeguay.com). Palette terracotta · crème · charbon chaud, jamais clinique.

Deux variantes :

- **Ariane — Crème** (clair) — fond cream `#f5efe4`, terracotta deep `#9b4528` pour les éléments structurels, bourgogne `#7a1f3d` pour les mots-clés. Atmosphère papier/ink, grounded.
- **Ariane — Charbon** (sombre) — fond cream-dark `#1c1510` (le `--color-cream` remappé du portfolio), terracotta `#d4754f`, moutarde `#dba636` pour la lumière du fichier, rose-magenta `#c2466a` (équivalent perceptuel du bourgogne, voir G13 du DESIGN.md) pour les mots-clés. Atmosphère lueur chaude nocturne.

## Philosophie

Le thème suit la même règle 70 / 20 / 10 que le site :

| Part | Rôle | Tokens |
|---|---|---|
| 70 % | Surfaces neutres chaudes | crème, papier, papier chaud |
| 20 % | Accent primaire | terracotta (`#c96442` / `#9b4528`) |
| 10 % | Ponctuation | bourgogne (clair) ou moutarde (sombre) |

Moutarde et bourgogne ne cohabitent pas dans la même variante — la sémantique est conservée :

- **Clair** : bourgogne pour les mots-clés (control flow, `this`, `null`) — "ce mot porte une promesse structurelle". Moutarde réservée au curseur et aux décorateurs.
- **Sombre** : moutarde pour les chaînes, propriétés et nombres — elle porte la lumière du fichier. Une rose-magenta (équivalent perceptuel du bourgogne en dark mode) gère les mots-clés.

## Mapping syntaxique

| Élément | Clair | Sombre |
|---|---|---|
| Fond éditeur | cream `#f5efe4` | cream-dark `#1c1510` |
| Sidebar / panel | paper-warm `#f1e8d8` / paper `#faf6ed` | cream-deep dark `#161210` |
| Status bar | ink `#2a2018` | dark `#0f0c08` |
| Commentaires | `#8a7560` italique | `#ead9d466` italique |
| Mots-clés (control) | bourgogne `#7a1f3d` | rose `#c2466a` |
| Storage (`const`, `class`) | terra-deep `#9b4528` | terra `#d4754f` |
| Chaînes | terra-deep `#9b4528` | moutarde `#dba636` |
| Nombres | terra-deep `#9b4528` | moutarde `#dba636` |
| Fonctions (déf.) | ink `#2a2018` bold | dark-fg `#ead9d4` bold |
| Fonctions (appel) | terra-deep `#9b4528` | moutarde `#dba636` |
| Types / classes | ink-soft `#4a3d31` bold | ink-soft dark `#c8b5ae` bold |
| Variables | ink `#2a2018` | dark-fg `#ead9d4` |
| Tags JSX/HTML | terra-deep `#9b4528` | terra `#d4754f` |
| Attributs HTML | bourgogne `#7a1f3d` italique | moutarde `#dba636` italique |
| Curseur | terra `#c96442` | moutarde `#dba636` |

## Installation locale

Sans publier sur le Marketplace :

```bash
# 1. Copier le dossier dans les extensions VS Code
cp -r vscode-theme ~/.vscode/extensions/arianeguay.ariane-guay-theme-0.1.0

# 2. Relancer VS Code, puis :
#    Cmd/Ctrl + K, Cmd/Ctrl + T → "Ariane — Crème" ou "Ariane — Charbon"
```

Pour packager en `.vsix` :

```bash
cd vscode-theme
npx @vscode/vsce package
# produit ariane-guay-theme-0.1.0.vsix → installable via "Install from VSIX..."
```

## Règles respectées du DESIGN.md portfolio

- Toutes les valeurs hex viennent directement de `tokens.css` du portfolio (light et dark sections). Le mapping dark suit la règle G13 du DESIGN.md : "même fonction sémantique, pas même couleur".
- Mappings dark exactement alignés avec `@media (prefers-color-scheme: dark)` du portfolio : cream `#1c1510`, paper `#221b14`, dark `#0f0c08`, terra `#d4754f`, bourgogne→rose `#c2466a`. La moutarde n'est pas remappée en dark dans le portfolio, donc `#dba636` est conservée.
- Contraste AA respecté : `#9b4528` (terra-deep) sur `#f5efe4` (cream) = 4.6:1 pour le texte de code. En clair, `#c96442` (terra) reste réservée aux éléments décoratifs/UI larges (G11 du DESIGN.md).
- Le curseur clignote sur terracotta (clair) ou moutarde (sombre) — même geste que le `@keyframes blink` du site.

## Licence

MIT.
