# PROJECT_SNAPSHOT — AK NUTRITION

## But
Système d'automatisation RH + comptable complet pour **AK Nutrition SARL** (franchisé BioTechUSA, boutiques Meaux/Noisy-le-Grand/Aulnay-sous-Bois, dirigeant Adam Halin), construit et maintenu par Allan sous le nom d'agence **SynkroniseIA**. Couvre tout le cycle employé : recrutement → onboarding alternant (avec école, entreprise, signature d'annexe) → gestion courante → fin de contrat (rupture CERFA signée électroniquement) — plus un mini-SaaS de comptabilité (import/OCR/validation de factures) et un site vitrine nutrition ("Morfo", calcul TMB/programmes).

## Contenu / Stack
Dossier le plus vaste et le plus actif des trois audités, structuré en sous-projets quasi indépendants, chacun avec son propre `CLAUDE.md`/`snapshot.md`/`historique.md` :
- **`onboarding/`** — le cœur du système : ~16 workflows N8N, pages Netlify + petit serveur Express (Render) pour l'espace alternance/école, base Airtable "Onboarding", Notion (Employés/Écoles), Google Drive, Gmail. Documenté en détail dans `CARTOGRAPHIE-FLUX-RH.md` à la racine.
- **`fin de contrat/`** — mini site Netlify de signature électronique du CERFA de rupture d'apprentissage (pdf.js/pdf-lib côté navigateur) + ~15 workflows N8N, écriture dans Notion, archivage Drive.
- **`facture/`** — mini SaaS compta : page d'import Netlify → OCR Mistral via N8N → IA de classification → validation Airtable → export Qonto. Mono-client (Adam), en V1 fonctionnelle.
- **`ak-nutrition-espace-alternance/`** — serveur Node/Express + pages HTML pour écoles et entreprises (répertoire séparé avec son propre repo).
- **`Morfo V2` / `Morfo Finalll`** — site marketing/nutrition (calculateur TMB, programmes, recettes) pour les boutiques, avec ses workflows N8N et exports.
- Stack transverse : N8N (VPS Hostinger), Airtable, Notion, Google Drive/Sheets, Gmail, Slack (canaux définis), Netlify, Render.

## État actuel
**Projet vivant et en production**, dernière modification 25 août 2026 (le plus récent des trois). Plusieurs modules sont **déployés et utilisés en réel par Adam** :
- Onboarding : Lot 5 livré le 23/08/2026, fonctionnalités en test par Adam sur de vrais dossiers alternants (Issam, Demba).
- Fin de contrat : v28 en production, validée par Allan en conditions réelles ; un chantier "fin normale de contrat" codé et testé localement mi-fin août, en attente de déploiement (go d'Allan).
- Facture (compta) : V1 en production, bug d'import en lot corrigé et vérifié le 30/06 ; le dashboard Airtable reste en pause (widgets à `0.00`).
- Plusieurs branches Git ouvertes (`feat/infos-cles-dashboard`, `feat/retours-adam-2026-08-19`, `feat/emails-partenaires-2026-08-10`) en attente de fusion.

## Ce qui est complet / incomplet
**Complet** : parcours onboarding de bout en bout (candidature → école → entreprise → signature annexe → dossier employé), signature électronique fin de contrat avec preuve scellée RSA-SHA256, import/OCR factures avec workflow de validation.
**Incomplet** : dashboard compta (widgets à 0), textes de partenaire (Dorina) non relus par le client, fusion de plusieurs branches en attente d'arbitrage d'Allan, workflow "fin normale du contrat" codé mais pas déployé, mails partenaires (Leila/Kolos/Dorina) jamais envoyés pour les dossiers réels existants.

## Prochaines étapes probables
- Décider de la fusion des branches Git en attente (onboarding).
- Déployer le correctif "fin normale de contrat" (front + n8n) après vérification par Adam de l'option Notion `fin_normale`.
- Finir le dashboard compta (diagnostic des widgets à 0.00).
- Continuer à traiter les retours d'usage réel d'Adam au fil de l'eau (mode "run" plus que "build").

## Questions ouvertes
- **Revenus : non trouvé.** Aucune facture ni montant côté prestation Allan → AK Nutrition trouvé dans les fichiers (le dossier `facture/` documente la compta interne du client, pas la facturation d'Allan). Relation présentée comme un partenariat actif et récurrent (SynkroniseIA), mais aucun chiffre de contrat, forfait mensuel ou paiement reçu n'apparaît dans les fichiers texte.
- Ce projet semble être le plus gros investissement de temps d'Allan actuellement (32 sous-dossiers, historiques de dizaines de milliers de mots) — vérifier s'il est facturé à la hauteur du temps passé.
- Statut réel du go-live complet : plusieurs "en attente d'un humain" listés dans les derniers snapshots (validation Adam en conditions réelles sur plusieurs fonctionnalités).
