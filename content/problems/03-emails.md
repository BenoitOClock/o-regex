# Problème 3 : correspondance avec des emails

Quand on travaille avec des formulaires, il est courant d'utiliser des expressions régulières pour la validation. Il peut être particulièrement compliqué de valider correctement des emails à cause de la complexité de la [spécification](https://datatracker.ietf.org/doc/html/rfc2822#section-3.4.1). Il est d'ailleurs généralement préférable d'utiliser un framework ou un plugin pluôt que de faire ce genre de chose nous même. Cela dit, il est quand même possible de créer des regex robustes qui correspondent à la majorité des emails les plus courants avec ce que nous avons appris.

Un des points délicat est que beaucoup de personnes ajoutent une chaîne de caractère après un `+` pour leur permettre de filtrer facilement leurs mails. `nom+filtre@gmail.com` arrivera sur `nom@gmail.com` et pourra facilement être filtrer. Pour ne rien simplifier, certains domaines utilisent plusieurs composants. Vous pourriez par exemple tomber sur un email comme `ilove@sushi.hk.com`

## Exercice

Voici quelques adresses emails, essayez de les valider et de capturer le nom, sans le filtre s'il y en a un, et le domaine.

| tâche   | texte                          | groupes capturés                 |
| ------- | ------------------------------ | -------------------------------- |
| capture | hermione@hogwarts.com          | `hermione` `hogwarts.com`        |
| capture | tom.riddle@hogwarts.com        | `tom.riddle` `hogwarts.com`      |
| capture | potter+gryffindor@hogwarts.com | `potter` `hogwarts.com`          |
| capture | harry.potter@hogwarts.eu.com   | `harry.potter` `hogwarts.eu.com` |
| skip    | albus@hogwart                  |                                  |
| skip    | drago+slytherin@hogwart+com    |                                  |
| skip    | regulus@.hogwarts.com          |                                  |

**Solution**

`^((?:\w+)\.?(?:\w*))(?:\+\w+)?@((?:\w+\.?){1,2}(?:\.\w+))$`