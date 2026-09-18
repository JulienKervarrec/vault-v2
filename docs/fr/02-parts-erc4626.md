# 2. Parts et comptabilité ERC-4626

Le coffre expose les opérations `deposit`, `mint`, `withdraw` et `redeem` de l’interface ERC-4626.
Les fonctions d’aperçu convertissent actifs et parts après avoir simulé l’accumulation des frais.
Des parts virtuelles protègent la conversion initiale et réduisent l’effet des dons sur le premier déposant.
`totalAssets` additionne les actifs inactifs et la valeur déclarée par chaque adaptateur.
Le prix de part dépend donc de la justesse de `realAssets` dans toutes les intégrations actives.
Le code renvoie volontairement zéro pour les quatre fonctions `maxDeposit`, `maxMint`, `maxWithdraw` et `maxRedeem`.
Les intégrateurs ne doivent donc pas les interpréter comme des plafonds utilisables classiques.
Les transferts de parts et d’actifs peuvent enfin être filtrés par des contrats de contrôle externes.

[Chapitre suivant : adaptateurs et allocations](03-adaptateurs.md)
