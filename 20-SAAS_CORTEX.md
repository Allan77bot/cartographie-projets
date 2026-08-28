# PROJECT_SNAPSHOT — SAAS CORTEX / SellerScale

*Généré par audit de cartographie, 2026-08-28. Ne remplace pas `snapshot.md` (mémoire de session vivante) — complément pour une vue globale multi-projets.*

## But

SaaS B2B qui transforme une méthodologie manuelle éprouvée de création de business Amazon FBA Private Label (9 phases, ~1000 membres accompagnés en formation, des dizaines de boutiques livrées) en outil automatisé par IA, en abonnement mensuel, pour débutants francophones. Renommé « SellerScale » le 04/07/2026 (ex-CORTEX), domaine `sellerscale.ai`. Promesse : trouver « TON produit gagnant, pour TON budget ».

## Contenu / Stack

- **Deux mondes dans le dossier** : la racine est un cerveau de pilotage (docs, specs, vault Obsidian `SellerScaleBrain/`, mémoire de session) — pas de code, pas de git à la racine. Le code réel vit dans `30_TECH/33_DEV_MVP/cortex-iq/`, dépôt git séparé avec remote `origin` actif.
- **Stack technique (cortex-iq)** : Next.js 16 / React 19 / TypeScript / Tailwind v4, Clerk (auth), Neon Postgres (Drizzle ORM), Vercel (hébergement + cron), Stripe (paiement live), Vitest (tests), Anthropic SDK, extension Chrome (dossier `extension/`, soumise au Chrome Web Store).
- Documentation source de vérité : `00_PILOTAGE/01_CERVEAU/CERVEAU_SAAS_SELLERSCALE_v4.md`. Moteur de scoring produit figé et testé (`src/lib/scoring/`).
- Fichiers clés : `CLAUDE.md`, `snapshot.md` (54 Ko, très actif), `historique.md` (1,2 Mo — journal long), `PROCHAINE-ETAPE.md`, `POINT-28-08-SOIR.md`, `TRI-SUPPORT-28-08.md`, `30_TECH/33_DEV_MVP/cortex-iq/package.json`.

## État actuel

**Projet actif, en production, avec de vrais utilisateurs payants.** Dernière modification : 27-28/08/2026 (quasi quotidien). Dépôt git `cortex-iq` avec commits fréquents (`master` stable + branches `feat/`, `release/`, `chore/`). Pricing 3 plans 39/79/129 €/mois, Stripe en mode live. Preuves d'utilisateurs réels dans `snapshot.md`/`POINT-28-08-SOIR.md` : comptes membres identifiés par email et ID Clerk, essais 7 jours, alertes de facturation en production, un incident de quota Neon ayant coupé la prod, une extension Chrome soumise au Web Store.

## Ce qui est complet / incomplet

**Complet** :
- Auth (Clerk) + profil persisté (Neon/Drizzle).
- Moteur de scoring produit V2.1, codé et verrouillé par tests.
- Onboarding, calculateur, dashboard, waitlist, offres/pricing, emails (bienvenue, churn).
- Extension Chrome (v1.3.0/1.3.1) soumise à Google.
- Système de support et de surveillance (monitoring cron, alertes) en cours de déploiement.

**Incomplet / ouvert** :
- Barème des seuils de verdict par profil non figé.
- Mapping profil ICP → plan tarifaire non tranché.
- Tarif fondateur (39 vs 49 €) non tranché.
- `PART_BUDGET_STOCK` à valider avec Christophe (associé/collaborateur).
- Bouton « Servir ce membre maintenant » en admin, non fait.
- Support client : 21 demandes en attente au 28/08, dont 6 demandes d'argent non traitées (prélèvement contesté 350 €, remboursement 39 € demandé deux fois, 3 résiliations non traitées).
- Base de test et de production partagent la même instance Neon (risque opérationnel identifié).
- Plusieurs branches non fusionnées (`feat/test-complet`, `feat/sursis-impaye`, `feat/market-place`, `feat/demo-moq`).

## Prochaines étapes probables

- Traiter les 6 demandes d'argent en attente (urgent, réputationnel).
- Valider le passage en prod du lot « surveillance » (monitoring cron).
- Suivre la réponse Google sur l'extension Chrome.
- Trancher les décisions business en attente (palier de prix, PART_BUDGET_STOCK, tarif fondateur).
- Séparer les bases Neon test/production.

## Questions ouvertes

- Volume réel d'abonnés payants et MRR (non chiffré dans les fichiers consultés — nécessiterait un accès direct à Stripe/Clerk).
- Le projet vaut-il la peine d'investir encore dans le chantier support (actuellement manuel, alors que le principe produit n°2 exige zéro humain dans la boucle client) ?
- Statu quo sur la séparation dev/prod Neon : risque de récidive de panne.
