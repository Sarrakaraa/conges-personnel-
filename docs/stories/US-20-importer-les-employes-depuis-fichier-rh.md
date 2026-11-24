# US-20 - Importer les employés depuis un fichier RH
En tant que membre du service RH autorisé, je veux importer les employés, leurs contrats, leurs équipes et leurs soldes initiaux depuis un fichier RH afin d'initialiser le système sans ressaisie manuelle.
**Exigences liées :** REQ-F-18, RM-01, RM-12, REQ-NF-01, REQ-NF-02

## Exemples
| # | Situation / demande | Décision attendue | Règle / exigence |
|---:|---|---|---|
| 1 | Fichier valide contenant des salariés en CDI et CDD avec les champs requis | Import accepté | REQ-F-18, RM-12 |
| 2 | Fichier contenant un salarié sans équipe renseignée | Ligne signalée comme invalide ou import partiel à confirmer | REQ-F-18 |
| 3 | Fichier contenant un type de contrat autre que CDI ou CDD | Salarié exclu de la version 1 | RM-12 |
| 4 | Fichier au format non pris en charge | Import refusé | REQ-F-18 |
| 5 | Utilisateur sans rôle RH tente un import | Accès refusé | REQ-NF-02 |
| 6 | Fichier contenant un salarié déjà importé | Doublon à détecter et signaler | REQ-F-18 |

## Critères d'acceptation
- [ ] Étant donné qu'un membre RH autorisé fournit un fichier au format accepté contenant les champs requis, quand il lance l'import, alors les employés, contrats, équipes et soldes sont enregistrés.
- [ ] Étant donné qu'un fichier ne respecte pas le format attendu, quand l'import est lancé, alors le système le refuse et indique l'erreur.
- [ ] Étant donné qu'une ligne concerne un contrat autre que CDI ou CDD, quand le fichier est traité, alors cette ligne n'est pas intégrée dans le périmètre de la version 1.
- [ ] Étant donné qu'un utilisateur n'a pas les droits RH, quand il tente un import, alors le système refuse l'accès.

## Questions ouvertes
- Quel format de fichier et quelles colonnes exactes le client RH fournira-t-il ? Hypothèse provisoire : fichier CSV ou Excel avec identifiant, nom, prénom, équipe, type de contrat et solde initial.


