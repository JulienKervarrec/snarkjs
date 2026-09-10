# 5. Ce que vérifie Groth16 et ce que décide l’application

[groth16_verify](../../src/groth16_verify.js) convertit les valeurs sérialisées, charge la courbe et reconstruit la combinaison des éléments IC avec les signaux publics.
Il contrôle que les signaux publics considérés sont dans l’intervalle du corps scalaire.
Il contrôle aussi la validité des points de preuve avant l’équation de couplage.
Une équation acceptée lie la preuve à la clé de vérification et aux signaux publics transmis.
Elle ne décide pas automatiquement que ces signaux correspondent au destinataire, à l’état ou à l’action souhaités par l’application.
L’application doit donc construire et interpréter l’énoncé public sans ambiguïté.
Le chargement et le décodage peuvent également produire des erreurs : ne pas supposer que tous les fichiers malformés deviennent simplement `false`.
Cette lecture concerne le vérificateur Groth16 ; ne pas recopier ses détails internes comme une description de PLONK ou FFLONK.
Une bibliothèque de preuves n’est pas un contrôle d’autorisation métier complet.

Suite : [Du vérificateur Solidity au rollup : le périmètre manquant](06-evm-limites.md).
