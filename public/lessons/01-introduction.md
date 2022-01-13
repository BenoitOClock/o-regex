# Leçon 1 : Introduction

Les **expression régulières** sont très utiles et très puissantes pour extraire les informations d'un texte quelconque, que cela soit du code, les logs d'un serveur ou les recettes de cuisine de votre grand-mère.

Les leçons suivantes ont pour but de vous familiariser avec l'utilisation pratique des expressions régulières afin de vous permettre de profiter de leur puissance le plus rapidement possible.

La première chose à bien comprendre lorsque l'on utilise les **regex** c'est que tout est essentiellement un caractère, et que nous écrivons des modèles (patterns) correspondant à une séquence spécifique de caractères. La plupart des patterns utilisent des caractères [ASCII](https://fr.wikipedia.org/wiki/American_Standard_Code_for_Information_Interchange), lettres, chiffres, signes de ponctuation et les autres symboles disponibles sur votre clavier, mais il est aussi possible d'utiliser des caractères unicode.

Vous trouverez ci-dessous un encart avec quelques lignes de texte et un champs de saisie où écrire votre **regex***. Pour passer à la leçon suivante, vous devrez utiliser les syntaxes et les concepts abordés dans la leçon pour écrire une expression régulière qui correspondent aux lignes présentées

Pour continuer, essayer d'écrire un pattern qui corresponde aux 3 lignes affichées... par exemple essayez simplement les lettres communes à chaque ligne

**exercice**

1. match abcdefg
2. match abcde
3. match abc

**solution**

`abc`