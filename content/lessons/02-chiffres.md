# Leçon 1 1/2 : Les chiffres

Au cours des leçons suivantes, nous vous présenterons un certain nombre de [métacaractères](https://fr.wikipedia.org/wiki/M%C3%A9tacaract%C3%A8re) utilisables dans les expressions régulières pour correspondre à un type de caractère particulier.

Concernant les chiffres, le métacaractère `\d` peut être utilisé pour correspondre à n'importe quel chiffre. Le backslash distingue le métacractère du simple caractère `d`.

## exercice

Voici quelques lignes de texte contenant des chiffres. Essayez d'écrire un pattern qui corresponde à tous les chiffres de ces lignes et remarquer comme votre pattern correspond avec les chiffres où qu'ils se situent dans la chaîne et pas simplement en partant du début. Nous verrons comment contrôler ce comportement dans une des leçons suivantes.

| tâche | texte                |
| ----- | -------------------- |
| match | const distance = 123 |
| match | define "123"         |
| match | abc123xyz            |

**solution**

`123` ou `\d\d\d`
