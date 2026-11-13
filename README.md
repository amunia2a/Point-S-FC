# Point S Fidélité V6.44 — Correctif PC commerçant

Base : V6.43. Aucun changement intentionnel au parcours mobile, au MFA, à Supabase ou aux permissions commerçants.

- L’icône crayon de l’avatar PC est remplacée par un pictogramme appareil-photo dans un cercle bleu correctement positionné.
- Le clic sur l’avatar ou « Modifier la photo » dans les paramètres ouvre un sélecteur de fichier dédié. Le précédent sélecteur était vidé par un gestionnaire avant le rafraîchissement du nouveau header.
- Formats acceptés : PNG, JPEG, WebP (3 Mo maximum). L’aperçu se synchronise dans le header et les paramètres pendant la session. **Aucune sauvegarde Supabase n’est encore active.**
- Uniformisation de la police par héritage de la police de la page et titres des quatre cartes en bleu #073B94.

## Tests à faire
1. Sur PC, cliquer sur l’avatar puis choisir une photo. Vérifier qu’elle apparaît dans le header et dans les paramètres.
2. Depuis les paramètres, choisir une autre photo. Vérifier la synchronisation de l’aperçu.
3. Vérifier les titres Fidélité, Actus, Clients et Avis Google, ainsi que la police du header.
4. Vérifier la version mobile, les garages autorisés, la navigation et les flux MFA avant déploiement.
