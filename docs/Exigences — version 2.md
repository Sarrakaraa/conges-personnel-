# Exigences — version 2

## Exigences fonctionnelles

- **REQ-F-01** — Le système doit permettre à un employé de soumettre une demande de congé avec une date de début et une date de fin. *(inchangée)*
- **REQ-F-02** — Le système doit permettre à un employé de consulter son solde de congés disponible, en tenant compte des demandes acceptées et en attente. *(modifiée — R1)*
- **REQ-F-03** — Le système doit enregistrer chaque demande de congé avec son statut : en attente, acceptée, refusée ou annulée. *(inchangée)*
- **REQ-F-04** — Le système doit permettre au responsable d'équipe de consulter les demandes de congé de son équipe et le planning des absences. *(modifiée — R5)*
- **REQ-F-05** — Le système doit permettre au responsable d'équipe d'accepter ou de refuser les demandes en attente. Un motif doit être indiqué en cas de refus. *(modifiée — R5)*
- **REQ-F-06** — Le système doit informer l'employé du résultat de sa demande dès qu'une décision est enregistrée ou générée automatiquement. *(modifiée — R10)*
- **REQ-F-07** — Le système doit permettre au service RH de saisir le solde initial, d'ajouter des jours de récupération et de consulter l'historique des mouvements. *(modifiée — R5)*
- **REQ-F-08** — Le système doit permettre au service RH de consulter la liste des absences des employés. *(inchangée)*
- **REQ-F-09** — Le système doit réserver les jours de congé annuel pour les demandes acceptées ou en attente et les libérer lorsque la demande est refusée ou annulée. *(modifiée — R1)*
- **REQ-F-10** — Le système doit vérifier le nombre d'employés absents dans une équipe et refuser automatiquement toute demande de congé annuel qui dépasse la limite autorisée. *(modifiée — R3, R9)*
- **REQ-F-11** — Le système doit refuser automatiquement toute demande de congé annuel soumise moins de 7 jours avant le début du congé. *(modifiée — R4)*
- **REQ-F-12** — Le système doit permettre à un employé de demander un congé exceptionnel pour mariage, naissance ou décès, avec une durée maximale de 3 jours ouvrables. *(modifiée — R7)*
- **REQ-F-13** — Le système doit permettre à un employé d'annuler une demande en attente ou acceptée jusqu'au début du congé. La modification directe d'une demande n'est pas autorisée. *(modifiée — R2)*
- **REQ-F-14** — Le système doit bloquer pendant 30 jours les nouvelles demandes de congé annuel lorsqu'un employé annule un congé annuel accepté moins de 7 jours avant son début. *(nouvelle — R8)*
- **REQ-F-15** — Le système doit permettre à la directrice RH de lever le blocage de 30 jours. *(nouvelle — R9)*
- **REQ-F-16** — Le système doit permettre à la directrice RH de saisir une demande exceptionnelle si le nombre d'absents ne dépasse pas 3 dans l'équipe et si le solde de l'employé est suffisant. *(nouvelle — R9)*
- **REQ-F-17** — Le système doit accepter automatiquement les demandes de congé annuel de 2 jours ouvrables ou moins si toutes les règles sont respectées. Les demandes de plus de 2 jours restent en attente de décision du responsable. *(nouvelle — R10)*
- **REQ-F-18** — Le système doit permettre d'importer depuis un fichier RH les employés, leurs contrats, leurs équipes et leurs soldes initiaux. *(nouvelle — R11)*
- **REQ-F-19** — Le système doit permettre au service RH de gérer la liste des jours fériés. *(nouvelle — R4)*

## Règles métier

- **RM-01** — Chaque employé bénéficie de 26 jours ouvrables de congé annuel par année civile. *(nouvelle — R4)*
- **RM-02** — Les jours ouvrables sont du lundi au vendredi, à l'exception des jours fériés figurant dans la liste gérée par le service RH. *(nouvelle — R4)*
- **RM-03** — Le solde disponible correspond au solde initial diminué des jours des demandes de congé annuel acceptées ou en attente. Les demandes refusées ou annulées libèrent les jours réservés. *(modifiée — R1)*
- **RM-04** — Une demande de congé annuel doit être soumise au moins 7 jours avant le début du congé. Le début du congé correspond à son premier jour ouvrable. *(nouvelle — R4)*
- **RM-05** — Une demande de congé annuel est automatiquement refusée si le solde disponible est insuffisant. *(nouvelle — R4)*
- **RM-06** — Au maximum 2 employés d'une même équipe peuvent être absents le même jour. Les demandes en attente et acceptées sont prises en compte. Si une demande dépasse cette limite, elle est entièrement refusée. *(nouvelle — R3)*
- **RM-07** — Le congé exceptionnel pour mariage, naissance ou décès est limité à 3 jours ouvrables. Il est accepté immédiatement, sans délai de préavis de 7 jours et sans application de la limite d'absents. L'employé compte toutefois parmi les absents de son équipe. *(nouvelle — R7)*
- **RM-08** — Un employé peut annuler une demande en attente ou acceptée jusqu'au début du congé. Il ne peut pas modifier directement une demande. *(nouvelle — R2)*
- **RM-09** — L'annulation d'un congé annuel accepté moins de 7 jours avant son début entraîne un blocage de 30 jours pour les nouvelles demandes de congé annuel. Exemple : une annulation le 4 mars permet une nouvelle demande à partir du 3 avril. *(nouvelle — R8)*
- **RM-10** — Seule la directrice RH peut autoriser une exception portant la limite d'absents à 3 employés maximum dans une équipe. Le nombre ne peut jamais dépasser 3 et le solde doit être suffisant. *(nouvelle — R9)*
- **RM-11** — Les demandes de congé annuel de 2 jours ouvrables ou moins sont acceptées automatiquement si elles respectent toutes les règles. Les demandes de plus de 2 jours restent en attente de décision du responsable. *(nouvelle — R10)*
- **RM-12** — Le système concerne uniquement les employés ayant un contrat CDI ou CDD. *(nouvelle — R12)*

## Exigences non fonctionnelles

- **REQ-NF-01** — L'accès aux données de congés doit nécessiter une authentification. *(inchangée)*
- **REQ-NF-02** — Le système doit respecter les droits d'accès selon le rôle : employé, responsable d'équipe et service RH. Seule la directrice RH peut autoriser les exceptions prévues et lever le blocage de 30 jours. *(modifiée — R9)*

## Hors périmètre v1

- Gestion des congés maladie — R6.
- Gestion des demandes de congés des stagiaires — R12.
- Gestion des demandes de congés des travailleurs temporaires — R12.

## Questions ouvertes

- Les jours de congé non utilisés peuvent-ils être reportés à l'année suivante ?
- Un justificatif est-il nécessaire pour les congés exceptionnels ?
- Qui valide la demande de congé du responsable d'équipe ?
- Quelles notifications doivent être envoyées aux employés et aux responsables ?
- Quelle méthode d'authentification doit être utilisée ?
- Quels sont précisément les rôles respectifs de la gestionnaire RH et de la directrice RH, en dehors des pouvoirs exceptionnels indiqués ?