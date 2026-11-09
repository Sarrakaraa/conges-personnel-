# Sujet 13 — Demandes de congés du personnel

## Partie 1 — Problème, parties prenantes, objectifs

## Q1 — Problème métier

La gestion actuelle des congés sur papier ne permet pas un suivi fiable : les demandes se perdent et les salariés ne connaissent pas leur solde exact.

Source : « Aujourd'hui, les demandes sur papier se perdent et personne ne connaît son solde exact. »


### Q-2 Parties prenantes

**Explicites :**

- Salarié (60) : demander un congé, voir son solde, obtenir une réponse immédiate.
- Responsable d'équipe (6) : gérer et valider lui-même chaque demande de son équipe.
- Service RH (une gestionnaire et une directrice) : gérer les soldes et suivre les absences.

**Potentielles :**

- Direction générale : non mentionnée dans la demande.
- Service informatique / paie : exploitation, maintenance, sécurité. À présenter comme hypothèse.

### Q3 — Objectifs SMART (sans valeurs inventées)

- OBJ-01 : Centraliser [proportion à valider] des demandes de congés dans le nouveau système dans un délai de [à valider] après la mise en service.

- OBJ-02 : Permettre à [proportion à valider] des salariés de consulter leur solde de congés à jour dans un délai de [à valider] après la mise en service.

- OBJ-03 : Réduire le délai moyen de traitement d'une demande, de [valeur actuelle à mesurer] à [valeur cible à valider], dans les [délai à valider] suivant la mise en service.

- OBJ-04 : Réduire le nombre de situations où le seuil d'absents simultanés d'une équipe est dépassé, de [valeur actuelle à mesurer] à [valeur cible à valider], sur [période à valider].

- OBJ-05 : Réduire le nombre d'annulations de dernière minute, de [valeur actuelle à mesurer] à [valeur cible à valider], sur [période à valider].

- OBJ-06 : Augmenter la proportion de demandes déposées dans le délai de préavis [à valider], de [valeur actuelle à mesurer] à [valeur cible à valider], sur [période à valider].

### Q4 — Objectif difficile à mesurer 

« Les salariés veulent une réponse immédiate » est difficile à mesurer. « Immédiate » est subjectif : instantanée, quelques minutes ou quelques heures ? Elle contredit aussi la validation manuelle par le responsable. Il faut définir avec le client un indicateur (délai maximum de réponse) et une cible : [à valider].

« Le système doit être sécurisé » pose le même problème. Il faut préciser quoi protéger, contre quoi, et avec quels critères vérifiables.

# Partie 2 — Ce que l'on sait et ce que l'on ne sait pas

## Q5 — Tableau de classification

| Élément | Catégorie | Justification |
|---|---|---|
| Demander un congé | Dans le périmètre | Explicitement demandé par le client. |
| Consulter le solde de congés | Dans le périmètre | Les salariés doivent voir leur solde exact. |
| Gérer les demandes de l'équipe | Dans le périmètre | Demandé aux responsables d'équipe. |
| Valider chaque demande | Dans le périmètre | Les responsables souhaitent valider eux-mêmes les demandes. |
| Gérer les soldes | Dans le périmètre | Demandé au service RH. |
| Suivre les absences | Dans le périmètre | Demandé au service RH. |
| Limiter les absences simultanées | Règle métier | Éviter trop d'absences dans une même équipe. |
| Déposer les demandes suffisamment tôt | Règle métier | Le client souhaite anticiper les demandes. |
| Prendre en compte les mariages et décès familiaux | Règle métier | Ce sont des événements imprévisibles. |
| Limiter les annulations tardives | Règle métier | Éviter de pénaliser les autres salariés. |
| Entreprise de 60 salariés répartis en 6 équipes | Contexte / contrainte | Information donnée par le client. |
| Un responsable par équipe | Contexte organisationnel | Information donnée par le client. |
| Une gestionnaire et une directrice RH | Contexte organisationnel | Information donnée par le client. |
| Système sécurisé | BNF | Exigence de sécurité demandée par le client. |
| Chaque salarié possède un compte personnel | Hypothèse | Le mode d'accès n'est pas précisé. |
| Authentification des utilisateurs | Point ouvert | Le mode d'identification n'est pas précisé. |
| Types de congés disponibles | Point ouvert | Les catégories de congés ne sont pas indiquées. |
| Calcul du solde de congés | Point ouvert | Les règles de calcul ne sont pas précisées. |
| Délai minimum de dépôt | Point ouvert | Aucun délai précis n'est donné. |
| Nombre maximal d'absents par équipe | Point ouvert | Aucun nombre n'est indiqué. |
| Conditions d'annulation | Point ouvert | Les règles d'annulation ne sont pas définies. |
| Rôle de la gestionnaire et de la directrice | Point ouvert | La répartition des responsabilités n'est pas précisée. |
| Notifications aux salariés | Point ouvert | Le mode d'information des salariés n'est pas précisé. |

## Q6 — Identifier les éléments hors périmètre

Les éléments suivants ne sont pas justifiés dans le périmètre initial :

- Gestion de la paie.
- Gestion du recrutement.
- Gestion des formations.
- Évaluation des performances des salariés.

**Justification :** Le projet concerne uniquement la dématérialisation et la gestion des demandes de congés du personnel.

## Conclusion

L'analyse du besoin client permet d'identifier les fonctionnalités principales du système, les contraintes et les règles métier. Cependant, plusieurs informations restent à clarifier, notamment les délais de dépôt, le calcul des soldes, le nombre maximal d'absences simultanées et les conditions d'annulation. Ces points devront être discutés avec le client afin de définir des exigences précises et adaptées à ses besoins.

# Partie 3 — — Premières exigences

## Exigences fonctionnelles
—REQ-F-01 — Le système doit permettre à un salarié de soumettre une demande de congé en indiquant une date de début et une date de fin.

—REQ-F-02 — Le système doit permettre à un salarié de consulter son solde de congés.

—REQ-F-03 — Le système doit conserver chaque demande de congé soumise avec son statut (en attente, acceptée, refusée, annulée).

—REQ-F-04 — Le système doit permettre à un responsable d’équipe de consulter les demandes de congé de son équipe.

—REQ-F-05 — Le système doit exiger la décision (acceptation ou refus) du responsable d’équipe pour chaque demande de son équipe.

—REQ-F-06 — Le système doit informer le salarié de la décision du responsable dès que celle-ci est enregistrée.

—REQ-F-07 — Le système doit permettre au service RH de consulter et de modifier le solde de congés de chaque salarié.

—REQ-F-08 — Le système doit permettre au service RH de consulter la liste des absences des salariés.

—REQ-F-09 — Le système doit déduire du solde du salarié les jours d’une demande acceptée.

—REQ-F-10 — Le système doit signaler au responsable d’équipe, lors du traitement d’une demande, si son acceptation ferait dépasser [N] absents simultanés dans l’équipe.

—REQ-F-11 — Le système doit refuser toute demande soumise moins de [X] jours avant la date de début du congé.

—REQ-F-12 — Le système doit permettre à un salarié de soumettre une demande sous le délai minimum en indiquant un motif exceptionnel (ex. mariage, décès).

—REQ-F-13 — Le système doit refuser l’annulation d’un congé accepté moins de [Y] jours avant son début.


## Exigences non fonctionnelles

—REQ-NF-01 — Le système doit exiger l’authentification de chaque utilisateur avant tout accès aux données de congés.

—REQ-NF-02 — Le système doit limiter l’accès aux données selon le rôle : un salarié ne voit que ses propres données, un responsable que celles de son équipe, le service RH celles de tous les salariés.
