# Leçon 12 : groupes imbriqués

Lorsque on travaille sur des données complexes, il peut souvent nous arriver de devoir extraire plusieurs couches d'information, ce qui peut entrainer la création de groupes imbriqués. En général, les résultats des groupes capturés sont dans le même ordre que celui dans lequel ils ont été défini (dans l'ordre des parenthèses ouvrantes).

Reprenons l'exemple de la leçon précédente où nous cherchions à extraire des noms de fichiers d'une liste. Nous pourrions simultanément extraire le nom complet et le nom sans l'extension en utilisant un seul et même pattern `^((IMG\d+)\.png)$`.

Les groupes imbriqués sont lus de gauche à droite, le premier groupe de capture étant celui contenu par la première paire de parenthèse.

## Exercice

Voici quelques dates. Ecrivez une regex qui corresponde et capture la date complète ainsi que l'année de chaque date.

1. capture Jan 1987 groupes capturés `Jan 1987` `1987`
2. capture Mai 1969 groupes capturés `Mai 1969` `1969`
3. capture Aou 2007 groupes capturés `Aou 2007` `2007`

**solution**

`(\w+ (\d+))`
