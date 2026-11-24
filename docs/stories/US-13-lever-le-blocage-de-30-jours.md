# US-13 - Lever le blocage de 30 jours
En tant que directeur RH, je veux lever le blocage de 30 jours appliqué à un salarié afin de lui permettre de déposer une nouvelle demande annuelle avant la fin du blocage.
**Exigences liées :** REQ-F-15, REQ-F-14, RM-09, REQ-NF-01, REQ-NF-02

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Directeur RH lève le blocage d'un salarié | Blocage levé | REQ-F-15 |
| 2 | Responsable d'équipe tente de lever le blocage | Action refusée | REQ-NF-02 |
| 3 | Salarié tente de lever son propre blocage | Action refusée | REQ-NF-02 |
| 4 | Directeur RH tente de lever un blocage inexistant | Aucune modification ; message adapté | REQ-F-15 |
| 5 | Directeur RH lève le blocage avant son expiration | Le salarié peut déposer une demande annuelle, sous réserve des autres règles | REQ-F-15 |

## Critères d'acceptation
- [ ] Étant donné qu'un salarié possède un blocage actif, quand le directeur RH le lève, alors le blocage devient inactif.
- [ ] Étant donné qu'un responsable d'équipe n'a pas le droit de lever un blocage, quand il tente cette action, alors le système refuse l'accès.
- [ ] Étant donné qu'un salarié est débloqué, quand il dépose une demande annuelle, alors les règles habituelles sont vérifiées.
- [ ] Étant donné qu'aucun blocage n'est actif, quand le directeur RH demande sa levée, alors le système indique qu'aucun blocage n'est à lever.

## Questions ouvertes
- Le directeur RH doit-il saisir un motif obligatoire lorsqu'il lève un blocage ? Hypothèse provisoire : oui, afin de conserver une trace de la décision.


