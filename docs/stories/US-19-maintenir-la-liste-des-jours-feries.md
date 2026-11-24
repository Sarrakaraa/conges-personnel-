# US-19 - Maintenir la liste des jours fériés
En tant que membre du service RH autorisé, je veux gérer la liste des jours fériés afin que le calcul des jours ouvrables soit correct.
**Exigences liées :** REQ-F-19, RM-02, REQ-NF-01, REQ-NF-02

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | RH ajoute un jour férié à la liste | Jour férié enregistré | REQ-F-19 |
| 2 | RH consulte la liste des jours fériés | Liste affichée | REQ-F-19 |
| 3 | RH tente d'ajouter deux fois la même date | Doublon à empêcher ou signaler | REQ-F-19 |
| 4 | Un salarié tente de modifier la liste | Action refusée | REQ-NF-02 |
| 5 | Une demande couvre une date déclarée fériée | Cette date n'est pas comptée comme jour ouvrable | RM-02 |

## Critères d'acceptation
- [ ] Étant donné qu'un membre RH autorisé ajoute une date comme jour férié, quand il valide l'opération, alors cette date est enregistrée dans la liste.
- [ ] Étant donné qu'une date figure dans la liste des jours fériés, quand le système calcule la durée d'un congé, alors cette date n'est pas comptée comme jour ouvrable.
- [ ] Étant donné qu'un utilisateur ne possède pas les droits RH, quand il tente de modifier la liste, alors le système refuse l'action.
- [ ] Étant donné qu'une date existe déjà dans la liste, quand RH tente de l'ajouter une seconde fois, alors le système signale le doublon.

## Questions ouvertes
- La gestion des jours fériés comprend-elle l'ajout, la modification et la suppression ? Hypothèse provisoire : les trois opérations sont possibles pour le service RH autorisé.

