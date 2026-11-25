# TP2 — Réponses, partie 4 : Prioriser le backlog

## Q7 — Priorités

Les priorités ont été attribuées selon l'importance des fonctionnalités pour disposer d'une première version utilisable.

- **Must :** US-01, US-02, US-07, US-08, US-09, US-10, US-11, US-15 et US-20.
- **Should :** US-03, US-04, US-05, US-06, US-12, US-13, US-14, US-16, US-18 et US-19.
- **Could :** US-17.
- **Won't :** US-21.

Il y a 9 stories Must sur 21, donc moins de la moitié du backlog.

La story « Ajouter une salle » de l'exemple de correction ne figure pas dans notre projet, qui porte sur les demandes de congés du personnel. Elle n'est donc pas applicable. Pour notre sujet, l'importation des employés depuis un fichier RH (US-20) est classée **Must**, car elle permet d'initialiser les employés, leurs équipes, leurs contrats et leurs soldes. La story de report des jours non utilisés (US-21) est classée **Won't**, car ce point reste une question ouverte dans les exigences et ne sera pas inclus dans la première version.

La story « Réservations répétées (R7) » de l'autre sujet ne correspond pas non plus à notre application. Elle est remplacée par US-21, qui reprend une demande réellement liée à notre sujet et qui reste visible dans le backlog.

## Q8 — Stories prêtes

Une story est considérée comme prête si elle possède une priorité, au moins deux critères d'acceptation et aucune question ouverte qui empêche de commencer son développement.

### Stories non prêtes et éléments manquants

| User Story | Ce qui manque / question à clarifier |
|---|---|
| US-01 | Confirmer si le délai de 7 jours est calculé en jours calendaires ou ouvrables et confirmer le cas d'une demande déposée exactement 7 jours avant. |
| US-03 | Déterminer le canal de notification de l'employé (application, e-mail ou autre). |
| US-05 | Confirmer si un justificatif est obligatoire pour un congé exceptionnel. |
| US-08 | Confirmer le contrôle de la limite d'absents au moment où le responsable accepte la demande. |
| US-10 | Définir l'ordre de traitement des demandes déposées presque simultanément pour appliquer la limite d'absents. |
| US-11 | Confirmer si le délai de 7 jours correspond à des jours calendaires ou ouvrables. |
| US-15 | Définir le calcul du solde pour les salariés qui arrivent ou quittent l'entreprise en cours d'année (proratisation). |
| US-16 | Définir la date d'expiration ou la durée de validité des jours de récupération. |
| US-17 | Préciser les informations à afficher pour chaque mouvement du solde (date, type, quantité, auteur, référence). |
| US-18 | Confirmer si la liste RH doit inclure les demandes en attente ou uniquement les absences confirmées, et comment les distinguer. |
| US-19 | Préciser les opérations autorisées sur les jours fériés : ajout, modification et suppression. |
| US-20 | Définir le format du fichier RH accepté et les colonnes obligatoires. |


Les autres stories sont considérées comme prêtes pour commencer : elles ont une priorité, au moins deux critères d'acceptation et leurs questions ouvertes ne bloquent pas la réalisation de la fonctionnalité principale dans le cadre des exigences actuelles.

## Stories prêtes:
US-02
US-04
US-06
US-07
US-09
US-12
US-13
US-14