# Leçon 2 : Le point

Nous devons souvent faire correspondre nos regex avec des morceaux de texte dont nous ne connaissons pas le contenu exact, mais uniquement qu'ils partagent une structure commune (ex: des numéros de téléphone, des code postaux...).

Pour réaliser ce genre de pattern nous disposons du métacaractère `.` qui correspond à n'importe quel caractère (lettres, chiffres, espace...). Si vous devez correspondre au caractère `.`, vous devrez l'échapper en utilisant un backslash.

## exercice

Vous trouverez ci-dessous 4 chaînes dont les caractères diffèrent mais qui sont de même longueur. Essayez d'écrire une expression régulière qui corresponde aux 3 premières lignes (indice : elles se terminent toutes par un point) mais pas à la dernière.

| tâche | texte |
| ----- | ----- |
| match | cat.  |
| match | 598.  |
| match | ?=+.  |
| match | abc1  |

**solution**

`...\.`
