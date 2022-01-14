# Problème 2 : correspondance avec un numéro de téléphone

Valider des numéros de téléphone peut être une tâche difficile en fonction du type de données disponible. Certains numéros comme aux états unis peuvent avoir un code de zone, les numéro internationaux qui nécessitent un prefix, les gens qui utilisent parfois des espaces ou des tirets entre des groupes de chiffres... tout cela peut sérieusement compliqué notre regex.

## Exercice

Voici quelques numéros de téléphones. Validez les numéros de téléphone fixe (ceux commençant habituellement par 01, 02, 03, 04 ou 05) et récupérez les indicatifs de régions.

| tâche   | texte             | groupes capturés |
| ------- | ----------------- | ---------------- |
| capture | (+33) 561 578 265 | `5`              |
| capture | 04 62 82 63 01    | `4`              |
| capture | +33 223-145-476   | `2`              |
| capture | 01-42-35-42-47    | `1`              |
| capture | 0312345678        | `3`              |
| skip    | 0605927705        |                  |
| skip    | 05123678415       |                  |
| skip    | +33 321-1456-124  |                  |
| skip    | +33 621 345 120   |                  |

**Solution**

`^(?:\(?\+33\)?|0) *([1-5])(?:[ -]?\d){8} *$`
