# PROJECT_SNAPSHOT — Sauveur2vie

## But
Site web de production pour **Sauveur2Vie (S2V)**, organisme de formation secourisme certifié Qualiopi, avec une filiale **S2IA** (formations IA, catalogue de 18 formations en 6 domaines × 3 niveaux). Refonte complète depuis un ancien site WordPress (bascule déjà faite, plus de fallback WordPress). C'est un vrai client avec une "cliente" identifiée (mention "créer le compte de la cliente" dans le dashboard) — pas une démo.

## Contenu/Stack
- Deux apps dans un seul dépôt Git : le **site vitrine** (racine, Next.js 16 App Router + Tailwind 4, en production sur `sauveur2vie.fr` via Netlify) et le **dashboard CMS** (`dashboard/`, Payload CMS 3.85 sur Next 16, base Postgres Neon, ciblant `dashboard.sauveur2vie.fr`).
- Contenu actuellement codé en dur dans `src/lib/` (formations, domaines, nav/coordonnées légales, LinkedIn, avis Google) ; migration progressive vers le CMS en cours (Phase 2 : Formations, Domaines, FAQ, Coordonnées et médias R2 déjà branchés avec fallback, Live Preview encore à faire).
- Intégrations : formulaire de contact → webhook n8n, flux LinkedIn via widget SociableKit (actuellement figé depuis le 2 juin, contournement manuel en place), avis Google via widget Trustindex.
- Dépôt Git réel (`.git` présent), historique de commits actif jusqu'au 22 août 2026 (retouches photo).

## État actuel
Site **en production et vivant**. Dernière mise à jour de `snapshot.md` : 20 juillet 2026 (rafraîchissement avis Google + posts LinkedIn, vérifié en prod). Le `git log` montre une activité encore plus récente (22 août 2026 : ajustements de recadrage photo). V1 déclarée en production depuis le 2 juillet 2026 (9 items mergés, vérifiés octet pour octet identiques à l'ancien site pour la partie non modifiée).

## Ce qui est complet/incomplet
**Complet / en prod :**
- V1 complète : accueil, S2IA, Formations, À propos, Certifications, Navigation, Contact.
- Phase 2 (branchement CMS) : Formations, Domaines, FAQ, Coordonnées, médias R2 — tous branchés avec repli automatique sur les données codées en dur si l'API échoue.
- Système de revalidation à la demande (`/api/revalidate`) + rebuild Netlify en filet de sécurité.
- Rafraîchissement Avis Google (283→311 avis) et posts LinkedIn (repli manuel documenté).

**Incomplet :**
- Phase 9 (pages légales dans le CMS) : décision prise de NE PAS la faire, restent codées en dur (choix juridique volontaire d'Allan).
- Phase 10 (SEO title/description/OG par le CMS) : non faite.
- Phase 11 (consommation des médias R2 par le site public, au-delà du dashboard) : non faite.
- Live Preview (aperçu temps réel dans le dashboard) : décision d'architecture non tranchée.
- Flux LinkedIn live cassé côté SociableKit depuis le 2 juin 2026 (compte d'un tiers nommé "Anis", accès demandés, pas encore résolu) — un contournement manuel tient la route en attendant.
- Chiffres clés (`HomeStats.tsx`) : champs vides côté CMS, à remplir par Allan.

## Prochaines étapes probables
- Continuer Phase 10 (SEO) et Phase 11 (médias R2 consommés par le site) si le client/Allan le décide.
- Relancer Anis pour réparer la synchro SociableKit, puis nettoyer le contournement LinkedIn manuel (cosmétique, non urgent).
- Décider et implémenter le Live Preview.
- Allan doit créer le compte de la cliente dans le dashboard et, en option, armer la revalidation instantanée (variables d'environnement Netlify).

## Questions ouvertes
- Aucune mention de facture, montant ou paiement trouvée dans les fichiers texte consultés (`snapshot.md`, `historique.md`, `README.md`, `PROCHAINE-ETAPE.md`, `AGENTS.md`) — s'agit-il d'un forfait déjà réglé, d'un abonnement en cours, ou d'une prestation bénévole/partenariat ? À vérifier ailleurs (comptabilité, devis signé).
- Le contournement LinkedIn manuel doit-il être nettoyé maintenant ou attendre la résolution côté Anis ?
- Le dossier `backup-sauveur2vie-2026-07-01` (backup figé du 1er juillet) est-il encore utile vu que le dépôt Git de ce projet contient déjà les tags de rollback correspondants ?
