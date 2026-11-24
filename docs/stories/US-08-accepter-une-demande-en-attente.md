# US-08 - Accepter une demande en attente
En tant que responsable d'équipe, je veux accepter une demande de congé en attente afin de confirmer l'absence d'un membre de mon équipe.
**Exigences liées :** REQ-F-05, REQ-F-06, REQ-F-03, REQ-NF-01, REQ-NF-02, RM-06, RM-11

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Responsable de l'équipe accepte une demande en attente de son équipe et plafond respecté | Demande acceptée | REQ-F-05 |
| 2 | Responsable tente d'accepter une demande déjà refusée | Action impossible | REQ-F-03 |
| 3 | Responsable tente d'accepter une demande d'une autre équipe | Accès refusé | REQ-NF-02 |
| 4 | Demande en attente mais le plafond d'absences n'est plus respecté au moment de la décision | Acceptation bloquée / décision à confirmer selon le contrôle au moment de validation | RM-06 |
| 5 | Demande courte déjà acceptée automatiquement | Aucune validation manuelle nécessaire | RM-11 |

## Critères d'acceptation
- [ ] Étant donné qu'une demande est en attente et concerne un salarié de son équipe, quand le responsable l'accepte, alors son statut devient « acceptée ».
- [ ] Étant donné qu'une demande n'est pas en attente, quand le responsable tente de l'accepter, alors le système refuse l'action.
- [ ] Étant donné qu'un responsable tente de traiter une demande d'une autre équipe, quand il lance l'action, alors l'accès est refusé.
- [ ] Étant donné qu'une demande dépasse la durée de 2 jours, quand elle est soumise, alors elle reste en attente jusqu'à la décision du responsable.

## Questions ouvertes
- Si la situation des absences change entre le dépôt et la validation, le plafond doit-il être vérifié de nouveau au moment où le responsable accepte ? Hypothèse provisoire : oui, afin d'éviter de dépasser la limite au moment de l'acceptation.


