# PROJECT_SNAPSHOT — Atelier Acidulé

## But
Site vitrine premium pour **Atelier Acidulé**, une créatrice de sacs et accessoires au crochet faits main, sur commande, dans la couleur choisie par la cliente (univers Italie/Méditerranée, "citron acidulé"). Commerce hybride : le site sert de vitrine et de catalogue, la commande et le SAV passent par DM Instagram (`@atelier_acidule`), le paiement en ligne étant prévu "plus tard" mais non implémenté.

## Contenu / Stack
Site **Astro 5** scaffoldé à la main, déployé sur Netlify (`atelier-acidule.netlify.app`), dépôt Git sur GitHub (`Allan77bot/atelier-acidule`), branche de travail `feat/refonte-accueil`. Pages : accueil (landing classique), `/mes-creations` (expérience scroll plein écran en CSS scroll-snap, une couleur/section par modèle de sac), `/editions-speciales`, `/atelier` (histoire + contact), `/commander` (formulaire placeholder, non branché à un paiement). Catalogue de 4 modèles définis dans `src/data/modeles.ts` (petit sac, pochette à livres, grand sac de plage, éditions spéciales) à 35/40/45 €. Documentation projet mature : `CLAUDE.md`, `CONTEXTE-PROJET.md`, `HISTORIQUE.md`, `docs/ETAT.md`/`JOURNAL.md`. Dossiers `Ref/PhotoClient`, `Ref/VideoClient`, `Ref/catalogue` (27 photos non triées) contiennent les assets bruts fournis par la cliente.

## État actuel
**Refonte terminée et déployée**, dernière modification 27 juin 2026. Le site est en ligne, le code est commité et poussé sur GitHub, la documentation est à jour. La feature de personnalisation (configurateur de recoloration du sac) a été **abandonnée** lors de la refonte du 27/06 — jugée trop complexe pour la valeur apportée, remplacée par un lien direct vers Instagram pour commander.

## Ce qui est complet / incomplet
**Complet** : landing page, page scroll `/mes-creations`, design system (palette, typographies), build de production propre (0 erreur, responsive vérifié), retrait des dépendances inutiles (GSAP, Lenis désinstallés).
**Incomplet** : auto-déploiement Netlify↔GitHub non branché (déploiement manuel via CLI uniquement) ; formulaire `/commander` reste un placeholder ; paiement en ligne non implémenté ; 27 photos du dossier `Ref/catalogue/` non exploitées ; validation visuelle finale de la cliente et de l'associé pas confirmée dans les fichiers ; merge de la branche `feat/refonte-accueil` vers `main` pas encore fait.

## Prochaines étapes probables
- Recueillir la validation visuelle de la cliente sur le site en ligne.
- Brancher l'auto-déploiement Netlify↔GitHub.
- Exploiter les 27 photos non triées pour enrichir le catalogue/les galeries.
- Merger la branche de refonte vers `main`.
- Plus tard : brancher un vrai système de commande/paiement en ligne.

## Questions ouvertes
- **Revenus : non trouvé.** Aucune facture, devis ou mention de paiement d'Allan par la cliente dans les fichiers du projet. Les seuls montants en euros présents (35 €, 40 €, 45 €) sont les prix de vente des sacs de la cliente, pas la rémunération d'Allan pour le site. Nature de l'accord (payant, échange de service, portfolio gratuit) à clarifier.
- Le site est-il toujours d'actualité côté client (pas de trace d'activité après le 27 juin, soit 2 mois avant la date d'audit) ?
- La cliente a-t-elle donné suite pour la validation finale et le passage en ligne définitif (merge vers `main`) ?
