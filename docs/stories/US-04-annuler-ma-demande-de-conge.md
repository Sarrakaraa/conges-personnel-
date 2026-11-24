# US-04 - Annuler ma demande de congé
En tant que salarié, je veux annuler une demande de congé en attente ou acceptée avant le début du congé afin de libérer les jours réservés si mes plans changent.
**Exigences liées :** REQ-F-03, REQ-F-09, REQ-F-13, REQ-F-14, RM-03, RM-08, RM-09

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Demande en attente annulée avant le début du congé | Annulation autorisée et jours libérés | RM-08, REQ-F-09 |
| 2 | Demande acceptée annulée plus de 7 jours avant le début | Annulation autorisée, sans blocage de 30 jours | RM-08, RM-09 |
| 3 | Demande acceptée annulée moins de 7 jours avant le début | Annulation autorisée et blocage de 30 jours | REQ-F-14, RM-09 |
| 4 | Demande annulée le jour du début du congé | Refusée car le congé a déjà commencé | RM-08 |
| 5 | Tentative de modifier directement les dates d'une demande existante | Modification directe non autorisée ; annuler puis créer une nouvelle demande | RM-08 |

## Critères d'acceptation
- [ ] Étant donné qu'une demande est en attente et que le congé n'a pas commencé, quand le salarié l'annule, alors son statut devient « annulée » et les jours réservés sont libérés.
- [ ] Étant donné qu'une demande acceptée est annulée moins de 7 jours avant son début, quand l'annulation est enregistrée, alors le salarié est bloqué pour les nouvelles demandes annuelles pendant 30 jours.
- [ ] Étant donné que le congé a déjà commencé, quand le salarié tente d'annuler la demande, alors l'annulation est refusée.
- [ ] Étant donné qu'une demande existe déjà, quand le salarié veut changer ses dates, alors le système ne permet pas une modification directe.

## Questions ouvertes
- La règle de blocage de 30 jours s'applique-t-elle à toute annulation tardive d'une demande acceptée, même si l'absence n'a finalement pas commencé ? Hypothèse provisoire : oui, car RM-09 se base sur la date d'annulation.


