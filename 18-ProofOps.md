# PROJECT_SNAPSHOT — ProofOps

## But
Dossier de recherche/décision stratégique (pas de code produit) explorant une nouvelle activité potentielle : à l'origine, un service d'« assurance de résultat » pour agences d'automatisation (n8n/Make/Zapier) qui vérifie qu'un workflow a réellement produit l'effet métier attendu (pas seulement un statut "réussi"). Une thèse concurrente (AI Delivery Assurance pour code produit par agents IA) a été explorée puis classée "EXPLORER, NE PAS CONSTRUIRE". Un scorecard comparatif (doc 10) a ensuite déclassé ProofOps au profit d'une piste "Revenue Recovery Desk" (récupération de leads entrants perdus) pour PME de rénovation à panier élevé, jugée plus rapide vers 10k€/mois. Le nom "ProofOps" est un code interne — usage public déjà pris par d'autres produits, à renommer avant toute commercialisation.

## Contenu / Stack
- Pas de code applicatif : que des documents Markdown numérotés (01 à 11) formant un raisonnement séquentiel (décision → marché → offre → PRD → architecture → sécurité → roadmap → sources → thèse alternative → scorecard → kit de validation).
- `README.md` : point d'entrée, statut global et table de navigation.
- `kitagentvocal/` : sous-dossier autonome (README + 6 fichiers numérotés + LANDING-BRIEF-MAITRE.md) documentant la piste "Revenue Recovery" liée au client actuel (Relais Vocal IA, hôtel), conçu pour être transmis tel quel à une autre session Codex.
- `outputs/2026-08-24-revenue-recovery/` et `kitagentvocal/outils/` : `Kit-validation-revenue-recovery.xlsx` (classeur de suivi d'appels + liste de 10 entreprises de rénovation candidates).
- `.artifacts/revenue-recovery-20260824/` : scripts Node (`build-kit.mjs`, `audit-kit.mjs`) ayant servi à générer/auditer le xlsx.
- `.firecrawl/` : cache probable d'une recherche web (Firecrawl) utilisée pour sourcer les documents.
- Aucun backend, aucune app, aucun déploiement : 100% travail de cadrage.

## État actuel
- **Idéation/validation, aucune exécution commerciale.** Le README est explicite : "statut : hypothèse de nouvelle activité à valider — aucun produit construit".
- Décision stratégique (doc 01) : "REPOSITIONNER" ProofOps comme couche d'assurance de résultat, mais priorité posée comme P0 **après arbitrage** avec le "Relais Vocal IA" (activité en cours de test commercial 60 jours, prioritaire).
- Le scorecard (doc 10, 23 août 2026) reclasse ProofOps en dessous de plusieurs autres pistes (Revenue Recovery Desk 33/40, AI Vendor Trust Pack 33/40, Accessibility Rescue Sprint 32/40, vs ProofOps Outcome Assurance 28/40 et AI Delivery Assurance 28/40). Conclusion : "ProofOps perd aujourd'hui" face au marché rénovation.
- Le kit de validation (doc 11, 24 août 2026 — fichier le plus récent) a fait pivoter le focus concret vers "Revenue Recovery" : un classeur prêt, mais "aucune prospection effectuée".
- Le dossier `kitagentvocal/` (modifié le 24 août à 18h07, dernière trace d'activité) semble être le point de travail actif actuel, plus concret que ProofOps lui-même.
- Aucune décision formelle écrite : le README demande explicitement à Allan de trancher entre `PARKING PROOFOPS` ou `GO PROOFOPS` — rien n'indique que ce choix a été fait.

## Ce qui est complet / incomplet
**Complet :**
- Cadrage stratégique très détaillé (marché, concurrence, offre, PRD, architecture, sécurité, roadmap, sources) pour ProofOps — niveau quasi pré-business-plan.
- Scorecard comparatif rigoureux avec critères de décision (piliers Hormozi, seuils de gates, conditions d'arrêt).
- Kit opérationnel de validation Revenue Recovery : classeur Excel avec 10 entreprises candidates + feuille de suivi d'appels anonymisée + règles de confidentialité.

**Incomplet :**
- Aucun entretien client, aucun pilote payé, aucune prospection réalisée pour ProofOps ni pour Revenue Recovery.
- Aucune ligne de code produit (le PRD et l'architecture technique existent sur papier seulement).
- Arbitrage stratégique final (ProofOps vs Relais Vocal vs Revenue Recovery) non tranché par écrit.
- Le nom ProofOps reste à changer (conflit de nom identifié, pas résolu).

## Prochaines étapes probables
- Trancher l'arbitrage : `PARKING PROOFOPS` (rester sur Relais Vocal IA) ou `GO PROOFOPS`.
- Exécuter le test de validation Revenue Recovery : vérifier 10 entreprises candidates, mener les conversations, chercher un premier acompte/pilote payé.
- Ne construire aucun logiciel (ProofOps ou autre) tant que les gates de validation (5 pilotes payés, 3 agences avec accès réel, etc.) ne sont pas atteintes.

## Revenus
- **Aucun revenu réel documenté.** Tous les chiffres (4 500€ HT + 1 500€/mois, marché 100M€, 6000€ de marge récupérable, chemins "5 clients × 2000€/mois") sont explicitement qualifiés d'**hypothèses/scénarios arithmétiques non validés**, pas de revenus encaissés.
- Le doc 10 distingue lui-même deux jalons non atteints : "10k€ encaissés sur un mois" et "10k€ mensuels pendant 3 mois" — aucun n'est signalé comme atteint.
- Mention d'un "client actuel" (hôtel, Relais Vocal IA) en test commercial de 60 jours, mais aucun montant encaissé n'est cité dans les documents lus.
- Conclusion : **revenu réel = non trouvé**.

## Questions ouvertes
- L'arbitrage Relais Vocal IA vs ProofOps a-t-il été tranché depuis le 24 août ?
- Le "client actuel" (hôtel) génère-t-il déjà du chiffre d'affaires réel sur le Relais Vocal IA, et combien ?
- La prospection des 10 entreprises de rénovation candidates a-t-elle commencé ?
- Le dossier `kitagentvocal/` a-t-il pris le pas définitivement sur ProofOps comme priorité de travail ?
- Le renommage de "ProofOps" (conflit de nom identifié) a-t-il été engagé ?
