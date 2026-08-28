# PROJECT_SNAPSHOT — 9mm / MerchOFF

## But
Refonte design (Atelier Klar) de la home + pages produit du site Shopify de la marque **9MM** (boissons énergisantes, canettes BODY & MIND) pour le client **MERCH OFF / 9MM Suisse SA** (contact marketing/brand : Kevin). Livrable = maquette HTML/CSS/JS validée + guide d'intégration transmis au développeur du thème (Sofiane) qui doit la porter en Liquid dans le thème de prod.

## Contenu / Stack
- Deux sous-dossiers : `9mm-shopify-theme/` (le thème Shopify **de production de Sofiane**, cloné pour audit — Liquid, sections, templates, locales) et `9mm-handoff-sofiane/` (package de livraison propre : README + `GUIDE-INTEGRATION.md` + `preview/` maquette HTML/CSS/JS vanilla + `source-videos/` + assets logo).
- Maquette déployée en aperçu sur Netlify : `9mm-apercu.netlify.app`.
- Documentation projet complète dans `9mm-shopify-theme/docs/` : `ETAT.md`, `JOURNAL.md` (79 Ko d'historique), `DIRECTION_SITE.md`, `MARQUE_9MM.md`, `HOME_COPY.md`, guides de référence (audit du thème existant, charte ton de voix).
- Animations vanilla JS : intro vidéo logo, spirale BODY→MIND, scrub vidéo produit au scroll, scroll-stack "transparence".

## État actuel
**Refonte validée par le client (Kevin)** — version "V2 blanche" retenue. Statut au 23 juin 2026 : **transfert/handoff en cours vers Sofiane** (dév thème), repo GitHub privé créé et Sofiane invité en collaborateur — en attente qu'il accepte l'invitation et intègre. Le portage Liquid final n'est **pas fait par Atelier Klar** (décision actée : c'est Sofiane qui l'exécute dans son thème).

## Ce qui est complet / incomplet
**Complet** : design/maquette des 5 pages (accueil, body, mind, achat-body, achat-mind), 4 modules d'animation JS documentés avec "contrat markup", mapping vers les sections existantes du thème, prix et mécanique panier/abonnement simulés, guide d'intégration très détaillé (metafields, pièges CDN vidéo, ffmpeg).
**Incomplet / en attente** : intégration Shopify réelle (côté Sofiane), plusieurs décisions business non tranchées (§10 du guide) — modèle produit (2 produits ? pack 24 en variante/bundle ?), intervalle de livraison abonnement, HEX officiels de charte, multilingue, destination du formulaire newsletter, assets manquants (avis clients, pixels tracking, favicon/OG).

## Prochaines étapes probables
- Attendre la réponse de Sofiane (acceptation invitation GitHub + retours techniques).
- Trancher les décisions business du §10 avec Sofiane et Kevin.
- Suivre l'intégration Shopify côté Sofiane, assister sans porter le code à sa place.
- Nettoyer les anciennes versions de prototypes (V1 noire) devenues obsolètes.

## Questions ouvertes
- Le handoff a-t-il été accepté par Sofiane et l'intégration a-t-elle réellement démarré (aucune trace après le 23 juin dans ce dossier) ?
- Prestation facturée ? Aucune facture ou mention de paiement trouvée dans le dossier.
- Le dossier est-il toujours actif ou en pause faute de retour de Sofiane/Kevin (dernière modification 23 juin 2026, plus de 2 mois avant la date d'audit) ?
