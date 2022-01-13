# Leçon 6 : Répétition

Jusqu'a présent nous avons appris à spécifier la correspondance avec un caractère, intéressons nous maintenant au nombre de fois où se répète une même correspondance. Il est possible de répéter un même pattern, ainsi `\d\d\d` correspondrait à 3 chiffres qui se suivent.

Il est également possible de spécifier le nombre de répétitions en utilisant la notation entre accolades. Par exemple `a{3}` correspond à 3 caractères `a` qui se suivent. Il est également possible de définir un intervalle de répétitions comme `a{1,3}` qui correspond au minimum à un `a` et au plus à 3.

Ce quantificateur peut-être utilisé avec n'importe quel caractère ou métacaractère. par exemple w{3} correspond à 3 `w`, `[wxy]{5}` correspond à 5 caractères pouvant être `w`, `x` ou `y` et .{2,6} correspond à entre 2 et 6 fois n'importe quel caractère.

## exercice

Ecrivez une expression régulière qui ne correspond qu'aux 2 premières lignes.

| tâche | texte     |
| ----- | --------- |
| match | wazzzzzup |
| match | wazzup    |
| skip  | wazup     |

**solution**

waz{2,5}up
