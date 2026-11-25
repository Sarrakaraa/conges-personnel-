# Product Backlog — Sujet 13 : Demandes de congés du personnel

| ID | Titre | Exigences liées | Priorité | Prêt ? |
|---|---|---|---|---|
| US-01 | Soumettre une demande de congé annuel | REQ-F-01, REQ-F-03, REQ-F-09, REQ-F-10, REQ-F-11, REQ-F-17 | Must | Non |
| US-02 | Consulter mon solde de congés | REQ-F-02, REQ-F-09 | Must | Oui |
| US-03 | Suivre l'état de mes demandes | REQ-F-03, REQ-F-06 | Should | Non |
| US-04 | Annuler ma demande de congé | REQ-F-13, REQ-F-09, REQ-F-14 | Should | Oui |
| US-05 | Demander un congé exceptionnel | REQ-F-12 | Should | Non |
| US-06 | Obtenir une réponse immédiate pour une courte demande | REQ-F-17, RM-11 | Should | Oui |
| US-07 | Consulter les demandes et le planning de mon équipe | REQ-F-04 | Must | Oui |
| US-08 | Accepter une demande en attente | REQ-F-05 | Must | Non |
| US-09 | Refuser une demande avec un motif | REQ-F-05 | Must | Oui |
| US-10 | Limiter les absences simultanées dans mon équipe | REQ-F-10, RM-06, RM-10 | Must | Non |
| US-11 | Refuser les demandes déposées trop tard | REQ-F-11, RM-04 | Must | Non |
| US-12 | Bloquer les nouvelles demandes après une annulation tardive | REQ-F-14, RM-09 | Should | Oui |
| US-13 | Lever le blocage de 30 jours | REQ-F-15, REQ-NF-02 | Should | Oui |
| US-14 | Autoriser une exception à la limite d'absents | REQ-F-16, RM-10 | Should | Oui |
| US-15 | Saisir le solde initial d'un employé | REQ-F-07, RM-01, RM-03 | Must | Non |
| US-16 | Ajouter des jours de récupération | REQ-F-07 | Should | Non |
| US-17 | Consulter l'historique des mouvements d'un solde | REQ-F-07, RM-03 | Could | Non |
| US-18 | Consulter la liste des absences | REQ-F-08 | Should | Non |
| US-19 | Maintenir la liste des jours fériés | REQ-F-19, RM-02 | Should | Non |
| US-20 | Importer les employés depuis un fichier RH | REQ-F-18, RM-12 | Must | Non |

## Justification générale des priorités

- **Must :** fonctionnalités indispensables au fonctionnement initial : déposer une demande, consulter son solde, permettre au responsable de consulter et traiter les demandes, appliquer les règles essentielles de disponibilité et de délai, initialiser les soldes et importer les données RH.
- **Should :** fonctionnalités importantes pour compléter la gestion quotidienne : suivi et annulation des demandes, congés exceptionnels, réponse automatique, blocage après annulation tardive, exceptions RH, récupération, absences et jours fériés.
- **Could :** l'historique détaillé des mouvements est utile pour le suivi RH, mais peut être ajouté après les fonctionnalités principales.
- **Won't :** le report des jours non utilisés n'est pas inclus dans la v1, car les exigences le signalent encore comme une question ouverte. La story reste visible dans le backlog pour ne pas oublier cette demande.
