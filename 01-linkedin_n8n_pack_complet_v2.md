# PROJECT_SNAPSHOT — linkedin_n8n_pack_complet_v2

## But
Pack de workflows N8N pour publier automatiquement du contenu sur LinkedIn, sur deux destinations : la page entreprise (Organization ID 109572605) et le profil personnel d'Allan Morjon (Person URN urn:li:person:UbR3KoqVrG). Outil interne pour l'automatisation de la présence LinkedIn d'Allan et/ou de son agence — aucune trace de packaging commercial (pas de page de vente, pas de pricing, pas de licence). C'est un outil interne, pas un produit à vendre.

## Contenu / Stack
- N8N (workflows JSON, credential `linkedInCommunityManagementOAuth2Api`).
- 4 workflows dans `workflows/` :
  - `01_test_publication_texte.json` — test publication page entreprise (validé HTTP 201).
  - `02_template_production_texte.json` — template production (page entreprise).
  - `03_template_publication_profil_personnel.json` — template publication profil personnel (non testé en prod).
  - `04_template_multi_destination.json` — routeur choisissant dynamiquement page vs profil.
- `config/linkedin.config.json` — configuration (IDs, URNs).
- `docs/` : `PUBLICATION_PAGE_VS_PROFIL.md`, `SOURCES.md`, `TROUBLESHOOTING_RAPIDE.md`.
- Doc d'entrée : `00_COMMENCER_ICI.txt` → `README_ULTRA_COMPLET.md` → `docs/PUBLICATION_PAGE_VS_PROFIL.md` → `MESSAGE_A_TRANSMETTRE_A_CODEX.txt` → workflows.
- `MESSAGE_A_TRANSMETTRE_A_CODEX.txt` : brief destiné à transmettre l'état du projet à un autre agent (Codex), preuve d'un usage multi-outils / multi-session par Allan.

## État actuel
- Publication page entreprise : **validée** (HTTP 201, Organization ID confirmé).
- Récupération Person ID / URN du profil personnel : validée.
- Publication profil personnel : **workflow prêt mais jamais testé en conditions réelles**.
- Pas de garde-fou (anti-doublon, validation humaine, journalisation, gestion d'erreur) confirmé comme implémenté dans les workflows — le message à Codex les liste comme règles à respecter, pas comme acquis.
- Explicitement documenté : la Community Management API ne permet PAS l'envoi de DM LinkedIn classiques (limite connue, pas un manque à corriger).
- Dernière modification : 24 juillet 2026 — projet inactif depuis (pas de mise à jour en plus d'un mois à la date d'audit).

## Ce qui est complet / incomplet
**Complet :**
- Documentation claire de configuration (IDs, credential, endpoints).
- Workflow de test page entreprise fonctionnel et validé.
- Template multi-destination écrit.

**Incomplet :**
- Test réel de publication sur le profil personnel (bloquant avant usage en prod).
- Anti-doublon, validation humaine, journalisation, gestion d'erreur — mentionnés comme requis, statut d'implémentation non vérifié dans ce audit (nécessiterait lecture du JSON des workflows).
- Aucune preuve d'usage récurrent depuis fin juillet.

## Prochaines étapes probables
- Lancer le premier test de publication sur le profil personnel et obtenir un HTTP 201.
- Décider si le pack reste un outil interne ou est industrialisé (documentation soignée type "pack" suggère qu'il a été pensé pour être potentiellement dupliqué/vendu, mais rien ne l'indique explicitement).
- Vérifier si le projet est toujours utilisé activement ou en dormance depuis juillet.

## Questions ouvertes
- Ce pack est-il encore utilisé aujourd'hui, ou abandonné après la phase de test ?
- Le workflow tourne-t-il réellement dans une instance N8N (Hostinger KVM4), ou reste-t-il un artefact de configuration jamais déployé en continu ?
- Les garde-fous demandés (anti-doublon, gestion d'erreur, journalisation) ont-ils été ajoutés aux JSON, ou seulement listés comme TODO ?
- Le nom "pack complet" suggère une intention de réutilisation/vente — confirmée ou pas par Allan ?
