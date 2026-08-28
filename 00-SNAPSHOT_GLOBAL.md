# Snapshot global — tous les projets (C:\Users\allan\Projects)

Cartographie réalisée le 2026-08-28. Chaque projet a aussi un `PROJECT_SNAPSHOT.md` dans son propre dossier avec le détail complet. Ce document est la vue macro pour décider quoi garder/couper.

Règle appliquée : tout ce qui est marqué "non trouvé" pour les revenus signifie qu'aucune facture, montant payé, ou preuve écrite de paiement réel n'a été trouvée dans les fichiers — pas que le projet n'a pas de valeur.

---

## 🟢 Actifs / en production réelle

### SAAS CORTEX (SellerScale)
`SAAS\SAAS - CORTEX` (+ code dans `30_TECH/33_DEV_MVP/cortex-iq/`)
- **But** : SaaS B2B qui automatise par IA une méthodo de sourcing produit Amazon FBA Private Label, abonnement mensuel pour débutants francophones. Renommé "SellerScale" (sellerscale.ai).
- **Stack** : Next.js 16, React 19, TS, Tailwind v4, Clerk, Neon/Drizzle, Stripe (mode LIVE), Vercel, Vitest, extension Chrome (soumise au Web Store).
- **État** : très actif, modifié quotidiennement fin août 2026, commits fréquents.
- **Maturité** : **MVP en production avec utilisateurs réels** (emails/IDs Clerk, essais 7 jours, crons de facturation, 21 tickets support en attente dont 6 liés à de l'argent).
- **Revenus** : Stripe en mode live, pricing 39/79/129 €/mois. Preuves indirectes de facturation réelle (un prélèvement contesté de 350€, remboursements demandés) mais MRR exact non trouvé.
- **C'est le projet le plus abouti de toute la cartographie.**

### Sauveur2vie
`Clients\Sauveur2vie`
- **But** : site + dashboard pour un organisme de formation secourisme certifié Qualiopi (S2V) et sa filiale IA (S2IA). Client réel, site en ligne (sauveur2vie.fr).
- **Stack** : Next.js 16 + Tailwind 4 (site) + Payload CMS 3.85/Postgres Neon (dashboard), Netlify.
- **État** : actif, commits jusqu'au 22 août 2026. V1 livrée le 2 juillet, migration progressive du contenu vers le CMS en cours.
- **Maturité** : quasi-fini / live — le projet client le plus mature et stable de la cartographie.
- **Revenus** : non trouvé dans les fichiers (mais engagement client manifestement réel — à vérifier côté devis/compta).
- Voir aussi `Clients\backup-sauveur2vie-2026-07-01` : simple sauvegarde figée du 1er juillet, pas un projet séparé — candidat à suppression (les tags Git équivalents existent déjà dans le repo).

### AK NUTRITION
`Clients\AK NUTRITION`
- **But** : système RH + compta automatisé complet (recrutement, onboarding, fin de contrat avec signature électronique, mini-SaaS compta OCR) pour un franchisé BioTechUSA. Relation client active et récurrente.
- **Stack** : N8N (VPS Hostinger), Airtable, Notion, Drive/Sheets, Gmail, Slack, Netlify, Render.
- **État** : en production active, modifié le 25 août 2026, plusieurs modules déployés et utilisés en réel par le client.
- **Maturité** : quasi-fini, gros volume de modules livrés ; quelques branches en attente de fusion.
- **Revenus** : non trouvé (le dossier "facture" documente la compta du client, pas la facturation d'Allan).

### Agence IA / Synkroniseia 2.0
`Agence IA\Synkroniseia 2.0`
- **But** : atelier de systèmes IA sur mesure pour PME françaises. Depuis mi-août, focus resserré 60 jours sur "Relais Vocal IA" (appels manqués, hôtellerie).
- **Stack** : Astro 7, déployé en continu sur Netlify, site réel en ligne (synkroniseia.fr), n8n/Airtable/Calendly.
- **État** : vivant, actif jusqu'au 22 août 2026, 19 pages en prod, SEO/RGPD faits.
- **Maturité** : produit déployé mais stratégie commerciale instable (deux pivots en un mois : Synkroniseia classique → Relais Vocal IA → réflexion ProofOps). Repo très encombré (58 900+ fichiers dans `.tmp/`, `livrables/`, `outputs/` — nettoyage à faire).
- **Revenus** : non trouvé — un pilote client (Tony, hôtel) en test 60 jours, sans confirmation de paiement encaissé.
- C'est le dossier vivant du couple ; **`synkroniseia` (racine, v1) est son prédécesseur mort** (voir section abandons).

### Double-AS (AIOS Atlas)
`Double-AS`
- **But** : système agentique (agent "Atlas") qui pilote les deux activités d'Allan+Alphim — Atelier Klar (design web) et Synkronise IA (agence automatisation). Contient le sprint commercial "Relais Vocal IA" avec un premier client pilote (Tony, groupe hôtelier).
- **Stack** : Python, N8N, Airtable, Mammouth (routeur multi-LLM), Obsidian (vault mémoire), git privé GitHub, skills Claude Code internes.
- **État** : très actif, dernier commit 27 août 2026, 12+ branches en cours.
- **Maturité** : quasi-fini côté infra/gouvernance (vault, contrats, cockpit fonctionnel) ; côté business, stade early.
- **Revenus** : "non encaissé" — devis accepté par un client (Tony) le 21/08 pour 1000€ + 300€/mois, statut "proposition acceptée" mais pas de preuve d'acompte encaissé.
- **C'est le cœur opérationnel de toute l'activité "Agence IA".**

---

## 🟡 Livrés / terminés (pas abandonnés, juste finis)

### 9mm - MerchOFF
`Clients\9mm - MerchOFF`
- **But** : refonte design (Atelier Klar) de la home + pages produit Shopify pour une marque de boissons énergisantes.
- **État** : design validé par le client, handoff transmis au développeur du thème (Sofiane), rien depuis — travail d'Allan terminé, en attente d'intégration côté client.
- **Maturité** : design terminé, intégration hors périmètre.
- **Revenus** : non trouvé.

### atelier-acidule
`Clients\atelier-acidule`
- **But** : site vitrine premium pour une créatrice de sacs au crochet, commande/SAV via Instagram DM.
- **Stack** : Astro 5, Netlify, GitHub.
- **État** : refonte terminée et déployée le 27 juin 2026, en pause depuis (attend validation finale cliente + merge vers main).
- **Maturité** : livrable technique complet et propre.
- **Revenus** : non trouvé (montants présents = prix de vente des sacs de la cliente, pas la rémunération d'Allan).

### dossier sac (Atelier Acidulé — packshots)
`Clients\dossier sac`
- **But** : prestation de retouche photo produit (27 packshots) pour la même marque de sacs.
- **État** : production terminée et contrôlée, en attente de validation finale Allan et d'intégration dans le vrai repo du site — 2 mois sans suite.
- **Maturité** : quasi-fini mais jamais formellement clôturé.
- **Revenus** : non trouvé.

### Formation
`Formation`
- **But** : formation pro de 9h sur Claude livrée en présentiel à une agente Allianz ("S2IA Medelia"), objectifs Qualiopi.
- **État** : mission ponctuelle livrée les 4-5 août 2026, pack complet remis à la cliente + rapport SEO bonus. Terminée, pas abandonnée.
- **Maturité** : livraison complète, mais `decisions.md` jamais rempli.
- **Revenus** : non trouvé (aucune facture dans les fichiers).

---

## 🟠 Prototypes avancés à l'arrêt / stratégie non tranchée

### scribe-app (SAAS Scribe)
`scribe-app`
- **But** : SAAS de notes vocales/écrites → coordination active d'équipe (tâches, passation), cible équipes en relais 3×8.
- **Stack** : Next.js 16 + React 19 + Supabase (Auth/RLS) + Stripe (TEST uniquement) + IA (Whisper, Claude).
- **État** : dernier commit 28 juin 2026, ~2 mois d'inactivité. Bloqué en prod par une migration DB non appliquée.
- **Maturité** : prototype avancé, proche MVP mais jamais mis en ligne pour de vrais clients ; Stripe jamais passé en LIVE.
- **Revenus** : non trouvé.
- **Doublon obsolète associé** : `SAAS\scribeappdossier` — version antérieure figée au 14 juin, sans Stripe ni IA, mais contenant en plus le journal de bootstrap de l'agent Hermes (Mem0, manifeste "soul") → à extraire avant suppression si cette partie a de la valeur.

### ProofOps
`ProofOps`
- **But** : dossier de recherche stratégique pour une nouvelle activité — d'abord "assurance de résultat" pour agences IA, puis pivot vers "Revenue Recovery Desk" (récupération de leads perdus, PME rénovation), jugé plus prometteur par un scorecard interne.
- **État** : 100% documentaire, idéation/validation pure, aucun produit construit, aucune prospection réelle effectuée. Nom de code à changer (conflit identifié). Le focus opérationnel semble avoir glissé vers `kitagentvocal/`.
- **Maturité** : pré-business-plan très soigné, zéro exécution commerciale.
- **Revenus** : non trouvé — tous les chiffres cités sont des hypothèses.
- **Décision requise** : arbitrer PARKING vs GO, écrit nulle part.

### Morfo V2/V3
`Morfo V2`
- **But** : app iPad pour vendeurs AK Nutrition (calcul TMB/TDEE, capture email, vente de programme nutrition 49/79€).
- **Stack** : V2 = 3 sites HTML/JS/CSS statiques par boutique (obsolètes). V3 = refonte React 19+Vite+Tailwind+PWA, une app "recettes" en double implémentation concurrente non tranchée.
- **État** : dossier touché le 23 août mais contenu réel (code) datant de mars-mai 2026 — pas de preuve de travail après mi-mai malgré la date de modif récente.
- **Maturité** : prototype avancé / MVP partiel, génération PDF en attente, deux pistes techniques concurrentes non tranchées.
- **Revenus** : non trouvé.

### letoileduchef-demo
`Clients\letoileduchef-demo`
- **But** : démo de prospection interne (restaurant réel mais Synkroniseia n'est PAS son prestataire — aucun contrat).
- **Stack** : Next.js 16 + Tailwind 4 + GSAP, données légales et tarifs explicitement fictifs.
- **État** : développement avancé (Phases 0-4 faites) arrêté au 26 mai 2026, 3 mois d'inactivité.
- **Maturité** : prototype avancé jamais poussé jusqu'au démarchage confirmé.
- **Revenus** : non trouvé (pack "700€+49€/mois" = gabarit commercial simulé).

---

## 🔴 Abandonnés / morts

### synkroniseia (v1, racine)
`synkroniseia`
- Site vitrine 700€/7 jours pour restaurateurs. Abandonné depuis le 19 mai 2026, remplacé intégralement par `Agence IA\Synkroniseia 2.0` (positionnement et stack différents). Aucun actif réutilisable identifié. **Candidat clair à la suppression.**

### backup-sauveur2vie-2026-07-01
`Clients\backup-sauveur2vie-2026-07-01`
- Sauvegarde figée (2 zips, ~94 Mo) redondante avec des tags Git déjà présents dans le repo `Sauveur2vie`. **Candidat à suppression/archivage froid.**

### linkedin_n8n_pack_complet_v2
`Agence IA\linkedin_n8n_pack_complet_v2`
- Pack de workflows N8N pour automatiser la publication LinkedIn. POC fonctionnel partiel (page entreprise validée, profil perso jamais testé), inactif depuis le 24 juillet 2026.

### PROCESS/PROTOCOLE-RECHERCHE
`PROCESS\PROTOCOLE-RECHERCHE`
- Kit générique d'étude de marché (7 sous-agents + génération PDF). Structurellement complet mais figé depuis le 1er juillet, aucune preuve d'usage réel.

---

## ⚙️ Outillage interne / méthode (pas des projets clients)

### HERMES/hermesdossier + HERMES/hermes-skills
- Agent "Hermes" (VPS Hostinger, co-gérant Atelier Klar) : mémoire, outils, runbooks, 3 skills packagés (cold-email-grounded, skill-forge, email-qa).
- Actifs jusqu'au 27 juin 2026, puis silence. Skills installés sur le VPS mais pilote de prospection jamais lancé.

### PROCESS/PILOTE - Kit Site Web
- Méthode réutilisable pour construire les sites Atelier Klar, étendue à un volet prospection commerciale complet (ICP, briefs, outreach). Active jusqu'au 7 juillet 2026 ; pipeline commercial avancé mais aucun envoi/signature confirmés.

### Clipping
`Clipping`
- Outil perso local (Next.js) qui transforme une vidéo longue en clips verticaux sous-titrés pour TikTok/Reels/Shorts. Pipeline FFmpeg → Whisper → Claude/GPT → Remotion fonctionnel, 100% local, jamais déployé. Modifié le 14 août 2026 — actif.
- Le fichier `_to_delete_archive.tar.gz` est un backup de refactor à nettoyer, pas un signe d'abandon.

### SAAS/business-plan-fileforge
`SAAS\business-plan-fileforge`
- Business plan pour un SaaS multi-tenant + hardware RFID (paintball/airsoft), 3 associés (Hubert 52%, Allan 24%, Alphim 24%). 100% documentaire, figé depuis le 15 juillet 2026 (~6 semaines), bloqué sur un chiffrage attendu d'un associé externe.
- **Revenus** : non trouvé, pas de produit ni de client.

---

## 📁 Dossiers ignorés (pas des projets)

- `05_DOUBLE_AS_SHARED` (racine) — vide.
- `11_AUDIT_SOURCES` (racine) — vide.
- `SAAS`, `Clients`, `Agence IA`, `PROCESS`, `HERMES` — ce sont des dossiers de regroupement Windows, pas des projets en soi ; leurs sous-dossiers sont traités individuellement ci-dessus.
- `desktop.ini` présents dans plusieurs dossiers de regroupement — artefacts Windows sans intérêt.

---

## Résumé (6-8 lignes)

**Le plus abouti** : SAAS CORTEX/SellerScale — seul projet en production réelle avec Stripe live et utilisateurs payants identifiables (montant exact non confirmé par les fichiers). Juste derrière : Sauveur2vie (client réel, site live) et AK Nutrition (système RH/compta opéré en continu pour un vrai client).

**Le plus proche de générer des revenus récurrents nouveaux** : Double-AS / Synkroniseia 2.0 via le sprint "Relais Vocal IA" — un client pilote (Tony) a accepté un devis (1000€ + 300€/mois) mais rien ne prouve un encaissement réel à ce jour ; c'est une conversion à confirmer, pas un revenu acquis.

**Le plus abandonné** : `synkroniseia` (v1) et `backup-sauveur2vie-2026-07-01` — aucun actif réutilisable, candidats francs à la suppression. `linkedin_n8n_pack_complet_v2` et `PROTOCOLE-RECHERCHE` sont figés aussi mais gardent une valeur d'outillage réutilisable.

**Le plus incertain stratégiquement** : ProofOps — beaucoup de réflexion écrite, zéro décision tranchée, zéro exécution. Et Synkroniseia 2.0 elle-même, qui a pivoté deux fois en un mois sans clore le sujet.

**Aucun revenu réel confirmé par écrit** n'a été trouvé nulle part dans la cartographie — uniquement des devis acceptés, des pricings affichés, ou des indices indirects (Stripe live, prélèvements contestés). Si Allan veut suivre ses revenus réels, rien dans ces dossiers ne fait actuellement ce travail.
