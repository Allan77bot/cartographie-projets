# PROJECT_SNAPSHOT — synkroniseia (v1, abandonné)

## Relation avec l'autre dossier Synkroniseia
Ce dossier est la **V1 abandonnée** de la marque Synkroniseia. Il a été
remplacé par un pivot complet de positionnement, développé dans
`C:\Users\allan\Projects\Agence IA\Synkroniseia 2.0\`. Ne pas reprendre ce
code : la stack, le positionnement et le copywriting sont obsolètes. Le
dossier "2.0" est le seul vivant (site en ligne à synkroniseia.fr).

## But
Site vitrine one-page pour un "studio digital premium AI-augmented" vendant
des sites web à 700€ livrés en 7 jours, cible principale les restaurateurs
(vertical resto avec module réservation/menu), cibles secondaires indépendants
premium et artisans haut de gamme. Positionnement 100% différent de la V2
(qui vend des systèmes IA sur mesure aux PME, pas des sites web).

## Contenu / Stack
- Next.js 16 (App Router), React 19, TypeScript strict, Tailwind CSS 4,
  Framer Motion (`motion`), GSAP + ScrollTrigger, React Hook Form + Zod.
- Repo Git local, 6 commits (dernier : `b856f27`, 19 mai 2026).
- Une seule page (`app/page.tsx`), Hero avec animation "MockupSequence" 8s
  signature, API route `app/api/lead` pour capter les leads.
- Déploiement visé : Vercel + Cloudflare DNS (`netlify.toml` présent aussi,
  incohérent avec CLAUDE.md qui dit Vercel — signe d'un projet non finalisé).
- Documentation très fournie : `CLAUDE.md` (9.7 Ko, règles strictes de build),
  `STRATEGY.md` (29 Ko, doc stratégique V5), `BRAND-BRIEF.md`.

## État actuel
**Abandonné.** Dernière activité : 19 mai 2026. Aucune trace de suite après
cette date ; le projet "2.0" démarre son propre historique en juillet 2026
avec une stratégie totalement différente (systèmes IA pour PME au lieu de
sites web pour restaurants). Pas de `snapshot.md`/`historique.md` — le
dossier n'a jamais adopté la méthode de session structurée.

## Ce qui est complet / incomplet
**Complet** :
- Structure Next.js fonctionnelle, une page d'accueil avec plusieurs sections
  (Hero, mockup animé, etc.), système de design tokens JSON.
- Documentation stratégique très détaillée (positionnement, cibles, pricing).

**Incomplet / jamais fini** :
- Un seul commit "prêt à déployer" (`55336a3`) puis quelques retouches
  visuelles mineures (logo) — aucune preuve de mise en ligne réelle.
- Pas de `.env.local` vide/rempli vérifiable pour Resend/Calendly.
- Aucune preuve de client, de lead réel, ou de paiement.
- Décision d'hébergement non tranchée (Vercel vs Netlify).

## Prochaines étapes probables
Aucune. Ce dossier n'a plus vocation à être développé — le pivot vers "2.0"
rend son contenu (positionnement resto, pricing 700€/7 jours) caduc.

## Questions ouvertes
- Peut-on supprimer ce dossier (ou l'archiver) maintenant que "2.0" est le
  produit vivant ? Il ne semble contenir aucun actif réutilisable (le design
  system, les polices et le copywriting de "2.0" sont repartis de zéro).
- Le nom de domaine synkroniseia.fr pointe déjà vers le site "2.0" — donc ce
  code v1 n'a jamais été mis en production publique de façon durable.
