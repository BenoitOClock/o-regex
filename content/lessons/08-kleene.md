# Leçon 7 : L'étoile et le plus de Kleene

Un des concepts les plus puissant des regex est la possibilité de correspondre à un nombre indéterminé de caractères.

Une manière d'exprimer un tel pattern est d'utiliser les quantificateurs connus sous le nom d'étoile `*` et de plus `+` de Kleene (Stephen Cole Kleene est considéré comme l'inventeur des expressions régulières). L'étoile de Kleene, `*` représente 0 ou d'avantage de fois le caractère ou le groupe qu'elle suit. Le plus de Kleene, `+` représente quant à lui 1 ou d'avantage de fois le caractère ou le groupe qu'il suit.
Par exemple `\d*` correspond à n'importe quel nombre de chiffres alors que `\d+` correspond à au moins un chiffre.

Ces quantificateurs peuvent-être utilisés avec n'importe quel caractère ou métacaractère. par exemple `a+` correspond à un `a` ou d'avantage, `[abc]*` à un ou plus de `a`, de `b` ou de `c` et `.*` à 0 ou d'avantage de fois n'importe quel caractère.

## exercice

Essayer de trouver une regex qui ne corresponde qu'aux 3 premières lignes en utilisant l'étoile et le plus de Kleene

| tâche | texte   |
| ----- | ------- |
| match | aaaabcc |
| match | aabbbbc |
| match | aacc    |
| skip  | a       |

**solution**

`aa+b*c+`
