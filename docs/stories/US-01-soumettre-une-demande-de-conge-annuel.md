# US-01 - Soumettre une demande de congé annuel
En tant que salarié, je veux soumettre une demande de congé annuel avec une date de début et une date de fin afin de demander mes congés sans utiliser de formulaire papier.
**Exigences liées :** REQ-F-01, REQ-F-03, REQ-F-09, REQ-F-10, REQ-F-11, REQ-F-17, RM-01, RM-02, RM-03, RM-04, RM-05, RM-06, RM-11

## Exemples
**Situation de référence :** Salarié E01, équipe A, solde disponible de 10 jours. Sauf indication contraire, aucune demande existante ne crée de conflit et aucun jour férié ne tombe dans les périodes citées.

| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Demande de 2 jours ouvrables, déposée 10 jours avant, solde suffisant, équipe sous la limite | Acceptée automatiquement | REQ-F-17, RM-11 |
| 2 | Demande de 1 jour ouvrable, déposée 10 jours avant, solde suffisant, équipe sous la limite | Acceptée automatiquement | REQ-F-17, RM-11 |
| 3 | Demande de 3 jours ouvrables, déposée 10 jours avant, solde suffisant, équipe sous la limite | En attente de décision du responsable | REQ-F-03, RM-11 |
| 4 | Demande de 5 jours ouvrables alors que le solde disponible est de 3 jours | Refusée automatiquement | RM-03, RM-05 |
| 5 | Demande dont le premier jour de congé est dans moins de 7 jours | Refusée automatiquement | REQ-F-11, RM-04 |
| 6 | Demande déposée exactement 7 jours avant le premier jour ouvrable de congé | Acceptée ou mise en attente selon les autres règles | RM-04, RM-11 |
| 7 | Demande sur une période comprenant un samedi et un dimanche | Les jours du week-end ne sont pas déduits du solde | RM-02, RM-03 |
| 8 | Demande sur une période comprenant un jour férié enregistré par les RH | Le jour férié n'est pas déduit du solde | REQ-F-19, RM-02 |
| 9 | Deux salariés de l'équipe sont déjà absents le même jour demandé | Refusée pour dépassement de la limite | REQ-F-10, RM-06 |
| 10 | Un seul salarié de l'équipe est déjà absent le jour demandé | La demande peut être acceptée si les autres règles sont respectées | RM-06 |
| 11 | Demande de plus de 2 jours ouvrables, toutes les règles automatiques respectées | En attente de décision du responsable | REQ-F-05, RM-11 |
| 12 | Demande déposée par un salarié soumis à un blocage de 30 jours | Refusée pendant la période de blocage | REQ-F-14, RM-09 |
| 13 | Demande avec un solde suffisant et une exception de limite autorisée par le directeur RH, sans dépasser 3 absents | Acceptée ou mise en attente selon la durée | REQ-F-16, RM-10, RM-11 |
| 14 | Demande d'un salarié dont le contrat n'est ni CDI ni CDD | Hors périmètre de la version 1 | RM-12 |

## Critères d'acceptation
- [ ] Étant donné que le salarié dispose d'un solde suffisant et que toutes les règles sont respectées, quand il soumet une demande de 2 jours ouvrables ou moins, alors la demande est acceptée automatiquement et les jours sont réservés.
- [ ] Étant donné que deux salariés de l'équipe sont déjà absents à une date demandée, quand un troisième salarié demande un congé annuel couvrant cette date, alors sa demande est refusée conformément à la limite d'absences.
- [ ] Étant donné que le premier jour ouvrable demandé se situe à moins de 7 jours du dépôt, quand le salarié soumet sa demande, alors le système la refuse automatiquement.
- [ ] Étant donné que le salarié demande plus de 2 jours ouvrables et respecte les règles automatiques, quand il soumet sa demande, alors son statut devient « en attente » pour décision du responsable.
- [ ] Étant donné que le solde disponible est inférieur au nombre de jours ouvrables demandés, quand le salarié soumet sa demande, alors le système refuse la demande et ne réserve pas les jours.

## Questions ouvertes
- Le délai de 7 jours de RM-04 est-il calculé en jours calendaires ou en jours ouvrables ? Hypothèse provisoire : jours calendaires, car la règle indique « 7 jours » et non « 7 jours ouvrables ».
- Pour une demande déposée exactement 7 jours avant le premier jour ouvrable du congé, le délai est-il considéré comme respecté ? Hypothèse provisoire : oui, car la règle exige au moins 7 jours.


