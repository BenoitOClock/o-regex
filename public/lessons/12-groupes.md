# Leçon 11 : groupes

Grâce aux expressions régulières nous pouvons chercher des correspondances dans du texte mais également extraire des informations pour un traitement ultérieur.

En utilisant la notation entre parenthèses, il est possible de définir un groupe de caractères qui sera capturé. En pratique c'est très utile pour extraire des informations comme des numéros de téléphone ou des emails à partir de n'importe quel genre de données.

Imaginez que nous devons traiter une liste de fichiers et que nous souhaitons en extraire les noms des fichiers commençant par `IMG` suivi d'un ou plusieurs chiffres et se terminant par l'extension `.png`. Un pattern comme `^(IMG\d+\.png)$` nous permet d'extraire le nom de fichier complet. Si nous ne souhaitons pas récupérer l'extension `^(IMG\d+)\.png$` conviendra parfaitement.

## Exercice

Ecrivez une regex qui corresponde aux fichiers PDF et capture le nom des fichiers sans l'extension.

1. capture file_record_transcript.pdf groupe capturé `file_record_transcript`
2. capture file_07241999.pdf groupe capturé `file_07241999`
3. skip testfile_fake.pdf.tmp

**solution**

`^(file.+)\.pdf$`
