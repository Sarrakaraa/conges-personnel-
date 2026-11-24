# US-14 - Autoriser une exception à la limite d'absents
En tant que directeur RH, je veux autoriser exceptionnellement jusqu'à 3 salariés absents dans une équipe si le solde du salarié est suffisant afin de gérer certaines situations particulières.
**Exigences liées :** REQ-F-16, RM-03, RM-06, RM-10, REQ-NF-01, REQ-NF-02

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Deux salariés sont déjà absents ; directeur RH autorise un troisième salarié avec solde suffisant | Exception autorisée | REQ-F-16, RM-10 |
| 2 | Trois salariés sont déjà absents ; une nouvelle exception est demandée | Refusée car le maximum de 3 serait dépassé | RM-10 |
| 3 | Solde du salarié insuffisant | Exception refusée | RM-03, RM-10 |
| 4 | Responsable d'équipe tente d'autoriser une exception | Action refusée | REQ-NF-02 |
| 5 | Directeur RH autorise une exception mais le salarié ne remplit pas les autres conditions de congé | Exception de plafond seule ; les autres règles applicables restent à vérifier | RM-10 |

## Critères d'acceptation
- [ ] Étant donné que deux salariés sont absents dans l'équipe et que le salarié possède un solde suffisant, quand le directeur RH autorise l'exception, alors un troisième salarié peut être autorisé conformément à RM-10.
- [ ] Étant donné que l'autorisation ferait dépasser 3 salariés absents, quand le directeur RH tente de l'accorder, alors le système refuse l'exception.
- [ ] Étant donné que le salarié ne possède pas un solde suffisant, quand une exception est demandée, alors elle est refusée.
- [ ] Étant donné qu'un utilisateur n'est pas le directeur RH, quand il tente d'autoriser une exception, alors le système refuse l'action.

## Questions ouvertes
- Une justification doit-elle être saisie pour chaque exception autorisée ? Hypothèse provisoire : oui, le motif est conservé dans l'historique RH.

