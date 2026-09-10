# 1. Identifier les fichiers avant de prouver

Le [tutoriel amont](../../README.md) sépare compilation du circuit, génération du témoin, preuve et vérification.
Circom produit les contraintes `circuit.r1cs` et le calculateur `circuit_js/circuit.wasm` ; snarkjs ne remplace pas ce compilateur.
`input.json` contient les valeurs d’entrée du calculateur, pas un témoin déjà sérialisé.
`witness.wtns` est le témoin calculé, qui comprend les valeurs nécessaires au circuit.
La clé `.zkey` appartient au protocole et au circuit préparés ; `verification_key.json` en est un export pour la vérification.
`proof.json` et `public.json` contiennent respectivement la preuve et les signaux publics associés.
Ces fichiers ne sont pas interchangeables, même lorsqu’ils partagent l’extension JSON.
Le [code de calcul du témoin](../../src/wtns_calculate.js) lit le WASM et construit le témoin à partir des entrées.
Ce parcours traite Groth16, PLONK et FFLONK tels que présentés dans snarkjs, sans implémenter un rollup.

Suite : [Séparer paramètres universels et circuit](02-setup.md).
