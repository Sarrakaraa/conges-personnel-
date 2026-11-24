# US-05 - Demander un congé exceptionnel
En tant que salarié, je veux demander un congé exceptionnel pour mariage, naissance ou décès afin de bénéficier d'une absence prévue par les règles de l'entreprise.
**Exigences liées :** REQ-F-03, REQ-F-06, REQ-F-12, RM-02, RM-07, REQ-NF-01, REQ-NF-02

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Demande pour mariage de 3 jours ouvrables | Acceptée immédiatement | REQ-F-12, RM-07 |
| 2 | Demande pour naissance de 2 jours ouvrables | Acceptée immédiatement | RM-07 |
| 3 | Demande pour décès de 3 jours ouvrables | Acceptée immédiatement | RM-07 |
| 4 | Demande exceptionnelle de 4 jours ouvrables | Refusée car la limite est de 3 jours | REQ-F-12, RM-07 |
| 5 | Demande exceptionnelle pour un motif autre que mariage, naissance ou décès | À confirmer avec le client | REQ-F-12 |
| 6 | Demande exceptionnelle alors que l'équipe a déjà 2 absents | La demande exceptionnelle reste soumise à RM-07 ; elle ne suit pas le plafond normal, mais le salarié compte dans les absences | RM-07 |

## Critères d'acceptation
- [ ] Étant donné qu'un salarié demande un congé exceptionnel pour mariage, naissance ou décès d'une durée maximale de 3 jours ouvrables, quand il soumet sa demande, alors celle-ci est acceptée immédiatement conformément à RM-07.
- [ ] Étant donné qu'un salarié demande plus de 3 jours ouvrables de congé exceptionnel, quand il soumet sa demande, alors la demande est refusée.
- [ ] Étant donné qu'un congé exceptionnel est accepté, quand le planning d'équipe est mis à jour, alors le salarié est comptabilisé parmi les absences de l'équipe.
- [ ] Étant donné qu'un salarié demande un congé pour un motif non prévu, quand il soumet la demande, alors le système ne décide pas automatiquement sans règle validée.

## Questions ouvertes
- Un justificatif doit-il être fourni pour un congé exceptionnel (mariage, naissance ou décès) ? Hypothèse provisoire : aucun justificatif obligatoire tant que le client ne l'a pas confirmé.

