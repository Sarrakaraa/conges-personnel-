# US-11 - Refuser les demandes déposées trop tard
En tant qu'entreprise, je veux refuser automatiquement les demandes de congé annuel déposées moins de 7 jours avant le début afin de faciliter l'organisation du travail.
**Exigences liées :** REQ-F-11, REQ-F-01, RM-02, RM-04

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Demande déposée 10 jours avant le premier jour ouvrable | Délai respecté | RM-04 |
| 2 | Demande déposée exactement 7 jours avant le premier jour ouvrable | Délai considéré respecté selon l'hypothèse | RM-04 |
| 3 | Demande déposée 6 jours avant le premier jour ouvrable | Refusée automatiquement | REQ-F-11, RM-04 |
| 4 | Le début demandé tombe un samedi ; le premier jour ouvrable est le lundi | Le calcul du délai se réfère au premier jour ouvrable | RM-04 |
| 5 | Période demandée commence un jour férié ; le jour suivant est ouvrable | Le premier jour ouvrable sert de référence au délai | RM-02, RM-04 |

## Critères d'acceptation
- [ ] Étant donné qu'une demande est déposée au moins 7 jours avant le premier jour ouvrable du congé, quand le système vérifie le délai, alors cette règle est respectée.
- [ ] Étant donné qu'une demande est déposée moins de 7 jours avant le premier jour ouvrable du congé, quand elle est soumise, alors le système la refuse automatiquement.
- [ ] Étant donné que la date de début tombe un jour non ouvrable, quand le système calcule le délai, alors il utilise le premier jour ouvrable du congé comme référence.

## Questions ouvertes
- Le délai de 7 jours est-il exprimé en jours calendaires ou en jours ouvrables ? Hypothèse provisoire : jours calendaires, à confirmer avec le client.


