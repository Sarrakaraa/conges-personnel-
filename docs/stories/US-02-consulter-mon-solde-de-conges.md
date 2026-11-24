# US-02 - Consulter mon solde de congés
En tant que salarié, je veux consulter mon solde de congés afin de connaître le nombre de jours dont je dispose avant de faire une demande.
**Exigences liées :** REQ-F-02, REQ-F-09, RM-01, RM-02, RM-03, REQ-NF-01, REQ-NF-02

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Salarié avec un solde initial de 26 jours et aucune demande | Solde affiché : 26 jours | RM-01, RM-03 |
| 2 | Salarié avec 5 jours acceptés et 2 jours en attente | Solde disponible diminué de 7 jours | REQ-F-02, RM-03 |
| 3 | Salarié avec une demande refusée de 3 jours | Les 3 jours refusés ne sont pas déduits | RM-03 |
| 4 | Salarié ayant annulé une demande | Les jours réservés sont libérés | REQ-F-09, RM-03 |
| 5 | Utilisateur non authentifié qui tente d'accéder au solde | Accès refusé / authentification requise | REQ-NF-01 |
| 6 | Salarié qui consulte le solde d'un autre salarié | Accès non autorisé | REQ-NF-02 |

## Critères d'acceptation
- [ ] Étant donné qu'un salarié est authentifié, quand il consulte son solde, alors le système affiche son solde disponible.
- [ ] Étant donné qu'un salarié possède des demandes acceptées ou en attente, quand son solde est calculé, alors les jours correspondants sont déduits du solde disponible.
- [ ] Étant donné qu'une demande est refusée ou annulée, quand le solde est recalculé, alors les jours concernés sont libérés.
- [ ] Étant donné qu'un utilisateur n'est pas authentifié, quand il tente d'accéder au solde, alors le système exige une authentification.

## Questions ouvertes
- Le solde doit-il afficher séparément les jours acquis, réservés et réellement disponibles ? Hypothèse provisoire : afficher au minimum le solde disponible et permettre de consulter le détail des mouvements.

