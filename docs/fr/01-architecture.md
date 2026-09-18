# 1. Architecture de Vault V2

Vault V2 sépare le coffre, sa fabrique et les marchés qui reçoivent les fonds.
La fabrique `VaultV2Factory.sol` déploie un coffre pour un propriétaire, un actif et un sel déterministe.
Elle conserve aussi une table qui permet de reconnaître les coffres qu’elle a créés.
Le contrat `VaultV2.sol` émet les parts, comptabilise les actifs et applique la configuration du risque.
Les positions externes ne vivent pas directement dans le coffre : elles passent par des adaptateurs.
Cette séparation rend chaque intégration explicite et limite l’interface confiée à un marché externe.
Le coffre lui-même est immuable ; son comportement évolue par sa configuration et ses adaptateurs autorisés.
La lecture doit donc suivre trois frontières : parts du coffre, allocation des adaptateurs et droits de gouvernance.

[Chapitre suivant : parts et comptabilité ERC-4626](02-parts-erc4626.md)
