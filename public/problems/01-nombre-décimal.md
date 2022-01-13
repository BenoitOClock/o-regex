# Problème 1 : correspondance avec un nombre décimal

A première vue, écrire une regex qui corresponde à un nombre semble facile non ?

Nous disposons de `\d` qui correspond à n'importe quel chiffre, ensuite il suffit de faire correspondre le point de la décimale...non ? Pour des nombres simples oui... mais quand on travaille avec des données scientifiques, ou financières, il faut souvent gérer des nombres négatifs, parfois des exposant ou des présentations différentes, avec par exemple une virgule pour séparer milliers et millions...

## Exercice

Voici quelques nombres dans différents formats, essayez de trouver un pattern qui corresponde uniquement

| tâche | texte      |
| ----- | ---------- |
| match | 3.14529    |
| match | -255.34    |
| match | 1.9e10     |
| match | 123,340.00 |
| skip  | 720p       |

**Solution**

`^-?\d+(,\d+)*(\.\d+(e\d+)?)?$`
