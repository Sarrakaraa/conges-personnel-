# US-12 - Bloquer les nouvelles demandes après une annulation tardive
En tant qu'entreprise, je veux bloquer temporairement les nouvelles demandes de congé annuel d'un salarié qui annule tardivement un congé accepté afin de limiter les désorganisations.
**Exigences liées :** REQ-F-13, REQ-F-14, RM-08, RM-09

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Salarié annule une demande acceptée 10 jours avant le début | Annulation sans blocage | RM-09 |
| 2 | Salarié annule une demande acceptée 6 jours avant le début | Blocage de 30 jours | REQ-F-14, RM-09 |
| 3 | Salarié annule une demande en attente | Annulation sans blocage lié à RM-09 | RM-08, RM-09 |
| 4 | Salarié tente une nouvelle demande pendant les 30 jours | Nouvelle demande annuelle bloquée | REQ-F-14 |
| 5 | Blocage arrivé à expiration | Nouvelle demande autorisée si les autres règles sont respectées | RM-09 |

## Critères d'acceptation
- [ ] Étant donné qu'un salarié annule une demande acceptée moins de 7 jours avant le début du congé, quand l'annulation est enregistrée, alors un blocage de 30 jours est appliqué.
- [ ] Étant donné qu'un salarié est bloqué, quand il tente de déposer une nouvelle demande annuelle pendant cette période, alors le système refuse le dépôt.
- [ ] Étant donné que les 30 jours de blocage sont écoulés, quand le salarié dépose une nouvelle demande, alors le système vérifie les autres règles normalement.
- [ ] Étant donné qu'une demande annulée était seulement en attente, quand elle est annulée, alors le blocage prévu pour l'annulation tardive d'une demande acceptée ne s'applique pas.

## Questions ouvertes
- Le blocage concerne-t-il uniquement les congés annuels ou également les congés exceptionnels ? Hypothèse provisoire : uniquement les nouvelles demandes de congé annuel, conformément au texte de REQ-F-14.

