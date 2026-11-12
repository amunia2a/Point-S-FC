# Point S Fidélité V6.31 — À tester

Base : V6.30.

## Modifications ciblées (commerçant PC uniquement, ≥ 960 px)
- Masquage du bouton dédié ouvrir/fermer.
- Clic dans la barre latérale : alterne entre menu compact et menu déployé. Les boutons de rubrique conservent leur navigation existante et provoquent aussi le changement d’état.
- Icônes et textes du menu en bleu `#073B94`, y compris l’élément actif.
- Logos S fermé et Point S ouvert conservés.

## Préservé
- Interface mobile, fonctionnalités, Supabase, MFA, RLS, accès, données, cartes, moteur de recherche et contenu des vues.

## Tests à réaliser
1. PC : cliquer dans la barre, sur le logo, puis sur une rubrique ; vérifier ouverture/fermeture et navigation.
2. Vérifier les six icônes en bleu `#073B94` (actives/inactives).
3. Vérifier les deux logos et la largeur du contenu dans les deux états.
4. Vérifier le mobile client et commerçant inchangé.

Contrôles : insertion localisée CSS/JS ; pas de test navigateur ni Supabase. En attente de validation.
