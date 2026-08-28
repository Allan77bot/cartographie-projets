# PROJECT_SNAPSHOT.md — PROTOCOLE-RECHERCHE

## But
Kit méthodologique générique et réutilisable pour faire mener à un agent IA une étude de marché sérieuse (scraping web, veille concurrentielle, fact-check triangulé) et produire deux livrables prêts pour un rendez-vous commercial : une présentation HTML interactive et un rapport/devis PDF. Conçu pour être appliqué à n'importe quel projet d'Allan (pas spécifique à un client).

## Contenu/Stack
- `PROTOCOLE.md` — chef d'orchestre qui enchaîne 7 sous-agents Claude Code de bout en bout.
- `agents/` — les 7 sous-agents installables : cadrage, scraping, fiabilité (fact-check A→E), analyse-marché (TAM/SAM/SOM), synthèse, présentation HTML, PDF. Chacun est un fichier `.md` substantiel (~8-12 Ko).
- `methodes/` — méthode de recherche, fiabilité des sources, outils de scraping (Firecrawl/Playwright/Claude-in-Chrome), outils MCP, skills utilisés.
- `templates/` — gabarits prêts à l'emploi : `presentation.html` (Inter + Chart.js, toggle clair/sombre), `generate_pdf.py` + `charts.py` (reportlab/matplotlib), `sources.csv` (journal de traçabilité).
- `checklists/` — contrôle qualité recherche et livraison.
- `exemples/exemple-brief.md` — brief type rempli.
- Stack : Python (reportlab, matplotlib), HTML/JS statique (Chart.js via CDN), outils MCP de scraping web (Firecrawl en priorité).

## État actuel
Dernière modification 1er juillet 2026. Pas de repo git détecté (contrairement aux dossiers HERMES). Le kit paraît terminé/figé dans une version cohérente : les 7 sous-agents existent tous, les templates et checklists sont présents, le README documente une "utilisation en 10 secondes" en copier-coller. Aucune trace de session de suivi (`snapshot.md`/`historique.md` absents) — contrairement aux 3 autres dossiers audités, ce qui suggère un kit livré une fois puis non retouché depuis, plutôt qu'un chantier actif suivi de près.

## Ce qui est complet/incomplet
**Complet** : les 7 sous-agents, les méthodes de fiabilité des sources, les templates HTML/PDF, les checklists, un exemple de brief. La documentation d'usage est claire et autonome (copier-coller une phrase pour démarrer).
**Incomplet** : pas de preuve dans le dossier qu'il ait été utilisé en conditions réelles sur un projet depuis sa création (pas de dossier de sortie/output archivé, pas de journal de session) ; pas de suivi de version (`snapshot.md`/`historique.md` absents, contrairement à la convention Allan pour les projets actifs) ; dépendance à des outils externes (Firecrawl, Playwright ou Claude-in-Chrome) dont la disponibilité/le coût actuel n'est pas vérifiée ici.

## Prochaines étapes probables
1. Tester le protocole sur un vrai sujet de recherche pour valider qu'il tourne de bout en bout.
2. Si utilisé, archiver un exemple de sortie réelle (présentation + PDF) pour prouver la valeur du kit.
3. Ajouter `snapshot.md`/`historique.md` si le kit redevient un chantier actif, sinon le laisser en l'état comme outil de référence figé.

## Questions ouvertes
- Ce protocole a-t-il déjà été exécuté sur un vrai sujet (client Atelier Klar, étude interne) depuis le 1er juillet ?
- Les 3 outils de scraping listés en prérequis (Firecrawl/Playwright/Claude-in-Chrome) sont-ils toujours connectés/à jour ?
- Ce kit est-il un doublon partiel de fonctions déjà couvertes par le skill `market-research` ou d'autres skills business listés dans l'environnement Claude Code d'Allan ?

## Revenus
Non trouvé — c'est un outil interne de méthode, pas un projet client ; aucune trace de revenus générés directement par ce kit.
