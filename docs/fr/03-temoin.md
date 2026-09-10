# 3. Un témoin calculé ne définit pas le besoin métier

[wtns_calculate](../../src/wtns_calculate.js) instancie le calculateur depuis le WASM et lui fournit les entrées.
Le code distingue les formats de calculateur Circom pris en charge pour sérialiser un témoin WTNS.
Les options du calculateur sont transmises lors de sa construction.
Le résultat représente une affectation des valeurs du circuit ; il ne constitue pas encore une preuve vérifiée.
Le tutoriel propose une étape distincte de contrôle du témoin contre les contraintes R1CS.
Les contraintes décrivent ce qui sera démontré : un calculateur qui produit une valeur attendue ne compense pas une contrainte manquante.
Les valeurs destinées à rester privées ne doivent pas être publiées dans ce fork pour illustrer un exemple réel.
Les signaux publics, eux, font partie de l’énoncé communiqué au vérificateur.
Cette séparation aide à diagnostiquer les erreurs de fichier, de circuit et d’entrées sans les confondre avec la cryptographie.

Suite : [Réparer la continuité du tutoriel](04-fullprove.md).
