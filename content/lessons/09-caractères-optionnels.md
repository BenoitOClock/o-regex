# Leçon 8 : Caractères optionnels

Nous avons vu dans la leçon précédente comment l'étoile et le plus de Kleene nous permettent de correspondre à une répétition de caractères.

Un autre quantificateur commun est `?` qui dénote l'optionnalité. Ce quantificateur permet de correspondre à 0 ou une fois le caractère ou le groupe précédent. Par exemple le pattern `ab?c` correspond aux chaînes `abc` et `ac`, le `b`étant considéré comme optionnel.

Tout comme le métacaractère `.`, le point d'interrogation est un caractère spécial et il faudra l'échapper pour le faire correspondre à un point d'interrogation dans une chaîne.

Remarquer comme le pluriel du mot `file` dépend du nombre de fichiers trouvés et essayer d'écrire un pattern utilisant le quantificateur `?`et correspondant aux 3 premières lignes, celles où au moins un fichier est trouvé.

## exercice

| tâche | texte           |
| ----- | --------------- |
| match | 1 file found?   |
| match | 2 files found?  |
| match | 24 files found? |
| skip  | No files found? |

**solution**

`\d+ files? found\?`
