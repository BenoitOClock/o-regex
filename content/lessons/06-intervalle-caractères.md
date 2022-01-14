# Leçon 5 : Intervalles de caractères

Nous venons de voir comment inclure ou exclure des caractères spécifiques, voyons maintenant comment correspondre avec un intervalle de caractères.

Quand on utilise la notation entre crochets, il est possible d'utilise le `-`pour indiquer un intervalle de caractères. Par exemple, le pattern `[0-6]` correspondrait à n'importe quel chiffre compris entre `0` et `6` inclus et à rien d'autre. Et de la même façon, `[^n-p]` correspondrait à n'importe quel caractères pourvu que ce ne soit pas une lettre comprise entre `n` et `p` inclus.

Il est possible d'utiliser plusieurs intervalles au sein de la même paire de crochets et aussi d'y adjoindre des caractères spécifiques. Par exemple `[A-Za-z0-9_]` correspondra à une lettre majuscule ou minuscule, un chiffre, ou au caractère `_`. Cet intervalle correspond au métacaractère `\w`, souvent utilisé pour correspondre à des caractères dans des textes en anglais (pour du français... `[a-zA-ZÀ-ÿ0-9-]`, pas de métacaractère directement accessible).

## exercice

Dans cet exercice vous devez trouver une regex correspondant aux 3 premières lignes. Notez que les intervalles sont sensibles à la casse. `[a-z]` ne correspond qu'aux minuscules et `[A-Z]` qu'aux majuscules.

| tâche | texte |
| ----- | ----- |
| match | Ana   |
| match | Bob   |
| match | Cpc   |
| skip  | aax   |
| skip  | bby   |
| skip  | ccz   |

**solution**

`[A-C][n-p][a-c]` ou `[^a-c][^a-c][^x-z]`
