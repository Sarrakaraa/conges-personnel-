# US-07 - Consulter les demandes et le planning de mon équipe
En tant que responsable d'équipe, je veux consulter les demandes de congé et le planning des absences de mon équipe afin d'organiser le travail.
**Exigences liées :** REQ-F-04, REQ-F-03, REQ-NF-01, REQ-NF-02, RM-06, RM-07

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Responsable consulte le planning de sa propre équipe | Planning affiché | REQ-F-04 |
| 2 | Responsable tente de consulter une autre équipe | Accès refusé | REQ-NF-02 |
| 3 | Planning avec une demande en attente | Demande visible et comptée dans le plafond d'absences | RM-06 |
| 4 | Planning avec une absence exceptionnelle acceptée | Absence visible et salarié compté dans l'effectif absent | RM-07 |
| 5 | Utilisateur non authentifié consulte le planning | Authentification requise | REQ-NF-01 |

## Critères d'acceptation
- [ ] Étant donné qu'un responsable est authentifié, quand il consulte son équipe, alors le système affiche les demandes et les absences de cette équipe.
- [ ] Étant donné qu'un responsable appartient à une équipe, quand il tente d'afficher les données d'une autre équipe sans autorisation, alors l'accès est refusé.
- [ ] Étant donné qu'une demande est en attente, quand le planning est affiché, alors cette demande est prise en compte dans le calcul des absences conformément à RM-06.
- [ ] Étant donné qu'un congé exceptionnel est accepté, quand le planning est affiché, alors l'absence apparaît dans le planning.

## Questions ouvertes
- Le responsable doit-il voir le motif détaillé des congés exceptionnels ou seulement les dates d'absence ? Hypothèse provisoire : afficher les dates et le type de congé, sans exposer de détails personnels non nécessaires.

