# 5. Liquidité et sorties forcées

Les retraits utilisent d’abord les actifs inactifs conservés directement par le coffre.
Si ce solde ne suffit pas, le coffre sollicite l’adaptateur de liquidité configuré par l’allocateur.
Le même adaptateur peut recevoir automatiquement les nouveaux dépôts pour éviter un solde inactif excessif.
La fonction `forceDeallocate` permet à un utilisateur de rapatrier des actifs depuis un adaptateur précis.
Elle peut prélever une pénalité propre à l’adaptateur, plafonnée par les constantes du protocole.
Ce chemin permet aussi une sortie en nature lorsque les marchés sous-jacents ne disposent pas de liquidité immédiate.
Le demandeur porte alors la complexité de la position sous-jacente et de son éventuel financement temporaire.
La liquidité dépend donc à la fois du solde inactif, de l’adaptateur choisi et des marchés réellement disponibles.

[Chapitre suivant : rôles et temporisations](06-roles-temporisations.md)
