# PROJECT_SNAPSHOT — Double-AS

*Généré le 2026-08-28 par audit de cartographie. Basé uniquement sur lecture des fichiers listés ; toute incertitude est marquée "à confirmer".*

## But

Double-AS est un **AIOS (Agentic Operating System)** — infrastructure de pilotage agentique (Atlas) pour deux personnes, Allan (owner) et Alphim, qui opèrent deux activités logées dans ce même dépôt :

- **Atelier KLAR** — création/design web (dossier `03_ATELIER_KLAR`, état "à confirmer" au-delà d'`ETAT-REEL.md`).
- **Synkronise IA** (renommé "Synkroniseia" dans l'usage courant) — agence d'automatisation IA pour PME, actuellement en **sprint commercial actif** "Relais Vocal IA" (15/08 → 13/10/2026).

Le dépôt a démarré comme une **mission d'audit documentaire** ("jumeau documentaire" de 29 015 fichiers sources, dossiers `00_CONTROL` à `14_TESTS`) — cette mission est explicitement **archivée/figée** depuis le montage de l'AIOS le 2026-07-24. Depuis, le pilotage vivant s'est déplacé vers `OS/` (5 vues : Aujourd'hui, Sprint, Pipeline, Tableau de bord, Décisions) et `docs/ETAT.md` / `docs/JOURNAL.md`.

## Contenu / Stack

- **Structure numérotée 00–14** : ancienne mission d'audit, en lecture seule ("on y puise, on n'y écrit plus").
- **`OS/`** : pilotage quotidien du sprint commercial (vues Aujourd'hui/Sprint/Pipeline/Décisions/Backlog), lié à un Google Sheet externe de pipeline.
- **`atlas/`** : identité de l'agent central (soul.md, user.md, memory.md).
- **`02_OBSIDIAN/`** : vault Obsidian, mémoire longue structurée (projets, décisions, hypothèses, erreurs, métriques).
- **`jarvis/`** : cockpit Python (`cockpit.py` → génère `cockpit.html`, lit Airtable/Hermes).
- **`automations/`** : n8n, Hermes (VPS), éditorial (blog/LinkedIn via Airtable), prospection (OSM scraping, qualification par 4 portes, terrain porte-à-porte).
- **`scripts/`** : intégrations (Airtable, Mammouth multi-LLM router, vérification secrets/mémoire).
- **`.claude/skills/`** : skills internes (os-audit, auto-correction, cyber-attaque, travailler-à-deux).
- **`kit-agentic/`** : templates et contrats de méthode agentique portables.
- **`07_AGENTIC_OS_FUTURE/`** : contrats/spécifications non implémentées pour un futur OS (explicitement marqué comme non réel).
- **Stack technique** : Python (scripts, cockpit), N8N (VPS Hostinger, déploiement en lecture seule miroir GitHub), Airtable (base "Double AS OS", tables Ops/Articles/Prospects), Mammouth (routeur multi-LLM : sonar-pro, kimi-k2.5, gemini, claude-sonnet-5), Git (repo privé `github.com/Allan77bot/Double-AS`, remote actif).
- **Deux postes** : Allan sous Windows 11, Alphim sous WSL2 Ubuntu — le CLAUDE.md documente des pièges spécifiques à chaque environnement.

## État actuel

**Très actif** : dernier commit le 2026-08-27, dépôt git avec 12+ branches de feature en cours, historique dense (prospection terrain, cadrage devis, cockpit, blog éditorial). Le sprint commercial Synkroniseia est daté au jour près (vue "Aujourd'hui" du 21-22/08/2026, J7/60).

**Client pilote en cours — Tony** (organigramme "Tony's Inn", holding avec 28 sociétés filles, ~12 hôtels, ~10 meublés, 2 laveries) :
- A **accepté un devis** le 21/08 : lot 1 = agent vocal + page de suivi, **1 000 € à la signature + 300 €/mois**, calibrage 3 mois.
- Statut au 22/08 : **"proposition acceptée", PAS "signature"** — la règle interne de l'OS est stricte : seul l'encaissement de l'acompte vaut signature. **L'acompte de 1 000 € n'était pas encore encaissé** à la dernière mise à jour lue.
- Aucune heure de build ne devait démarrer avant l'encaissement (règle explicite).
- Un point technique bloquant non résolu : vérification du renvoi d'appel conditionnel sur la ligne téléphonique de Tony (dépendant d'un numéro français à commander).
- Objectif du sprint (2 signatures hors Tony d'ici J60/13-10) : **non atteint**, prospection à "zéro compte contacté" au 21/08 malgré 7 jours de sprint.

5 décisions de gouvernance internes (`DEC-01` à `DEC-05`, dont le partage de revenu Allan/Alphim) étaient **échues et non tranchées** à la dernière lecture.

## Ce qui est complet / incomplet

**Complet / en place :**
- Infrastructure documentaire et de gouvernance très mature (vault Obsidian, contrats, ontologie, registres, règles de vérité A-E).
- Cockpit Python fonctionnel avec intégration Airtable/Hermes.
- Pipeline de prospection scriptée (collecte OSM, qualification 4 portes, ciblage terrain) — utilisée activement (338 leads réels selon commit du 09/08, tournée terrain Meaux avec 10 fiches prospects au 27/08).
- Chaîne éditoriale blog/LinkedIn (script + tests, publication non automatique — validation humaine requise).
- Devis envoyé et accepté par un premier client (Tony).

**Incomplet / bloqué :**
- Encaissement du premier revenu (acompte Tony) — non confirmé dans les fichiers lus.
- Gouvernance minimale Double AS (`VAL-2026-001`) — décision humaine ouverte depuis fin juillet, jamais tranchée, pourtant prérequis pour facturer (nécessite une entité juridique).
- Accord de partage économique Allan/Alphim (`DEC-05`) — non tranché, alors qu'un client réel est en cours.
- Plateforme vocale technique non choisie/validée en production (`DEC-04`), démo pas encore appelable au 16/08 (échéance dépassée).
- Rotation de secrets signalée comme risque ouvert depuis le 28/07, toujours listée comme bloquée le 22/08.
- Atelier KLAR : état "à confirmer", peu documenté au-delà d'`ETAT-REEL.md`.

## Prochaines étapes probables

- Encaisser l'acompte Tony et démarrer le build du lot 1 (agent vocal).
- Trancher les décisions de gouvernance échues (`DEC-01` à `DEC-05`), notamment le partage de revenu.
- Poursuivre la prospection (objectif : 2 signatures hors Tony avant le 13/10/2026).
- Résoudre le point technique du renvoi d'appel conditionnel (numéro FR requis).

## Questions ouvertes

- L'acompte de 1 000 € de Tony a-t-il été encaissé depuis le 22/08 ? (à confirmer, hors périmètre de cet audit)
- Statut juridique de "Double AS" comme entité facturante — existe-t-il déjà ou est-ce encore hypothétique ?
- Répartition réelle des rôles/revenus entre Allan et Alphim (RACI provisoire seulement, `DEC-05` non tranchée).
- Volume d'appels réel attendu pour l'agent vocal de Tony — explicitement inconnu au moment du cadrage.
- État réel d'Atelier KLAR (peu de matière dans ce dépôt ; probablement documenté ailleurs).
- Revenus historiques : aucune facture ou montant encaissé trouvé dans les fichiers audités — seul un devis accepté (non payé) est documenté.
