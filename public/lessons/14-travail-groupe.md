# Leçon 13 : Travail sur les groupes

Nous l'avons vu lors des leçons précédentes, tous les quantificateurs (`*`, `+`, `{m,n}` et `?`) sont utilisables à l'intérieur des pattern de capture de groupe. C'est d'ailleurs la seule façon de les appliquer sur une séquence de caractères plutôt que sur un caractère isolé.

Imaginons par exemple que nous travaillons sur une liste de numéros de téléphone dont certains sont précédés de l'indicatif international (une série de 3 chiffres, 033 pour le france). Le pattern correct doit vérifier l'existence du groupe entier avec `(\d{3})?` et pas chaque caractère pris individuellement.

Certaines versions du moteur des expressions régulières permettent la création de groupe non-capturants. Ils permettent de correspondre à un groupe de caractères mais ne capture pas la valeur qui ne sera pas dans les résultats de l'extraction.

## Exercice

Vous trouverez ci-dessous une liste de résolutions d'affichage courantes, essayer de capturer la largeur et la hauteur de chacune d'entre elles. 

1. capture 1280x720 groupes capturés `1280` `720`
2. capture 1920x1600 groupes capturés `1920` `1600`
3. capture 1024x768 groupes capturés `1024` `768`

**solution**

`(\d+)x(\d+)`
