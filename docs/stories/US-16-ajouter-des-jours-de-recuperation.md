# US-16 - Ajouter des jours de récupération
En tant que membre du service RH autorisé, je veux ajouter des jours de récupération au solde d'un salarié afin de mettre à jour ses droits.
**Exigences liées :** REQ-F-07, RM-03, REQ-NF-01, REQ-NF-02

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | RH ajoute 1 jour de récupération | Solde augmenté d'un jour | REQ-F-07 |
| 2 | RH ajoute 3 jours de récupération | Solde augmenté de 3 jours | REQ-F-07 |
| 3 | Salarié tente d'ajouter lui-même des jours | Action refusée | REQ-NF-02 |
| 4 | RH saisit une quantité négative | Saisie refusée | REQ-F-07 |
| 5 | RH ajoute des jours à un salarié inexistant ou non importé | Opération refusée | REQ-F-07 |

## Critères d'acceptation
- [ ] Étant donné qu'un membre RH autorisé sélectionne un salarié, quand il ajoute un nombre positif de jours de récupération, alors le solde est augmenté de ce nombre de jours.
- [ ] Étant donné qu'un utilisateur salarié tente d'ajouter des jours, quand il valide l'action, alors le système refuse l'accès.
- [ ] Étant donné qu'une quantité nulle ou négative est saisie, quand le formulaire est validé, alors le système refuse l'opération.
- [ ] Étant donné que des jours sont ajoutés, quand le salarié consulte son solde, alors le nouveau solde disponible est pris en compte.

## Questions ouvertes
- Les jours de récupération ont-ils une date d'expiration ou une période de validité ? Hypothèse provisoire : ils restent disponibles jusqu'à utilisation, en attendant la règle RH.

