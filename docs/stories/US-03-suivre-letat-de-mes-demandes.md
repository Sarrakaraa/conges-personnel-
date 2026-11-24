# US-03 - Suivre l'état de mes demandes
En tant que salarié, je veux consulter l'état de mes demandes de congé afin de savoir si elles sont en attente, acceptées, refusées ou annulées.
**Exigences liées :** REQ-F-03, REQ-F-06, REQ-NF-01, REQ-NF-02

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Le salarié consulte une demande nouvellement déposée | Statut « en attente » ou statut automatique correspondant | REQ-F-03 |
| 2 | Le responsable accepte une demande en attente | Statut « acceptée » | REQ-F-03, REQ-F-06 |
| 3 | Le responsable refuse une demande avec motif | Statut « refusée » et motif consultable | REQ-F-03, REQ-F-05 |
| 4 | Le salarié annule une demande | Statut « annulée » | REQ-F-03, REQ-F-13 |
| 5 | Le salarié consulte les demandes d'un autre salarié | Accès refusé | REQ-NF-02 |

## Critères d'acceptation
- [ ] Étant donné qu'un salarié est authentifié, quand il ouvre ses demandes, alors le système affiche ses demandes avec leur statut.
- [ ] Étant donné qu'une décision est enregistrée, quand le salarié consulte la demande concernée, alors le nouveau statut est affiché.
- [ ] Étant donné qu'une demande est refusée, quand le salarié consulte son détail, alors le motif de refus est visible lorsqu'il est requis.
- [ ] Étant donné qu'un salarié tente de consulter les demandes d'un autre salarié, quand il accède à cette page, alors l'accès est refusé.

## Questions ouvertes
- Par quel canal le salarié doit-il être informé du changement de statut (notification dans l'application, e-mail ou autre) ? Hypothèse provisoire : le statut est toujours visible dans l'application ; le canal de notification externe reste à confirmer.

