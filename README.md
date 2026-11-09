# Point S Fidélité — V6.14 (préparation test)

Base : `PointS_Fidelite_V6_13_retournement_corrige(1).html`.

## Modifications dans ce fichier
- Retrait du panneau « Derniers clients » sur l'accueil commerçant PC, sans suppression des clients ni de leurs données.
- Répartition sur six colonnes des boutons du menu commerçant sur PC (largeur >= 800 px). Menu mobile inchangé.
- L'en-tête commerçant ne montre plus un prénom fictif par défaut ; « Mon compte » est affiché tant que l'identité réelle n'est pas chargée.
- Ajout d'une fenêtre de profil commerçant consultative (PC/mobile), sans écriture Supabase ni modification des rôles.
- Détail des récompenses : suppression de l'ID artificiellement calculé à partir du nom. Affiche un code à six chiffres seulement s'il existe dans les données de la récompense ; sinon « Code client non disponible ».
- Suppression des quatre récompenses fictives de repli dans la liste des récompenses attribuées.

## Non implémenté / raccordement nécessaire
- Récupération du prénom, nom, email et photo du commerçant depuis la table réellement utilisée dans Supabase ; upload sécurisé des photos (Storage et RLS).
- Récupération du code `clients.code_client` depuis le compte client lié à chaque attribution. Les données actuelles des récompenses de la maquette ne garantissent pas ce lien.
- Routage automatique nouveau compte client / commerçant autorisé. **Non modifié** tant que la structure des autorisations Supabase et des comptes existants n'a pas été vérifiée.
- Rendez-vous au verso de la carte : projet distinct, non modifié.

## Sécurité / déploiement
- Aucun SQL exécuté, aucune autorisation Supabase modifiée, aucune migration ni déploiement.
- Les accès existants Ajaccio et Alata, MFA et RLS doivent rester strictement inchangés.
- Tester localement et sur la branche `test-recompenses` uniquement après revue.
