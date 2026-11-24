# US-17 - Consulter l'historique du solde
En tant que membre du service RH autorisé, je veux consulter l'historique des mouvements du solde d'un salarié afin de suivre les ajouts et les déductions.
**Exigences liées :** REQ-F-07, RM-03, REQ-NF-01, REQ-NF-02

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | RH consulte l'historique d'un salarié avec plusieurs mouvements | Mouvements affichés | REQ-F-07 |
| 2 | Historique contient solde initial et jours de récupération | Les deux opérations sont visibles | REQ-F-07 |
| 3 | Historique contient réservation de jours pour une demande en attente | Mouvement de réservation visible ou reflété dans le détail | RM-03 |
| 4 | Salarié tente de consulter l'historique RH détaillé d'un autre salarié | Accès refusé | REQ-NF-02 |
| 5 | Aucun mouvement n'existe encore | Historique vide avec indication adaptée | REQ-F-07 |

## Critères d'acceptation
- [ ] Étant donné qu'un membre RH autorisé sélectionne un salarié, quand il ouvre l'historique, alors le système affiche les mouvements enregistrés.
- [ ] Étant donné qu'un solde initial ou des jours de récupération ont été enregistrés, quand l'historique est consulté, alors ces opérations apparaissent.
- [ ] Étant donné qu'une demande réserve ou libère des jours, quand l'historique est consulté, alors le mouvement correspondant peut être retracé.
- [ ] Étant donné qu'un utilisateur n'a pas les droits RH requis, quand il tente d'accéder à l'historique, alors le système refuse l'accès.

## Questions ouvertes
- Quelles informations doivent apparaître pour chaque mouvement (date, quantité, type, auteur, référence de demande) ? Hypothèse provisoire : date, type de mouvement, nombre de jours et référence associée.


