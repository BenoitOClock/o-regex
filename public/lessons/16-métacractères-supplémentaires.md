# Leçon 15: Quelques métacaractères de plus...

Cette dernière leçon aborde quelques métacaractères supplémentaires et l'utilisation de groupes capturés.

Nous avons déjà parlé des métacractères les plus communs

- `\d` pour les chiffres
- `\s` pour les espacements
- `\w` pour les caractères alphanumériques

mais il existe aussi des métacractères pour les ensembles opposés

- `\D` pour tous les caractères hormis les chiffres
- `\S` pour tous les caractères qui ne sont pas des espacements
- `\W` pour tous les caractères non-alphanumériques comme la ponctuation

Il existe aussi un métacractère `\b` qui correspond à la fin d'un mot et qui est très pratique pour capturer des mots complets (en utilisant par exemple un pattern comme `\w+\b`).

Un des concepts que nous n'avons pas encore abordé concerne le **back referencing**. le back referencing est la possibilité de faire référence aux groupes que nous avons capturés dans notre pattern en utilisant `\0` pour la correspondance complète, `\1` pour le premier groupe, `\2` pour le second, etc... Par exemple on peut correspondre avec la répétition d'un mot malencontreusement tapé 2 fois avec `\b(\w+)\s+\1\b` qui correspond aussi bien à `le le` qu'a `maintenant maintenant`.

## Exercice

Quelques lignes ci-dessous, amusez-vous avec les différents métacaractères et tout ce que vous avez appris au cours des leçons précédentes. Et passer à la suite quand vous en avez assez :)

| tâche | texte                                                        |
| ----- | ------------------------------------------------------------ |
| match | The quick brown fox jumps over the lazy dog.                 |
| match | There were 614 instances of students getting 90.0% or above. |
| match | The FCC had to censor the network for saying &$#\*@!.        |

**Solution**

`.*`