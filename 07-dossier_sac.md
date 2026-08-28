# PROJECT_SNAPSHOT — dossier sac (Atelier Acidulé)

## But
Prestation de retouche photo produit pour la marque **Atelier Acidulé** (sacs au crochet faits main, univers Italie/Méditerranée, compte Insta @atelier_acidule), en vue de son site vitrine. Pas de développement de site ici — uniquement production d'images (packshots).

## Contenu/Stack
- Pas de code applicatif : projet de production visuelle piloté par Claude Code + MCP Higgsfield (modèle `nano_banana_pro`) + Python/Pillow pour le compositing.
- `CLAUDE.md` / `snapshot.md` / `historique.md` : mémoire de session (méthode organisée, snapshot réécrit à chaque session, journal daté append-only).
- `Pool/hieggfield-prompt.md` : brief client V1 (jugé « nul » par Allan, abandonné en session 2).
- `_retouche/` : ateliers de régénération réutilisables — `catalogue_manifest.json` (prompt exact par sac), `catalogue_index.md`, `sources_catalogue/` (27 sources), `calib/` (calibrage V1/V2 + planche-contact), scripts (`rebuild.py`, `compose.py`).
- `public/images/` : livrables finis (catalogue 27 packshots + anciens livrables session 1 à trancher).

## État actuel
**Terminé côté production** : 27 packshots livrés et contrôlés (session 2, 26/06/2026), en attente de revue finale par Allan et d'intégration dans le vrai repo du site de la marque. Aucune activité après le 26/06/2026 (dossier non modifié depuis).

## Ce qui est complet/incomplet
**Complet :**
- 27 modèles de sacs retouchés en méthode « retouche IA fidèle » (fond crème, lumière chaude, cadrage V2), qualité contrôlée (agents + revue manuelle), 2 corrections ciblées appliquées.
- Outillage de régénération/swap documenté et réutilisable sans repayer le détourage.

**Incomplet / en attente :**
- Validation finale d'Allan sur la planche-contact (`_retouche/calib/_apercu_catalogue.jpg`).
- Décision non prise : le catalogue de 27 remplace-t-il les 6 anciens livrables de la session 1 encore présents dans `public/images/` ?
- Visuel « Emballage » (coffrets logo) — optionnel, non traité.
- Intégration effective de `public/images/catalogue/` dans le repo réel du site de la marque (ce dossier n'est pas ce repo — c'est un atelier de production à part).

## Prochaines étapes probables
- Allan valide/pointe les sacs à reprendre sur la planche-contact.
- Trancher le remplacement des anciens livrables.
- Copier les livrables finaux dans le repo du site Atelier Acidulé (repo non présent dans ce dossier).

## Questions ouvertes
- Ce dossier est-il un livrable en attente de facturation, ou une prestation déjà réglée en amont (aucune trace de facture/montant/paiement dans les fichiers texte lus) ?
- Le site vitrine d'Atelier Acidulé existe-t-il déjà ailleurs dans les projets d'Allan, ou est-ce encore à créer ?
- Le projet est-il abandonné (aucune activité depuis 2 mois) ou simplement en pause en attendant un retour client ?
