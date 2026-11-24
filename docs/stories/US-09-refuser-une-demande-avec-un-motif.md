# US-09 - Refuser une demande avec un motif
En tant que responsable d'équipe, je veux refuser une demande de congé en attente en indiquant un motif afin que le salarié comprenne la décision.
**Exigences liées :** REQ-F-05, REQ-F-06, REQ-F-03, REQ-NF-01, REQ-NF-02

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Responsable refuse une demande en attente et saisit un motif | Demande refusée et motif enregistré | REQ-F-05 |
| 2 | Responsable refuse sans saisir de motif | Refus impossible | REQ-F-05 |
| 3 | Responsable refuse une demande déjà acceptée | Action impossible | REQ-F-03 |
| 4 | Responsable d'une autre équipe tente le refus | Accès refusé | REQ-NF-02 |
| 5 | Salarié consulte une demande refusée | Statut et motif visibles au salarié concerné | REQ-F-05, REQ-F-06 |

## Critères d'acceptation
- [ ] Étant donné qu'une demande est en attente, quand le responsable la refuse avec un motif, alors le statut devient « refusée » et le motif est enregistré.
- [ ] Étant donné qu'un responsable n'a pas saisi de motif, quand il tente de refuser la demande, alors le système bloque l'action.
- [ ] Étant donné qu'une demande est déjà traitée, quand le responsable tente de la refuser à nouveau, alors le système empêche cette action.
- [ ] Étant donné qu'une demande est refusée, quand le salarié la consulte, alors il peut voir le motif du refus.

## Questions ouvertes
- Le client souhaite-t-il une liste de motifs prédéfinis ou un texte libre ? Hypothèse provisoire : un champ texte libre obligatoire.

