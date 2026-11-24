# US-15 - Saisir le solde initial
En tant que membre du service RH autorisé, je veux saisir le solde initial d'un salarié afin que le système puisse calculer ses jours disponibles.
**Exigences liées :** REQ-F-07, REQ-F-18, RM-01, RM-03, RM-12, REQ-NF-01, REQ-NF-02

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | RH saisit le solde initial d'un salarié éligible | Solde enregistré | REQ-F-07 |
| 2 | RH saisit 26 jours pour un salarié éligible sur une année complète | Solde conforme à RM-01 | RM-01 |
| 3 | Utilisateur salarié tente de modifier le solde initial | Action refusée | REQ-NF-02 |
| 4 | Solde initial saisi avec une valeur négative | Saisie refusée | REQ-F-07 |
| 5 | Solde initial saisi pour un salarié hors CDI/CDD | Hors périmètre de la version 1 | RM-12 |

## Critères d'acceptation
- [ ] Étant donné qu'un membre RH autorisé sélectionne un salarié éligible, quand il saisit son solde initial, alors le système enregistre ce solde.
- [ ] Étant donné qu'un utilisateur n'a pas le rôle RH autorisé, quand il tente de saisir un solde, alors l'accès est refusé.
- [ ] Étant donné qu'une valeur de solde négative est saisie, quand le formulaire est validé, alors le système refuse cette valeur.
- [ ] Étant donné qu'un solde initial est enregistré, quand le salarié consulte son solde, alors le calcul tient compte de cette valeur.

## Questions ouvertes
- Le solde annuel de 26 jours doit-il être proratisé pour les salariés qui arrivent ou quittent l'entreprise en cours d'année ? Hypothèse provisoire : appliquer 26 jours conformément à RM-01 tant que la règle de proratisation n'est pas définie.

