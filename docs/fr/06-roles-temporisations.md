# 6. Rôles et temporisations

Le propriétaire choisit le curateur, les sentinelles ainsi que le nom et le symbole du coffre.
Le curateur configure les adaptateurs, les plafonds, les frais, les contrôles et les allocateurs.
Les allocateurs déplacent les fonds entre les intégrations déjà autorisées et gèrent la liquidité.
Les sentinelles peuvent annuler des actions en attente, réduire des plafonds et ramener des fonds au repos.
Une action sensible est d’abord enregistrée par `submit`, puis devient exécutable après son délai.
`revoke` supprime une action en attente lorsque le curateur ou une sentinelle intervient à temps.
Chaque sélecteur de fonction possède son propre délai, ce qui permet une politique graduée.
`abdicate` désactive irréversiblement une capacité de configuration : cette décision exige une revue particulière.

[Chapitre suivant : contrôles, taux et frais](07-controles-frais.md)
