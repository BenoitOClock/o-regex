# Leçon 14 : Conditions

Plus une expression régulière est précise, meilleure elle est. Si vous deviez écrire une liste de course pour quelqu'un, vous n'écririez pas `acheter du ./`. Dieu seul sait avec quoi il reviendrait. Vous écririez `acheter du pain` ou `acheter du lait` et les expressions régulières nous permettent de définir ces conditions.

Vous pouvez utiliser le `|` (**OR logique, aka the pipe**) pour signifier différents ensemble de caractères possible. Si nous reprenons l'exemple précédent, nous pourrions écrire le pattern`acheter du (pain|lait)` pour ne correspondre qu'aux chaînes `acheter du pain` ou `acheter du lait`.

Vous pouvez utilisez n'importe quelle suite de caractères ou de métacaractères dans une condition. Par exemple `([cb]at|[dh]og)` correspond à `cat`, `bat`, `dog` ou `hog`.

## Exercice

Essayez d'écrire un pattern conditionnel qui ne corresponde qu'aux 3 premières lignes.

| tâche | texte       |
| ----- | ----------- |
| match | I love cats |
| match | I love dogs |
| skip  | I love logs |
| skip  | I love cogs |

**solution**

`I love (cats|dogs)`
