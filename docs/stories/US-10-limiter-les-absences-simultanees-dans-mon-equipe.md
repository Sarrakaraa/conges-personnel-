# US-10 - Limiter les absences simultanées dans mon équipe
En tant qu'entreprise, je veux limiter le nombre de salariés absents simultanément dans une équipe afin de maintenir la continuité du travail.
**Exigences liées :** REQ-F-10, REQ-F-16, RM-06, RM-07, RM-10

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Aucun salarié absent à la date demandée ; un salarié demande un congé | Demande compatible avec le plafond | RM-06 |
| 2 | Un salarié déjà absent ; un deuxième demande un congé le même jour | Demande compatible avec le plafond de 2 | RM-06 |
| 3 | Deux salariés déjà absents ; un troisième demande un congé annuel | Demande refusée | REQ-F-10, RM-06 |
| 4 | Demande sur plusieurs jours, plafond dépassé sur un seul des jours | Demande entière refusée | RM-06 |
| 5 | Directeur RH autorise une exception portant l'effectif absent à 3 | Exception autorisée si les conditions de RM-10 sont respectées | REQ-F-16, RM-10 |
| 6 | Congé exceptionnel accepté pendant une journée déjà chargée | Le salarié compte dans les absences, même si RM-07 écarte le plafond pour sa demande exceptionnelle | RM-07 |

## Critères d'acceptation
- [ ] Étant donné que deux salariés de l'équipe sont déjà absents le même jour, quand un troisième salarié demande un congé annuel couvrant cette date, alors la demande est refusée.
- [ ] Étant donné qu'une demande couvre plusieurs jours, quand le système vérifie les effectifs, alors il contrôle chaque jour de la période.
- [ ] Étant donné que le directeur RH autorise une exception et que le nombre total d'absents ne dépasse pas 3, quand l'exception est appliquée, alors la demande peut être traitée selon RM-10.
- [ ] Étant donné qu'un salarié bénéficie d'un congé exceptionnel, quand le planning est calculé, alors il est compté dans les absences de l'équipe.

## Questions ouvertes
- Quand plusieurs demandes sont déposées presque simultanément, dans quel ordre le système doit-il les traiter pour appliquer le plafond ? Hypothèse provisoire : traiter les demandes dans l'ordre de dépôt et recalculer le nombre d'absents après chaque décision.

