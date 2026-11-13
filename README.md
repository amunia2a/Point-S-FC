# Point S Fidélité — V6.41 (préparation Supabase)

Base : V6.40. Aucun déploiement.

## Modifications PC commerçant (≥ 960 px)
- Header agrandi et épuré, notifications et icône carte masquées sur PC uniquement.
- Avatar cliquable (clavier inclus) : sélection PNG/JPEG/WebP, maximum 3 Mo, aperçu rond.
- Même aperçu et bouton « Modifier la photo » dans Paramètres.
- Icônes officielles garage et Point S fournies intégrées en base64, sans fichiers externes.
- Sélecteur de garage existant conservé. Aucun moteur de recherche ajouté.

## À configurer dans Supabase (non activé)
- Stockage privé des avatars dans Storage, contrôles d'accès par identifiant Auth.
- Profil commerçant avec nom affiché et référence d'avatar.
- Préférence garage persistée uniquement parmi les garages autorisés.
- Lecture/écriture sécurisée et synchronisation multi-appareils après validation du schéma et des RLS.

**Important :** la photo n'est qu'un aperçu temporaire et n'est PAS enregistrée dans Supabase. Le nom continue d'être enregistré localement par le code V6.35 existant. Ne pas considérer la persistance comme opérationnelle.

## Contrôles à effectuer
1. Sur PC, vérifier taille du header, absence de notification, garage et prénom.
2. Cliquer sur l'avatar, sélectionner une image, ouvrir Paramètres et vérifier le même aperçu.
3. Vérifier les PNG officiels et le bouton photo dans Paramètres.
4. Recharger : l'aperçu disparaît (comportement temporaire attendu).
5. Vérifier que la version mobile, les accès commerçants, RLS, MFA et les pages existantes sont inchangés.
