# financial-automation-tools

Budget Analytique — Synchronisation automatique des factures
Contexte

Ce script a été développé pour un club sportif de 1000 membres afin d'éliminer les saisies manuelles entre le fichier de suivi des factures et le budget analytique. Avant sa mise en place, les données étaient copiées-collées à la main chaque semaine dans des dizaines d'onglets différents.
Ce que fait le script
Il lit automatiquement un fichier Google Sheets externe contenant les factures, identifie le code analytique de chaque facture, et l'injecte dans le bon onglet du budget analytique à la bonne ligne et dans la bonne colonne. Un log journalier est généré à chaque exécution pour tracer toutes les opérations effectuées. Le script tourne via un déclencheur automatique quotidien à 8h, sans intervention humaine.
Fonctionnement
Le comportement du script est entièrement piloté par un onglet "Codification" dans le fichier budget. Chaque ligne de cet onglet est une règle qui indique où envoyer les données selon le code analytique de la facture. Il n'est pas nécessaire de toucher au code pour ajouter ou modifier une catégorie.
Technologies utilisées
Google Apps Script, JavaScript, Google Sheets API
Points notables

Architecture découplée : la logique métier est séparée du code via la feuille de codification
Logging automatique des opérations pour faciliter le débogage
Conçu pour être maintenu par des non-développeurs
Déclencheur automatique quotidien configurable depuis l'interface
