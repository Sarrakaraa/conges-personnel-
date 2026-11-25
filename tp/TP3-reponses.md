# TP3 — Réponses Sujet 13 — Demandes de congés du personnel

## Q1 — Les acteurs

### a) Qui utilise le système ?

Le système est utilisé par quatre acteurs.

- **Employé** : il est montré par US-01 : « En tant qu'employé, je veux soumettre une demande de congé annuel… ».
- **Responsable d'équipe** : il est montré par US-08 : « En tant que responsable d'équipe, je veux accepter une demande en attente… ».
- **Service RH** : il est montré par US-15 : « En tant que service RH, je veux saisir le solde initial d'un employé… ».
- **Directrice RH** : elle est montrée par US-13 : « En tant que directrice RH, je veux lever le blocage de 30 jours… ».

### b) Ce qui n'est pas un acteur

- **Direction générale** : elle n'apparaît dans aucune story.
- **Service informatique** : aucune story ne lui donne d'objectif.
- **Base de données** : elle fait partie du système et elle n'a aucun objectif.

## Q2 — Les cas d'utilisation

### a) Cas d'utilisation par acteur

**Employé**
- Soumettre une demande de congé annuel (US-01)
- Consulter mon solde de congés (US-02)
- Suivre l'état de mes demandes (US-03)
- Annuler ma demande de congé (US-04)
- Demander un congé exceptionnel (US-05)

**Responsable d'équipe**
- Consulter les demandes et le planning de l'équipe (US-07)
- Accepter une demande en attente (US-08)
- Refuser une demande avec un motif (US-09)

**Service RH**
- Saisir le solde initial d'un employé (US-15)
- Ajouter des jours de récupération (US-16)
- Consulter l'historique des mouvements d'un solde (US-17)
- Consulter la liste des absences (US-18)
- Maintenir la liste des jours fériés (US-19)
- Importer les employés depuis un fichier RH (US-20)

**Directrice RH**
- Lever le blocage de 30 jours (US-13)
- Autoriser une exception à la limite d'absents (US-14)

**Stories qui ne deviennent pas des cas d'utilisation :** US-06, US-10, US-11 et US-12. Ce sont des vérifications faites par le système, pas des objectifs d'un acteur. US-06 (acceptation automatique des demandes de 2 jours ou moins), US-10 (limite d'absents) et US-11 (préavis de 7 jours) sont des règles à l'intérieur de « Soumettre une demande de congé annuel ». US-12 (blocage de 30 jours) est une conséquence de « Annuler ma demande de congé ».

### b) Quelle proposition est un cas d'utilisation ?

**« Annuler une demande de congé »** est un cas d'utilisation : c'est un objectif de l'employé, qui lui apporte quelque chose (libérer ses jours).

**« Saisir la date de début dans le formulaire »** n'en est pas un : c'est une étape à l'intérieur de « Soumettre une demande de congé annuel ».

**« Vérifier la limite d'absents de l'équipe »** n'en est pas un : c'est le système qui le fait, pas l'acteur.
