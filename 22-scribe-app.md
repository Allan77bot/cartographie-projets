# PROJECT_SNAPSHOT.md — scribe-app

*Généré par audit de cartographie globale, 2026-08-28. Ne remplace pas `snapshot.md` (état de travail détaillé) — vue de synthèse pour décision garder/couper.*

## But

SAAS Scribe : transformer des notes vocales/écrites (équipes en relais 3×8, cible logistique/entrepôt)
en **coordination active** — suivi de tâches, accusés de lecture, rapport de passation automatique.
Explicitement PAS un outil de transcription passive. ICP = "Route B" tranchée le 2026-06-19 (équipes
en relais 3×8, vertical logistique par défaut, non gelé).

## Contenu / Stack

Repo Next.js 16 complet (App Router) + React 19 + TypeScript + Tailwind v4. Supabase (Postgres/Auth/RLS
multi-org, storage URL signées, EU Frankfurt). IA : transcription OpenAI (Whisper), extraction Claude
Haiku 4.5, synthèse Claude Sonnet 4.6 (route API Anthropic directe + DPA EU). Stripe pour billing
(mode TEST). Playwright pour les tests e2e. Structure `src/app` (routes + dashboard), `src/lib`
(actions serveur), `supabase/migrations` (13 migrations), `legacy/` (archive figée d'un prototype
Atelier Klar antérieur — n'est plus le code actif). Docs riches : `CLAUDE.md` (routeur), `DESIGN.md`
(design system "Corporate Modern" thème clair, Manrope), `docs/brief-produit.md` (spec canonique),
`docs/etude-strategique.md`, `docs/audit-global.md`, `docs/plan-attaque.md`, `HERMES.md` (règles pour
l'agent VPS Hermes qui contribue par PR sur ce même repo).

## État actuel

Dernier commit 2026-06-28 ("docs: cap la reprise sur Claude Design"). Fonctionnalités posées : auth
Supabase + RLS isolée par org (4/4 tests d'isolation), capture (audio/texte), tâches avec validation
humaine obligatoire, rapport de passation 3×8, invitations d'équipe par jeton signé, billing Stripe
(webhook + checkout, TEST uniquement), onboarding wizard, migration complète vers un design clair
("Professional Flow"). Landing page de vente construite fin juin (hero, sections, animations sobres).
**Bloqué en prod** au dernier snapshot : migration `0013` (réconciliation drift) non exécutée en base
réelle par Allan — tant que ce n'est pas fait, validation de tâche et passation plantent en prod.

## Ce qui est complet

- Auth + RLS multi-org, isolation prouvée.
- Pipeline capture → extraction → tâches → rapport (async).
- Facturation Stripe (structure) en mode TEST.
- Invitations d'équipe, page Équipe, onboarding.
- Design system clair appliqué à 28 fichiers UI, zéro trace de l'ancien thème sombre.
- Landing page de vente avec animations.
- CI GitHub Actions (lint + build + migrations + check:rls).

## Ce qui est incomplet

- Migration `0013` jamais appliquée en base de prod réelle (blocage connu).
- `feat/onboarding` et `feat/tasks-assignment` : maquettes `/demo` validées mais **jamais portées**
  dans les vraies pages.
- Stripe jamais passé en mode LIVE ; pas de vente ni de client identifié dans les fichiers consultés.
- Conformité (DPA, page `/conformité`, suppression d'org) non commencée.
- Confirmation e-mail à l'inscription absente.
- Reset périodique du quota minutes non branché.
- Gabarit e-mail encore aux couleurs Atelier Klar (pas Scribe).
- Sort des maquettes `/demo` (garder en dev ou retirer) non tranché.
- Pricing final non figé (dépend de preuve d'activation sur 10-20 clients).

## Prochaines étapes probables

1. Débloquer la prod (exécuter la migration 0013 avec snapshot DB avant).
2. Nettoyer/committer proprement la branche `fix/stabilite-prod`.
3. Porter les maquettes `/demo` dans `feat/onboarding` et `feat/tasks-assignment`.
4. Trancher l'archi tâches (JSONB vs table dédiée `public.tasks`).
5. Discovery terrain (5-10 entretiens) pour confirmer le vertical logistique et le canal de
   notification du shift entrant, avant de coder le Sprint 2.
6. Avant toute vente : socle conformité minimal + Stripe live + confirmation e-mail.

## Questions ouvertes

- Le projet est-il toujours actif ? Dernière activité fin juin 2026, ~2 mois d'inactivité au
  28/08/2026 — à confirmer avec Allan si c'est un pivot de priorité ou un abandon de fait.
- Y a-t-il eu des entretiens de discovery terrain depuis fin juin ? Rien dans le repo ne l'indique.
- Le sandbox Supabase Hermes (`doorjfxqetoawqnvguvz`) répondait déjà en ENOTFOUND au dernier snapshot —
  état actuel inconnu.
- Décision GitHub Pro (protection de `main`) : prise ou toujours en attente ?

## Doublon avec SAAS/scribeappdossier ?

**Oui, partiellement.** `SAAS/scribeappdossier` est un **checkout antérieur du même repo** (dernier
commit 2026-06-14, avant l'ajout de Stripe/billing, avant Sonnet/Haiku dans les dépendances, snapshot.md
7,6 Ko contre 44 Ko ici). Il a en plus accumulé des artefacts propres à l'agent VPS Hermes (Mem0, kit de
credentials, manifeste "soul", skills forgés) qui ne vivent pas dans ce repo. `scribe-app` (ce dossier)
est la version **la plus à jour et la référence active** — `scribeappdossier` peut être archivé/supprimé
sans perte de code produit, sous réserve de vérifier qu'aucun doc Hermes unique n'y manque ailleurs.
