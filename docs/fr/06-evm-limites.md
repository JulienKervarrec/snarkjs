# 6. Du vérificateur Solidity au rollup : le périmètre manquant

L’[export Solidity](../../src/zkey_export_solidityverifier.js) sélectionne le traitement selon le protocole, avec un chemin spécifique pour FFLONK.
Le tutoriel décrit ensuite l’export des arguments destinés à l’appel du vérificateur.
Exporter un contrat ne suffit pas à créer un rollup : il faut encore définir et lier les transitions d’état à ce contrat.
La disponibilité des données, les dépôts et retraits, l’ordre des transactions et les mises à jour ne sont pas fournis par ce parcours.
Un mécanisme de preuve de validité n’implique pas à lui seul la confidentialité de toutes les données d’une application.
Cette contribution comprend une correction documentaire proposée en amont et une lecture française du code ; aucun algorithme cryptographique n’a été modifié.
Aucune installation, compilation, exécution de preuve ou de test n’a été réalisée pour ces travaux.
Pour prolonger la vérification, consulter [test](../../test), [package.json](../../package.json) et le [workflow du tutoriel](../../.github/workflows/tutorial.yml).
La licence du projet est décrite dans [COPYING](../../COPYING) ; ce fork conserve le code et les mentions amont.

Retour au [sommaire](README.md).
