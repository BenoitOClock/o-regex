# Leçon 8 : Caractères optionnels

Nous avons vu dans la leçon précédente comment m'étoile et le plus de Kleene nous permettent de correspondre à une répétition de caractères.

Un autre quantificateur commun est le métacractère `?` qui dénote l'optionnalité. Ce métacaractère permet de correspondre à 0 ou une fois le caractère ou le groupe précédent. Par exemple le pattern `ab?c` correspond aux chaînes `abc` et `ac`, le `b`étant considéré comme optionnel.

Tout comme le métacaractère `.`, le point d'interrogation est un caractère spécial et il faudra l'échapper pour le faire correspondre à un point d'interrogation dans une chaîne.

Remarquer comme le pluriel du mot `file` dépend du nombre de fichiers trouvés et essayer d'écrire un pattern utilisant le métacaractère `?`et correspondant aux 3 premières lignes, celles où au moins un fichier est trouvé.

**exercice**

1. match 1 file found?
2. match 2 files found?
3. match 24 files found?
4. skip No files found?

**solution**

`\d+ files? found\?`
