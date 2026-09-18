# 7. Contrôles, taux et frais

Quatre contrôles externes peuvent filtrer la réception et l’envoi des parts ou des actifs.
L’absence d’un contrôle signifie que l’opération correspondante reste ouverte.
Le dépôt fournit des exemples de listes blanches, mais leur politique dépend du contrat branché.
`maxRate` borne la vitesse d’augmentation du prix de part observé par le coffre.
Cette limite peut lisser le rendement distribué et créer un tampon contre des pertes futures.
Les frais de performance prélèvent une part des intérêts, tandis que les frais de gestion portent sur le principal.
Le code plafonne ces deux catégories et comptabilise séparément leurs destinataires.
Une revue doit relier chaque contrôle au rôle qui peut le changer et au délai appliqué à ce changement.

[Chapitre suivant : limites et vérification](08-limites-verification.md)
