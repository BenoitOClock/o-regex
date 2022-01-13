# Leçons 9 : Les espacements

Il est très fréquent de devoir manipuler des textes contenant des espaces, des tabulations, ou des retours à la ligne qui sont utilisés pour les formater et les rendre plus lisibles.

Les espacements les plus fréquents sont :

- l'espace ` `,
- la tabulation `\t`,
- la nouvelle ligne `\n`
- le retour chariot `\r` (utile principalement sous Windows).

Il existe en plus un métacaractère `\s` qui correspond à tous les espacements ci-dessus.

Ecrivez une expression régulière qui corresponde aux 3 premières lignes (les seules à contenir un ou des espacements).

## exercice

1. match 1. abc
2. match 2.     abc
3. match 3.        abc
4. skip 4.abc

**solution**

`\d\.\s+abc`
