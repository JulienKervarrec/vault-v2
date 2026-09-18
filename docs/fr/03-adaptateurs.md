# 3. Adaptateurs et allocations

Un adaptateur représente une position détenue pour le compte du coffre dans un protocole sous-jacent.
`allocate` transfère des actifs vers l’adaptateur, puis contrôle les identifiants de risque qu’il retourne.
`deallocate` récupère des actifs et met à jour les mêmes identifiants après l’opération.
Le dépôt contient un adaptateur pour les marchés Morpho Blue et un autre pour les coffres Morpho V1.
Chaque instance fixe de manière immuable son coffre parent et les dépendances qu’elle utilise.
L’adaptateur Morpho Blue suit les parts fournies marché par marché et estime leur valeur courante.
L’adaptateur de coffre V1 suit une position ERC-4626 sous-jacente et expose sa valeur au coffre parent.
Une liste d’adaptateurs autorisés peut être imposée par un registre, notamment avant une abdication.

[Chapitre suivant : plafonds et facteurs de risque](04-plafonds-risque.md)
