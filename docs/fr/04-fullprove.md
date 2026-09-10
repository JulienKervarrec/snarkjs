# 4. Réparer la continuité du tutoriel

Dans [groth16_fullprove](../../src/groth16_fullprove.js), les entrées sont converties, un témoin est calculé en mémoire, puis le prouveur Groth16 est appelé.
Le premier argument désigne donc les entrées du calculateur, pas un fichier WTNS préexistant.
En suivant les étapes du README, la commande Groth16 cohérente est :

`snarkjs groth16 fullprove input.json circuit_js/circuit.wasm circuit_final.zkey proof.json public.json`

La même continuité de chemins s’applique aux exemples PLONK et FFLONK du guide, avec leur propre clé préparée.
La [PR amont #635](https://github.com/iden3/snarkjs/pull/635) corrige ces trois commandes ainsi que le nom de clé dans deux commandes FFLONK.
La correction est volontairement isolée des présents chapitres ; une proposition ouverte n’est pas une contribution déjà fusionnée.
La validation effectuée est statique, par comparaison avec [cli.js](../../cli.js) et le [workflow du tutoriel](../../.github/workflows/tutorial.yml), sans exécuter les commandes.

Suite : [Ce que vérifie Groth16 et ce que décide l’application](05-verification.md).
