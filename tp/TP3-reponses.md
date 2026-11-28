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

## Q4 --- Les classes et leurs attributs

### a) Les attributs de la classe Salarié

  Attribut          Source / justification
  ----------------- ------------------------------------------------------------
  Nom               Informations du salarié importées depuis le fichier RH.
  Type de contrat   Seuls les salariés en CDI ou CDD sont concernés.
  Équipe            Informations d'affectation importées depuis le fichier RH.
  Solde de congés   Permet au salarié de consulter son solde.

### b) Les attributs des classes DemandeConge et Salarié

**Classe DemandeConge :**

  Attribut       Règle qui le justifie
  -------------- -------------------------------------------------
  dateDebut      Règle de dépôt et calcul des jours de congé.
  dateFin        Calcul de la durée du congé.
  typeConge      Distinction entre congé annuel et exceptionnel.
  nombreJours    Calcul des jours ouvrables concernés.
  statut         Acceptation, refus ou attente de validation.
  dateCreation   Vérification du préavis de 7 jours.

**Classe Salarié :**

  Attribut      Règle qui le justifie
  ------------- ----------------------------------------------------
  nom           Identification du salarié.
  typeContrat   Seuls les CDI et CDD sont concernés.
  equipe        Application de la limite des absences simultanées.
  soldeConge    Vérification du solde disponible.
  estBloque     Blocage de 30 jours après une annulation tardive.

## Q5 --- Les associations

### a) Les multiplicités

-   Un salarié fait **0..**\* demandes de congé.
-   Une demande de congé est faite par **1** salarié.
-   Un responsable gère **0..**\* demandes.
-   Une demande est traitée par **0..1** responsable.

La classe DemandeConge est séparée, car elle possède ses propres
informations : dates, type, nombre de jours et statut. Un salarié peut
effectuer plusieurs demandes au cours du temps.

## Q6 --- Lire l'exemple GET du document du professeur

### a) Où se trouvent les données envoyées et les réponses possibles ?

Les données envoyées par l'enseignant se trouvent dans `parameters`,
avec les paramètres `date`, `debut` et `fin`, placés dans l'adresse
grâce à `in: query`.

Les réponses possibles se trouvent dans `responses`, avec les codes HTTP
`200` et `400`.

### b) Que reçoit l'enseignant si l'heure de fin est avant l'heure de début ?

Il reçoit le code HTTP **400 (Bad Request)** avec un objet `Erreur`
contenant un message qui explique le problème, par exemple : « L'heure
de fin doit être après l'heure de début. »

### c) À quoi sert `$ref: "#/components/schemas/Salle"` ?

Cette ligne permet de réutiliser le schéma `Salle` défini dans
`components/schemas`, sans réécrire ses attributs à chaque utilisation.

## Q7 --- Le contrat d'API de POST

### c) Une même demande peut-elle recevoir 409 aujourd'hui et 201 demain ? Et 400 aujourd'hui et 201 demain ?

**409 aujourd'hui et 201 demain : oui.** Une demande correcte peut être
refusée temporairement à cause de l'état actuel du système. Par exemple,
une demande de congé peut être refusée parce que la limite d'absences de
l'équipe est atteinte. Si une autre demande est annulée, la même demande
peut ensuite être acceptée.

**400 aujourd'hui et 201 demain : non.** Le code 400 indique que la
demande elle-même ne respecte pas une règle, par exemple des dates
invalides ou un préavis non respecté. Il faut corriger la demande avant
de la soumettre à nouveau.

## Q8 --- Lire l'exemple du diagramme de séquence

### a) Quels sont les quatre participants ? Pourquoi l'enseignant n'envoie-t-il jamais de message au Dépôt ?

Les quatre participants sont : l'enseignant, l'API, le Service et le
Dépôt.

L'enseignant ne communique pas directement avec le Dépôt, car
l'architecture est organisée en couches. Il communique avec l'API, qui
transmet la demande au Service. Seul le Service communique avec le
Dépôt.

### b) Que représentent les flèches pleines et les flèches en pointillés ?

-   **Flèche pleine :** elle représente un message ou une demande
    envoyée à un participant.
-   **Flèche en pointillés :** elle représente une réponse retournée par
    un participant.

### c) Si la fin est avant le début, le Dépôt est-il appelé ?

Non. Le Service vérifie les dates et les horaires avant de consulter le
Dépôt. Le cadre `break` montre que le scénario s'arrête dès que la
condition d'erreur est vérifiée.

## Q9 --- Préparer le scénario de US-02

### a) Tableau des messages

Pour notre projet, le scénario choisi est la soumission d'une demande de
congé annuel.

  --------------------------------------------------------------------------------------------------
  Étape             Qui envoie        Qui reçoit        Message
  ----------------- ----------------- ----------------- --------------------------------------------
  1                 Salarié           API               POST /demandes-conge

  2                 API               Service           soumettreDemande(salarié, dateDebut,
                                                        dateFin)

  3                 Service           Service           Vérifier les dates et calculer les jours
                                                        ouvrables

  4                 Service           Service           Vérifier le préavis de 7 jours

  5                 Service           Dépôt             lireSalarie(salarié)

  6                 Dépôt             Service           Retourner les informations du salarié

  7                 Service           Dépôt             lireBlocageEtSolde(salarié)

  8                 Dépôt             Service           Retourner le blocage et le solde disponible

  9                 Service           Dépôt             lireAbsencesEquipe(equipe, dateDebut,
                                                        dateFin)

  10                Dépôt             Service           Retourner les absences et demandes en
                                                        attente

  11                Service           Service           Déterminer le statut de la demande

  12                Service           Dépôt             enregistrerDemandeEtReserverJours(demande)

  13                Dépôt             Service           Confirmer l'enregistrement

  14                Service           API               Retourner la demande créée et son statut

  15                API               Salarié           201 --- Demande créée
  --------------------------------------------------------------------------------------------------

### b) Les trois principaux arrêts du scénario

1.  **Dates invalides ou préavis non respecté :** le système retourne le
    code **400**.
2.  **Salarié hors du périmètre (contrat différent de CDI ou CDD) :** le
    système retourne le code **403**.
3.  **Solde insuffisant, salarié bloqué ou limite d'absences dépassée
    :** le système retourne le code **409**.

## Q11 --- Pourquoi la vérification est-elle faite par le Service et non par l'API ?

Le Service vérifie les règles métier, car l'API reçoit les requêtes HTTP
et transmet les demandes, tandis que le Service applique les règles et
prend les décisions métier.
