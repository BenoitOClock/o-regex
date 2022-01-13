# Leçon 4 : Exclure des caractères spécifiques

Dans certains cas, on cherchera plutôt à exclure caractères spécifiques avec lesquels nous ne voulons pas que notre pattern corresponde. On pourrait par exemple ne vouloir correspondre qu'avec les numéros de téléphone ne commençant pas par `08`.

Pour représenter l'exclusion de caractères spécifiques, on utilise la même notation avec des crochets que pour les inclusions en ajoutant un `^` après le crochet ouvrant. Par exemple `[^abc]` correspond à n'importe quel caractère qui n'est ni `a`, ni `b`, ni `c`.

Ecrivez une expression régulière qui corresponde uniquement aux 2 premières lignes ci-dessous. La plupart des pattern de ce genre peuvent aussi être écrit en utilisant la technique de la leçon précédente. Utilisez la plus adaptée.

**exercice**

1. match hog
2. match dog
3. skip bog

**solution**

`[^b]og` ou `[hd]og`
