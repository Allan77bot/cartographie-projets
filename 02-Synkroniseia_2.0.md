# PROJECT_SNAPSHOT — Synkroniseia 2.0 (vivant)

## Relation avec l'autre dossier Synkroniseia
Ce dossier est le **pivot vivant** de la marque Synkroniseia, qui remplace
totalement `C:\Users\allan\Projects\synkroniseia\` (V1, Next.js, positionnement
"sites web pour restaurants à 700€", abandonné mi-mai 2026, aucune suite).
Ici, à partir de juillet 2026, le positionnement change radicalement :
Synkroniseia devient un atelier de **systèmes IA sur mesure pour PME**
(20-150 salariés), pas un studio de sites web. Nouveau stack (Astro au lieu
de Next.js), nouveau copywriting, nouveau design system — rien n'est repris
du dossier V1. Le site est réellement en ligne : **synkroniseia.fr**.

Important : à l'intérieur même de ce dossier "2.0", une **deuxième
réorientation** a eu lieu le 14-22 août 2026 — priorité de 60 jours donnée à
une offre "Relais Vocal IA" (voix IA pour appels entrants non répondus,
hôtellerie/résidences), au détriment de la prospection Synkroniseia
classique (sites web, Back-Office, SaaS). Une piste "ProofOps" (service
d'assurance de résultat pour agences n8n/Make/Zapier) a aussi été
documentée le 22 août mais reste au stade décision, isolée dans un dossier
`ProofOps/` séparé, sans arbitrage tranché par Allan.

## But
Vendre des "systèmes IA qui rapportent" à des PME françaises : *le
Diagnostic* (porte d'entrée payante, 900-1500€ HT crédités), *le Moteur
Commercial* (offre phare), *le Back-Office Autonome*, *le Suivi*, *le
Dossier de propriété* — le tout mesuré en "clients récupérés" et "heures
rendues", et appartenant au client (pas de lock-in). Depuis mi-août, focus
commercial temporaire sur une offre unique test : "Relais Vocal IA managé"
pour hôtels/résidences (2900€ HT setup + 490€ HT/mois), en pilote avec un
client nommé "Tony".

## Contenu / Stack
- **Site public** (`site/`) : Astro 7, sortie statique, déployé en continu
  sur Netlify (branche `agent/synkroniseia-site`) → https://synkroniseia.fr.
  19 pages au dernier état connu (accueil, diagnostic, moteur-commercial,
  back-office, méthode, cas-clients, à-propos, contact, ressources, blog en
  friche, questionnaire caché, pages légales).
- **Contenu source figé** : `Synkroniseia-Package/` (stratégie, positionnement,
  offre/pricing, copywriting final des 9 pages, procédures métier, kit RDV) —
  dossier read-only, ne pas réécrire.
- **Design system** : `synkroniseia-design-system/` (tokens JSON/CSS, polices
  Fraunces/Geist/JetBrains Mono, logo, composants JSX de référence) —
  read-only.
- Intégrations : formulaires → n8n (webhooks) → Airtable, Calendly embed,
  lead magnets PDF (guide "5 automatisations"), planning LinkedIn.
- Mémoire de session en place : `CLAUDE.md`, `snapshot.md`, `historique.md`,
  `PROCHAINE-ETAPE.md` — méthode structurée bien suivie (contrairement à la
  V1).
- Beaucoup de dossiers annexes : `.tmp/` (worktrees Git isolés, très
  volumineux), `livrables/`, `outputs/`, `marketing/`, `A-DEPLOYER-NETLIFY/`
  (paquet statique prêt au drag-and-drop, redondant avec le déploiement
  continu Netlify).

## État actuel
**Vivant, mais en pause sur son positionnement d'origine.** Le site
Synkroniseia (systèmes IA / Diagnostic / Moteur Commercial) est construit,
en ligne, avec plusieurs itérations de design et de SEO jusqu'au 22 août
2026. Depuis le 14 août 2026, Allan a mis la prospection Synkroniseia
classique en pause 60 jours pour tester une offre "Relais Vocal IA" plus
étroite. Une piste "ProofOps" (pivot B2B agences d'automatisation) a été
étudiée le 22 août mais aucune décision (GO/PARKING) n'a encore été prise —
c'est le blocage actif le plus récent.

## Ce qui est complet / incomplet
**Complet** :
- Site Astro en production, 19 pages, SEO technique traité (sitemap,
  noindex ciblés, JSON-LD, Open Graph), RGPD (mentions légales, confidentialité,
  consentement Calendly), formulaires connectés à n8n/Airtable.
- Lead magnet PDF produit et diffusé ; planning éditorial LinkedIn écrit.
- Historique de décisions et de tests très documenté (offre, pricing,
  ciblage sectoriel, benchmark 17 prestataires vocaux).

**Incomplet** :
- Blog : socle technique fait mais verrouillé (`BLOG_PUBLICATION_ENABLED =
  false`), aucun article publié.
- Plusieurs branches/PR en attente de GO explicite d'Allan (questionnaire UX,
  workflow n8n Blog vers OS) — non fusionnées en production.
- Décision stratégique majeure non tranchée : continuer Synkroniseia
  (Diagnostic/Moteur Commercial) vs. pivoter durablement sur Relais Vocal IA
  vs. explorer ProofOps.
- Cas clients affichés avec chiffres `[à valider]` — aucun chiffre client
  confirmé à ce jour.
- Repo Git détecté comme dossier (`.git` présent) mais `git log` échoue
  ("not a git repository") depuis l'environnement de cet audit — à vérifier
  (accès distant GitHub `Allan77bot/Auditsynkronise` mentionné dans les
  fichiers de mémoire, mais fetch a échoué plusieurs fois selon
  `PROCHAINE-ETAPE.md`).

## Prochaines étapes probables
1. Allan doit trancher explicitement : GO Synkroniseia classique / GO Relais
   Vocal IA / GO ProofOps / parking d'une ou plusieurs pistes.
2. Si Relais Vocal IA est confirmé : lancer le pilote payant avec "Tony",
   choisir la plateforme technique (Retell vs ElevenLabs Agents) sur le banc
   d'essai à 20 scénarios déjà préparé.
3. Si Synkroniseia classique reprend : fusionner les PR en attente
   (questionnaire UX, blog), reprendre la prospection outbound (secteurs
   recrutement/intérim et courtage crédit/financement déjà étudiés).
4. Nettoyer les dossiers `.tmp/`, `livrables/`, `outputs/` (très nombreux
   fichiers, dont beaucoup de doublons de builds) — impact fort sur la
   lisibilité du repo (58 900+ fichiers listés lors de cet audit).

## Questions ouvertes
- Le dossier `ProofOps/` (séparé, `C:\Users\allan\Projects\ProofOps\`) doit-il
  être traité comme un troisième projet à part entière dans la cartographie
  globale, ou comme une simple annexe de Synkroniseia 2.0 ?
- Statut réel du dépôt GitHub distant (`Allan77bot/Auditsynkronise`) : les
  fichiers de mémoire mentionnent des échecs de fetch répétés en août 2026 —
  le lien avec le remote est-il cassé ?
- Aucune preuve de revenu trouvée (voir ci-dessous) : le pilote "Tony" est-il
  payant à ce jour, ou reste-t-il un simple test technique ?

---

## Revenus
**Non trouvé.** Aucune intégration Stripe, aucune facture, aucun chiffre
d'affaires confirmé dans les fichiers consultés. Les seuls montants présents
sont des **hypothèses de pricing non validées** : Diagnostic 900-1500€ HT,
Relais Vocal IA 2900€ HT + 490€ HT/mois, objectif "2320€ d'acomptes encaissés
et 980€ de MRR" fixé comme *objectif* à J60 (pas un résultat atteint). Le
pilote client "Tony" est mentionné comme test technique/commercial, sans
confirmation de paiement encaissé dans les documents lus.
