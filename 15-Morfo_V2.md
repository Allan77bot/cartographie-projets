# PROJECT_SNAPSHOT — Morfo V2/V3

Généré par audit automatique le 2026-08-28. Basé uniquement sur l'observation des fichiers présents.

## But

MORFO est une application web utilisée **en boutique sur iPad** par des vendeurs AK Nutrition (franchisé BioTechUSA, CEO Adam Halin — cf. CLAUDE.md, boutiques Meaux / Noisy-le-Grand / O'Parinor). Elle calcule le profil nutritionnel du client (TMB/TDEE, formule Mifflin-St Jeor), capture son email en échange d'un lead magnet, puis lui vend un programme personnalisé (Nutrition 49€ / Sport 49€ / Pack 79€) via un code vendeur. Client final du projet : Allan agit comme prestataire (SynkroniseIA) pour AK Nutrition.

La V2 = 3 sites HTML/JS/CSS distincts (un par boutique). La V3 = refonte totale en une seule app React, en cours.

## Contenu / Stack

- **morfo-meaux / morfo-noisy / morfo-parinor** : sites V2, HTML/CSS/JS statiques (dossiers nichés en double, ex. `morfo-meaux/morfo-meaux/`), datés du 9 mars 2026. Pas de package.json — pages statiques (`index.html`, `tmb.html`, `resultat-tmb.html`, `offres.html`, `programme.html`, `confirmation.html`). Semblent être la version "en prod" historique (ou en fin de vie), remplacée par V3.
- **morfo-v3** : app React 19 + Vite 8 + Tailwind 4 + react-router-dom, PWA (vite-plugin-pwa). Contient `dist/` (build généré) et `.netlify/state.json` (siteId lié) → a été déployée sur Netlify à un moment donné. Pages présentes : BoutiqueSelection, Questionnaire, LeadMagnet, Offres, ConfirmationAchat, VideoIntro, + un dossier `recettes`. Structure conforme au plan dans `docs/superpowers/plans/2026-03-30-morfo-v3-refonte.md`.
- **morfo-recettes-preview** : app React+Vite+Tailwind+TS séparée (avec Radix UI), a un `dist/` → build/preview de l'app "MORFO Recettes" (voir RECETTE.md).
- **morpho-recipes** : autre implémentation de l'app recettes, stack différente (Express + tsx + Drizzle ORM côté serveur, `client/`+`server/`+`shared/`), semble être un prototype/alternative technique à `morfo-recettes-preview` (nom quasi-identique, à confirmer lequel est le "bon").
- **RECETTE.md** : doc décrivant l'architecture de découpage des macros journalières en macros par repas pour l'app recettes (réservée aux clients ayant acheté le Pack), avec sync N8N → Airtable (base `appcG4EJIV3FhtzSN`).
- **Template PDF Diet / Template PDF Entrainement** : fragments HTML/CSS (`html.txt`/`css.txt`) pour templates PDFMonkey — à confirmer s'ils sont branchés en prod (le CLAUDE.md dit "PDF en attente de décision", section 14).
- **Recap/** : nœuds de code N8N (JS) + exports de workflows pour rapports quotidiens/mensuels par boutique (Airtable), en plusieurs versions (V2, V3, "V3 PROD") — indique un système de reporting qui a tourné en production à un moment (versions "PROD" distinctes des versions de dev).
- **docs/** : specs/plans Superpowers (brainstorming Claude Code), prompts IA nutrition/sport, template de facture PDFMonkey + workflow N8N facturation.
- **design/** : exports de maquettes (dossiers nommés d'après des écrans : calculateur_tmb, confirmation, questionnaire, résultats, offres) — probablement générés par un outil de design IA.
- **Logo/**, **Email HTML/**, **Video/**, **Pdf morfo/** : assets (logos, templates d'emails HTML texte, une vidéo 28 Mo, deux PDF d'exemple "plan alimentaire" / "programme sport Allan" — semblent être des PDF de test/démo générés pour Allan lui-même, pas un vrai client).
- **Fichiers JSON racine** (`Morfo Programme.json` ~250 Ko, `TMB Morfo Oparinor.json`, `TMB Noisy.json`, `Morfo TMB meaux.json`, `Formulaire client.json`) : exports de workflows N8N V2, datés du 29 mars 2026 — logique métier de référence pour la V3 (cf. CLAUDE.md section 0).
- **.claude/ + .superpowers/** : projet géré avec Claude Code + méthode Superpowers (brainstorming, specs, plans traçés dans docs/superpowers/).
- **Git** : dépôt local avec seulement 2 commits (1 juin puis 5 juin 2026) — "Initial commit" massif puis un ajout de templates. Pas d'historique incrémental malgré l'ampleur du projet (le vrai suivi de travail a dû se faire hors git, ou le repo a été réinitialisé/importé tardivement).

## État actuel

- Dossier racine touché le 23 août 2026 (accès/copie récente), mais le **contenu réel** (code, JSON) date majoritairement de mars-mai 2026 ; rien ne prouve un travail de code après mi-mai 2026 (dernier fichier modifié dans Recap = 14 mai, morfo-v3/src/index.css = 12 avril).
- morfo-v3 a un `dist/` et un site Netlify lié → **a été déployé au moins une fois**, mais impossible de confirmer si le déploiement est toujours live/à jour (à confirmer : vérifier l'URL `morfo-v3.netlify.app`).
- Le CLAUDE.md V3 est très détaillé et daté du 30 mars 2026 — brief de refonte complet, avec workflows N8N à créer listés mais **statut de création non vérifiable depuis les fichiers locaux** (le MCP N8N n'est pas accessible depuis cet audit).
- Deux implémentations concurrentes de l'app recettes (`morfo-recettes-preview` et `morpho-recipes`) suggèrent une hésitation technique non tranchée, ou un abandon d'une des deux pistes.

## Ce qui est complet / incomplet

**Complet (probable) :**
- V2 (3 sites boutique) : pages HTML full (index, tmb, résultats, offres, programme, confirmation) — semble fonctionnel/fini pour son époque.
- Formules TMB/TDEE et grille tarifaire figées dans CLAUDE.md.
- Templates PDF (Diet, Entraînement, facture) rédigés.
- Système de reporting N8N (Recap jour/mensuel par boutique) avec versions "PROD".

**Incomplet / en suspens :**
- Génération des PDF programmes : explicitement marquée "en attente" dans CLAUDE.md section 14 ("Ne pas implémenter pour l'instant").
- App V3 : squelette React présent (pages, hooks, lib) mais profondeur/finition du code non auditée en détail ici (à confirmer : lire le contenu de `src/pages/*.jsx` pour juger la complétude fonctionnelle).
- App Recettes : deux stacks concurrentes non tranchées.
- Workflows N8N V3 listés dans CLAUDE.md (6 workflows) : existence réelle sur l'instance N8N non vérifiable localement.

## Prochaines étapes probables

- Trancher entre `morfo-recettes-preview` et `morpho-recipes` (garder une seule implémentation).
- Vérifier l'état réel du déploiement Netlify de morfo-v3 (live ou pas).
- Décider enfin la stratégie PDF (point resté "en attente" depuis le brief initial).
- Nettoyer les doublons/déchets (`Nouveau dossier` vide, dossiers nichés en double comme `morfo-meaux/morfo-meaux`).

## Questions ouvertes

- Le projet est-il toujours un client actif (AK Nutrition / Adam Halin) ou une piste arrêtée ? À confirmer avec Allan.
- Y a-t-il eu des ventes réelles (49€/79€) via ce système ? **Aucune preuve trouvée dans les fichiers locaux** (pas de facture émise, pas de montant réel dans les JSON de Recap — uniquement des templates et du code générique). Réponse : **non trouvé**.
- Le site Netlify `morfo-v3.netlify.app` est-il toujours en ligne ?
- Les workflows N8N V3 ont-ils été effectivement créés sur l'instance Hostinger ?
- Pourquoi seulement 2 commits git pour un projet aussi volumineux (perte d'historique, ou import tardif dans git) ?
