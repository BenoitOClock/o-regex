# Leçon 3 : Correspondre avec des caractères spécifiques

Le métacaractère `.` que nous venons de voir est très puissant... parfois il est même trop puissant. Si on cherchait une expression régulière correspondant à des numéros de téléphone, nous ne souhaiterions pas valider une chaîne comportant des lettres comme `(abc) def-ghi-klm `.

Il est possible de faire correspondre notre pattern avec plusieurs caractères spécifiques en les listants entre crochets. Par exemple le pattern `[abc]` ne correspondra qu'a un seul caractère pouvant être `a`, `b` ou `c` et rien d'autre.

Trouvez une expression régulière qui corresponde uniquement aux 3 première lignes ci-dessous. Vous constatez qu'en utilisant le`.` il est impossible de ne pas correspondre avec les 3 dernières lignes.

**exercice**

1. match can
2. match man
3. match fan
4. skip dan
5. skip ran
6. skip pan

**solution**

[cmf]an ou [^drp]