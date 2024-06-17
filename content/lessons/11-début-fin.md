# Leçon 10 : Début et fin

Jusqu'a maintenant nous avons écrit des expressions régulières qui correspondaient avec des parties de notre texte, indifféremment de leur position dans ce texte.

Imaginez par exemple que nous recherchons le mot `success` dans un fichier de log. On souhaiterais par contre éviter que notre motif corresponde avec une ligne comme `Error: unsuccessful operation`. Avec le motif `success`, nous correspondrions aux 2. C'est la raison pour laquelle il est généralement important d'écrire des regex les plus restrictives possibles.

Une des manière de restreindre nos regex est de définir un pattern qui décrit le début et la fin de notre ligne, en utilisant les métacaractères `^` et `$`.

En reprenant l'exemple du dessus, nous pourrions utiliser `^success` pour ne correspondre qu'avec les lignes commençant par le mot `success` et ainsi éviter tout faux positif causé par une ligne comme `Error: unsuccessful operation`.

Si on combine `^` et `$`, on crée un pattern qui correspond à la ligne complète, du début à la fin.

## Exercice

Ecrivez une regex qui corresponde seulement à la première ligne.

| tâche | texte                                           |
| ----- | ----------------------------------------------- |
| match | Mission: successful                             |
| skip  | Last Mission: unsuccessful                      |
| skip  | Next Mission: successful upon capture of target |
