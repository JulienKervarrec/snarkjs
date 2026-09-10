# 2. Séparer paramètres universels et circuit

Le [guide](../../README.md) commence par une cérémonie Powers of Tau et prépare le fichier `.ptau` pour la suite.
Dans le chemin Groth16, la préparation de la clé est suivie d’une phase de contributions spécifique au circuit.
Les chemins PLONK et FFLONK utilisent les paramètres préparés mais ne suivent pas cette même cérémonie spécifique au circuit.
Cela ne signifie pas « aucun trusted setup » : il faut distinguer paramètres universels et phase spécifique.
Une clé doit rester associée au bon circuit et au bon protocole lors de la preuve et de l’export du vérificateur.
Le fichier `circuit_final.zkey` du tutoriel désigne la clé retenue dans le chemin choisi, pas une clé utilisable indistinctement pour les trois protocoles.
La [vérification depuis R1CS](../../src/zkey_verify_fromr1cs.js) reconstruit une clé initiale puis vérifie la phase suivante ; elle ne prouve pas à elle seule toutes les propriétés d’une cérémonie.
La provenance des paramètres et la conservation des transcriptions restent importantes.
Ne pas confondre un exemple pédagogique de cérémonie avec une préparation opérationnelle de production.

Suite : [Un témoin calculé ne définit pas le besoin métier](03-temoin.md).
