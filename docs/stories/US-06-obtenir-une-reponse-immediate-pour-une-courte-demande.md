# US-06 - Obtenir une réponse immédiate pour une courte demande
En tant que salarié, je veux obtenir une réponse automatique pour une demande de congé annuel de courte durée afin de ne pas attendre une validation manuelle lorsque les règles sont respectées.
**Exigences liées :** REQ-F-03, REQ-F-06, REQ-F-17, RM-02, RM-03, RM-04, RM-05, RM-06, RM-11

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Demande de 1 jour ouvrable avec toutes les règles respectées | Acceptée automatiquement | REQ-F-17, RM-11 |
| 2 | Demande de 2 jours ouvrables avec toutes les règles respectées | Acceptée automatiquement | RM-11 |
| 3 | Demande de 3 jours ouvrables avec toutes les règles respectées | Mise en attente pour décision du responsable | RM-11 |
| 4 | Demande de 2 jours mais solde insuffisant | Refusée automatiquement | RM-05, RM-11 |
| 5 | Demande de 2 jours déposée moins de 7 jours avant le début | Refusée automatiquement | RM-04, RM-11 |
| 6 | Demande de 2 jours dépassant le plafond d'absences | Refusée automatiquement | RM-06, RM-11 |

## Critères d'acceptation
- [ ] Étant donné qu'une demande annuelle porte sur 1 ou 2 jours ouvrables et respecte toutes les règles, quand elle est soumise, alors elle est acceptée automatiquement.
- [ ] Étant donné qu'une demande annuelle porte sur plus de 2 jours ouvrables, quand elle est soumise et respecte les règles automatiques, alors elle passe au statut « en attente ».
- [ ] Étant donné qu'une demande courte ne respecte pas une règle obligatoire, quand elle est soumise, alors elle n'est pas acceptée automatiquement et le système applique la règle de refus concernée.
- [ ] Étant donné qu'une décision automatique est prise, quand elle est enregistrée, alors le salarié est informé du résultat conformément à REQ-F-06.

## Questions ouvertes
- Le système doit-il afficher explicitement que la décision est automatique ? Hypothèse provisoire : oui, le statut et le message doivent indiquer que la demande a été acceptée automatiquement.

