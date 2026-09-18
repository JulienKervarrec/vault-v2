# 8. Limites et vérification

Ce parcours décrit l’architecture visible dans `src/VaultV2.sol`, les adaptateurs et la périphérie principale.
Il ne constitue ni un audit de sécurité ni une recommandation d’allocation dans un coffre.
La valeur déclarée par un adaptateur, les registres autorisés et les contrats de contrôle restent des frontières critiques.
Les temporisations protègent seulement les opérations auxquelles un délai non nul est effectivement associé.
Une abdication est irréversible et doit être évaluée avec la liste finale des adaptateurs et des registres.
Les fonctions ERC-4626 de maximum renvoient zéro, particularité importante pour les interfaces et agrégateurs.
Les rapports du dossier `audits/` documentent des périmètres précis et ne remplacent pas une revue de la version utilisée.
Pour vérifier le comportement, consulter les scénarios du dossier `test/` et leurs invariants associés.
Aucune installation, compilation ou exécution de test n’a été réalisée pour ce parcours documentaire.
