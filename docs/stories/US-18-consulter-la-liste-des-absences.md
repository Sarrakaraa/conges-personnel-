# US-18 - Consulter la liste des absences
En tant que membre du service RH autorisé, je veux consulter la liste des absences des salariés afin de suivre les absences dans l'entreprise.
**Exigences liées :** REQ-F-08, REQ-F-03, REQ-NF-01, REQ-NF-02, RM-02, RM-07

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | RH consulte les absences de tous les salariés | Liste affichée | REQ-F-08 |
| 2 | RH filtre les absences par équipe | Résultats limités à l'équipe choisie | REQ-F-08 |
| 3 | Liste comprend des congés acceptés | Absences affichées | REQ-F-08 |
| 4 | Demande encore en attente | Ne doit pas être présentée comme une absence confirmée | REQ-F-03 |
| 5 | Salarié tente d'accéder à la liste RH complète | Accès refusé selon les droits | REQ-NF-02 |

## Critères d'acceptation
- [ ] Étant donné qu'un membre RH est authentifié et autorisé, quand il ouvre la liste des absences, alors le système affiche les absences des salariés.
- [ ] Étant donné qu'une demande est seulement en attente, quand la liste des absences confirmées est consultée, alors elle est distinguée des absences acceptées.
- [ ] Étant donné qu'un membre RH sélectionne une équipe, quand il applique le filtre, alors seules les absences de cette équipe sont affichées si le filtre est prévu.
- [ ] Étant donné qu'un utilisateur ne possède pas les droits nécessaires, quand il tente d'accéder à la liste RH, alors l'accès est refusé.

## Questions ouvertes
- La liste RH doit-elle inclure les demandes en attente en plus des absences confirmées ? Hypothèse provisoire : afficher deux états distincts afin de ne pas confondre une demande et une absence confirmée.


