# PROJECT_SNAPSHOT — backup-sauveur2vie-2026-07-01

## But
Sauvegarde de sécurité prise le 1er juillet 2026, juste avant le chantier « rendre tout le site éditable dans le CMS » (= la Phase 2 documentée dans `Sauveur2vie/AGENTS.md`). Objectif unique : pouvoir tout restaurer si une modification du chantier CMS s'était révélée irréversible. Ce n'est PAS un projet actif, c'est une archive figée.

## Contenu/Stack
- `LISEZ-MOI.txt` : notice explicative.
- `site-prod-e339af9.zip` (~47 Mo) : code source de la branche `main` en production à cette date (commit `e339af9`), sans `node_modules` ni `.git`.
- `site-feature-464e3a0.zip` (~47 Mo) : code de la branche de travail `feat/dashboard-ux`/`feat/live-preview` (commit `464e3a0`) — thème dashboard + Live Preview + correctif d'auth.
- Points de restauration Git correspondants documentés : tags `backup-2026-07-01-prod` et `backup-2026-07-01-feature` (dans le dépôt `Sauveur2vie`, pas ici).
- Précise explicitement que la base Neon (contenu du dashboard) n'est PAS incluse — sauvegardée séparément.

## État actuel
Archive statique, non modifiée depuis sa création (1er juillet 2026, 21h48). Aucune action requise dessus.

## Ce qui est complet/incomplet
- Complet pour son objectif (snapshot de rollback autonome, réinstallable via `npm install`).
- Rien à compléter — ce n'est pas un livrable, juste un filet de sécurité.

## Prochaines étapes probables
Aucune, sauf besoin de restauration en cas de problème sur `Sauveur2vie`. Candidat naturel à l'archivage/suppression une fois le chantier CMS confirmé stable en prod depuis longtemps (le projet vivant `Sauveur2vie` a largement continué depuis : Phase 2 CMS livrée, LinkedIn, avis Google, retouches photo — dernières traces début-mi août 2026, plus d'un mois après ce backup).

## Questions ouvertes
- Ce backup est-il encore utile aujourd'hui (28/08/2026), sachant que les tags Git de rollback existent déjà dans le dépôt `Sauveur2vie` lui-même ? Les 2 zips (~94 Mo au total) font doublon avec ces tags.
- Peut-il être supprimé, ou déplacé vers un stockage froid (backup externe), pour libérer de l'espace local ?
