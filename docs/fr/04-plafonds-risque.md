# 4. Plafonds et facteurs de risque

Vault V2 regroupe les expositions par identifiants abstraits appelés `id`.
Un même identifiant peut représenter un collatéral, un oracle, un protocole ou un autre facteur commun.
Chaque allocation renvoyée par un adaptateur est ajoutée à la consommation de ses identifiants.
Un plafond absolu limite la quantité totale exposée à un facteur donné.
Un plafond relatif limite cette exposition par rapport à la valeur totale du coffre.
Les hausses de plafonds passent par le mécanisme temporisé, car elles augmentent le risque autorisé.
Les baisses peuvent être appliquées immédiatement afin de réduire l’exposition sans délai.
Une allocation n’est valide que si tous ses identifiants restent sous leurs deux plafonds applicables.

[Chapitre suivant : liquidité et sorties forcées](05-liquidite-sorties.md)
