# PROJECT_SNAPSHOT.md — SAAS/scribeappdossier

*Généré par audit de cartographie globale, 2026-08-28.*

## But

Un **checkout ancien du même repo Scribe** (même produit que `scribe-app` : notes vocales/écrites →
coordination d'équipe, tâches, accusés de lecture, passation) figé au 2026-06-14, sur lequel s'est en
plus greffé le travail de bootstrap de l'agent **Hermes** (orchestrateur VPS Hostinger, NousResearch,
branché sur DeepSeek) : mémoire longue (Mem0), manifeste "soul", kit de credentials, skills forgés
(`skillYTB.md`, `skillnotebook.md`, `skillapprentissage.md`, `skillorganisation.md`), scripts Python
(`apprendre.py`), audit VPS (`audit-hermes-vps.sh`).

## Contenu / Stack

- **Côté produit Scribe** : même structure Next.js (`src/app`, `src/lib`, `supabase/migrations`,
  `tests/`, `docs/`), mais **version antérieure** : `package.json` sans Stripe, sans SDK Anthropic/OpenAI
  (dépendances = Next 16, React 19, Supabase seulement) → correspond à l'état du repo avant la Phase 5
  Billing (13/06) et avant l'intégration IA complète.
- **Côté Hermes/agent** (spécifique à ce dossier, absent de `scribe-app`) : `__mem0_v2/` et
  `usersallanprojectsscribeappdossier__mem0_dl/` (paquets Python mem0ai vendorés), `manifeste-soul-hermes.md`,
  `kit-credentials-hermes.md`, `kit-transmission-hermes.md`, `memoire-agent-hermes.html`,
  `tests/projethermes.md` (briefing portable Atelier Klar), `.firecrawl/` (cache de recherches web
  volumineux, non lié au produit).
- Git local avec historique propre (`git log` visible), dernier commit :
  "docs(hermes): acte la decision acces Google (OAuth complet garde) + trace session".

## État actuel

Figé depuis le 2026-06-14 (dernière modif). Reflète l'état du projet Scribe juste après le socle
auth/RLS (`main` a fusionné `feat/integration-hermes`), avant toute la suite (billing, design clair,
tâches, passation, landing). En parallèle, sert de journal de mise en place d'Hermes comme agent VPS
autonome (accès Google OAuth, Mem0, dreaming loop, skills).

## Ce qui est complet / incomplet

**Complet (à cette date du 14/06)** : socle Next.js + auth Supabase + RLS par org, CI GitHub Actions,
Hermes opérationnel sur un sandbox Supabase dédié (4/4 tests d'isolation), documentation de transmission
Hermes (credentials, manifeste, skills).

**Incomplet** : tout ce qui a été construit après le 14/06 dans `scribe-app` (capture, tâches, rapport,
billing, invitations, design clair, landing) est **absent ici** — ce dossier n'a jamais suivi cette suite.

## Prochaines étapes probables

Aucune — ce dossier semble être un point figé dans le temps, pas une ligne de développement active.
S'il s'agit du répertoire de travail local d'Hermes sur le VPS (ou une copie synchronisée depuis celui-ci),
la suite logique serait de le resynchroniser avec `scribe-app` ou de l'archiver.

## Questions ouvertes

- Ce dossier est-il un clone local fait à la main le 14/06, une sauvegarde automatique, ou le mirror
  du répertoire de travail réel d'Hermes sur le VPS Hostinger ? À clarifier avec Allan.
- Les fichiers Hermes (manifeste, kit credentials, Mem0) ont-ils une valeur propre à conserver
  indépendamment du code Scribe (ex. reproductibles pour un futur agent) ? Si oui, les extraire avant
  suppression du dossier.
- `.firecrawl/` contient un gros cache de recherches web (mem0, API docs) — purge sans risque si
  le dossier est jugé obsolète.

## Revenus

Non trouvé. Stripe n'apparaît que comme décision à venir dans la documentation (`docs/brief-produit.md`,
`docs/stack-technique.md`) — aucune mention de facturation active, de client payant ou de mode LIVE.

## Doublon avec scribe-app ?

**Oui, clairement.** Il s'agit d'une **version antérieure et partielle** du même repo Scribe
(commit du 14/06 contre fin juin pour `scribe-app`, `package.json` sans Stripe/IA, `snapshot.md` de
7,6 Ko contre 44 Ko). Le contenu produit ici est un sous-ensemble strict et obsolète de `scribe-app`.
Seule la partie **Hermes/agent VPS** (Mem0, manifeste, kit credentials, skills) n'a pas d'équivalent
dans `scribe-app` et mériterait vérification avant suppression — le reste (code Next.js, docs produit)
peut être supprimé sans perte, `scribe-app` faisant foi.
