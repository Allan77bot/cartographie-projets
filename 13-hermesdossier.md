# PROJECT_SNAPSHOT.md — hermesdossier

## But
Dossier de travail dédié à **Hermes**, l'agent autonome (NousResearch Hermes Agent) co-gérant d'Atelier Klar, hébergé sur un VPS Hostinger (DeepSeek + Claude Code + Gemini). Sépare le périmètre "agent" du produit Scribe (`../scribeappdossier`). Contient l'identité de l'agent (soul), son architecture mémoire, ses outils, ses runbooks de mise en prod, et le build d'un dashboard agentique OS.

## Contenu/Stack
- Docs marché/config en Markdown : `CLAUDE.md` (routeur de session), `AGENTS.md`, `manifeste-soul-hermes.md` (identité), `snapshot.md`/`historique.md` (mémoire de session), `kit-transmission-hermes.md`/`kit-credentials-hermes.md` (runbooks VPS), `regles-profil-marketing.md`.
- Scripts : `apprendre.py` (skill vidéo → Mem0), `audit-hermes-vps.sh` (diagnostic lecture seule VPS).
- Gros fichiers HTML générés : `memoire-agent-hermes.html`, `scribe-graph.html` (démo Graphify, gitignored à l'usage).
- Sous-dossiers : `contexte/` (mémoire dure, gouvernance mémoire, intégration outils), `dashboard/` (build "Mission Control"), `docs/` (specs superpowers), `.firecrawl/`, `.git/`.
- Repo git local, branche `feat/integrate-agent-tools`, commits locaux non poussés.

## État actuel
Dernière activité 27 juin 2026. Très actif à cette date : mémoire autonome d'Hermes (filtre d'ingestion, wiki domaine, janitor cron) livrée et active sur 5 gateways ; deux outils agentiques greffés sur le VPS (Graphify, Agent-Reach) ; un agent email marketing (profil "marketing", bot Telegram dédié) vient d'être monté avec des skills liés (voir `hermes-skills`). Travail arrêté juste avant de lancer le pilote sur 10 leads de prospection.

## Ce qui est complet/incomplet
**Complet** : architecture mémoire (filtre + wiki + janitor), outils Graphify/Agent-Reach, profil agent marketing créé avec sa soul, skills poussés et installés sur le VPS.
**Incomplet** : le pilote de 10 leads n'a jamais été lancé ; clé `GOOGLE_PLACES_API_KEY` manquante (cron Prospection en erreur depuis le 20/06) ; décision DeepSeek vs Claude pour Hermes non tranchée ; sécurité côté Allan non traitée (OAuth Google en clair sur OneDrive, clés API en clair sur le Desktop) ; purge de 877 souvenirs mem0 en attente de validation ; commits locaux jamais poussés sur GitHub ; dashboard Phase 2 parkée.

## Prochaines étapes probables
1. Lancer le pilote 10 leads sur le bot marketing (prompt déjà prêt).
2. Fournir la clé Google Places manquante.
3. Sécuriser les credentials qui traînent en clair chez Allan.
4. Trancher DeepSeek vs Claude pour le runtime d'Hermes.
5. Décider du sort de la purge mem0 et du push GitHub des commits locaux.

## Questions ouvertes
- Ce dossier est-il toujours la source de vérité, ou le travail a-t-il continué ailleurs depuis fin juin (voir aussi `hermes-skills` qui est un repo séparé et plus récent) ?
- Le pilote de prospection a-t-il été lancé depuis (aucune trace après le 27/06 dans ce dossier) ?
- Les credentials en clair (Desktop, OneDrive) ont-ils été sécurisés depuis ?
