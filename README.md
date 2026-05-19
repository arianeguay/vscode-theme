# Ariane Guay — Atelier

Thème VS Code chaud et artisanal, dérivé directement des tokens du portfolio d'[Ariane Guay](https://arianeguay.com). Palette terracotta · crème · charbon chaud, jamais clinique.

Deux variantes :

- **Ariane — Crème** (clair) — atmosphère papier, accent terracotta, ponctuation bourgogne pour les mots-clés.
- **Ariane — Charbon** (sombre) — surface `--color-dark` du portfolio (#2a2018) avec accents terracotta éclaircis et moutarde pour les chaînes/valeurs.

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
| Commentaires | `#8a7560` italique | `#ead9d477` italique |
| Mots-clés (control) | bourgogne `#7a1f3d` | rose `#e8909f` |
| Storage (`const`, `class`) | terra-deep `#9b4528` | terra `#e07a5a` |
| Chaînes | terra-deep `#9b4528` | moutarde `#e8c267` |
| Nombres | terra-deep `#9b4528` | moutarde `#e8c267` |
| Fonctions (déf.) | ink `#2a2018` bold | dark-fg `#ead9d4` bold |
| Fonctions (appel) | terra-deep `#9b4528` | moutarde `#e8c267` |
| Types / classes | ink-soft `#4a3d31` bold | beige-rosé `#c8b3ab` bold |
| Variables | ink `#2a2018` | dark-fg `#ead9d4` |
| Tags JSX/HTML | terra-deep `#9b4528` | terra `#e07a5a` |
| Attributs HTML | bourgogne `#7a1f3d` italique | moutarde `#e8c267` italique |

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

- Aucune valeur hex en dehors des tokens du site (les valeurs `#e07a5a`, `#e8c267`, `#e8909f`, `#c8b3ab` du thème sombre sont les équivalents perceptuels — voir G13 du portfolio AGENTS.md, "même fonction sémantique, pas même couleur").
- Moutarde et bourgogne ne cohabitent jamais dans la même variante.
- Contraste AA respecté : `#9b4528` (terra-deep) sur `#f5efe4` (cream) = 4.6:1 pour le texte de code.
- Le curseur clignote sur terracotta (clair) ou moutarde (sombre) — même geste que le `@keyframes blink` du site.

## Licence

MIT.
