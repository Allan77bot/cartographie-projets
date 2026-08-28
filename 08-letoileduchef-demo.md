# PROJECT_SNAPSHOT — letoileduchef-demo

## But
**Démo de prospection / rodage de process, explicitement non-commerciale.** Le `CLAUDE.md` du projet le déclare noir sur blanc : « projet test réel-fictif pour rodage du process Synkroniseia » (le nom de l'activité d'agence d'Allan dans ce dossier). Le restaurant "La Toile du Chef" à Meaux est réel, mais **Synkroniseia n'est pas (et n'était pas) son prestataire** — aucun contrat, aucun client réel derrière. But réel : servir de test grandeur nature du "process" de production de site (template `process.md`, phases 0 à 7) pour se roder avant de vendre à de vrais clients, et potentiellement démarcher ce restaurant avec une démo concrète.

## Contenu/Stack
- Next.js 16 App Router + Tailwind v4 + Motion 12 + GSAP 3.13 (ScrollTrigger) + Paper Shaders, one-page scroll storytelling (13 sections), Phase 7 mini-CMS prévue (non confirmée livrée).
- Volumineuse documentation méthodologique : `CLAUDE.md` (32 Ko, règles + garde-fous du projet), `STRATEGY.md` (42 Ko, copy verrouillé + positioning), `BRAND-BRIEF.md`, `process.md` (79 Ko, méthode générique agence), `design-tokens.json`, `ANNEXE-COMMERCIAL.md` (grille tarifaire type : Pack Express 700€, Pack Pro 700€+49€/mois, Pack Pro+ 1200€+89€/mois — **générique/gabarit, pas une facture réelle**), `ANNEXE-PASSATION.md` (procédure de remise client type), `CHANGELOG.md`, `historique.md`.
- Toutes les données légales sont fictives et marquées comme telles (SIRET `12345678901234` invalide exprès, raison sociale "(DÉMO)").
- Garde-fous obligatoires imposés par le projet lui-même : bandeau `<DemoBanner />`, `noindex,nofollow`, `robots.txt Disallow: /` — sécurité anti-indexation Google, car ce n'est pas un vrai site officiel.

## État actuel
D'après `CLAUDE.md` (§11) : Phase 0 (brief stratégique) terminée le 23/05/2026, direction artistique retravaillée 3 fois (v1 « Tellurique Doré » puis v2 « Bordeaux gastro » puis v3 « Black/Orange/Gold » adoptée en dernière session, 26/05/2026). Le `CHANGELOG.md` montre du développement jusqu'à la version [0.6.0] du 26/05/2026 (Phase 4 sections commerciales + refonte DA v3 avec 12 composants). Dernière modification de fichiers : 26 mai 2026 — **aucune activité depuis 3 mois**.

## Ce qui est complet/incomplet
**Complet :**
- Cadrage stratégique et copy entièrement verrouillés.
- Développement front avancé : Hero, sections narratives (Chef, Carte, Formule), signature animation storytelling "L'ancrage Meaux" (GSAP pin 3 panneaux), sections commerciales (Privatisation, Avis, FAQ, Contact, CTA final, Footer, WhatsApp Float).

**Incomplet :**
- Assets visuels (12 photos IA + vidéo Hero Kling) : listés comme "à générer", statut de génération réelle non confirmé dans les fichiers lus.
- Phase 5 (connectivité & sécurité), Phase 6 (polish & déploiement), Phase 7 (mini-CMS) : cochées "à faire" dans le plan, pas de preuve qu'elles aient été terminées.
- Checklist finale de mise en production (Lighthouse, cross-browser, RGPD, Schema.org) non cochée.
- Domaine `latoileduchef-demo.fr` : décision d'achat non tranchée (peut être resté en localhost).
- Aucune trace de démarchage réel du vrai restaurant avec cette démo.

## Prochaines étapes probables
Aucune reprise probable en l'état — projet dormant depuis 3 mois. Si relance : soit terminer le rodage (Phases 5-7 + checklist), soit l'utiliser tel quel comme pitch de démarchage auprès du vrai restaurant "La Toile du Chef".

## Questions ouvertes
- Ce projet a-t-il servi son but (rodage du process) et peut-il être archivé/supprimé sans risque, la méthode ayant peut-être été réutilisée ailleurs (ex. `Sauveur2vie` utilise une structure de dépôt différente donc pas de lien direct visible) ?
- Le vrai restaurant a-t-il été contacté avec cette démo, ou le projet est-il resté un exercice interne ?
- Le domaine `latoileduchef-demo.fr` a-t-il été acheté (coût récurrent à vérifier) ?
