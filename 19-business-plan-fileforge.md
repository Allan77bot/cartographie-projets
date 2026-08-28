# PROJECT_SNAPSHOT — business-plan-fileforge

*Généré par audit de cartographie, 2026-08-28.*

## But

Rédiger le business plan d'une solution SaaS multi-tenant + hardware RFID qui digitalise les parties de paintball et d'airsoft : bornes sur le terrain, check-in joueurs, scénarios, scoring temps réel, suivi du matériel, dashboard centralisé pour les clubs. Nom produit : **FileForge**. Projet à 3 associés (Hubert Cots 52 %, Allan Morjon 24 %, Alphim Ntsatou 24 %), lancement visé début 2027 avec un client pilote.

## Contenu / Stack

- **Aucun code applicatif** : c'est un dépôt de rédaction de business plan uniquement (fichiers `.md` + un livrable HTML de présentation avec Chart.js).
- Structure : `CLAUDE.md` (pilotage), `ETAT.md` (snapshot vivant), `JOURNAL.md` (journal daté), `BUSINESS-PLAN.md` (document principal, 42 Ko), `docs/` (8 fichiers de fondation : marché, produit-tech, business-model, finances, juridique, go-to-market, équipe, pacte d'associés), `sources/` (comptes rendus de réunion), `recherche/` (étude de marché), `livrables/` (PDF pacte d'associés, HTML dashboard de présentation), `data/` (sorties Firecrawl).
- Stack technique visée par le produit décrit (pas construite ici) : Docker + Linux, PostgreSQL multi-tenant à schémas séparés, VPS, hardware RFID.
- Dépôt git présent (`.git`) mais rien n'indique de push (`ETAT.md` précise « pas de push »).

## État actuel

**Dernière modification : 15/07/2026** — inactif depuis 6 semaines par rapport à CORTEX. Stade : document de discussion chiffré en v1, pas encore validé en réunion d'équipe. Étude de marché livrée (note 68/100). Pacte d'associés v1 exporté en PDF. Pas de produit, pas de code, pas de client, pas de MVP.

## Ce qui est complet / incomplet

**Complet** :
- Analyse marché (`docs/01-marche.md`) — positionnement différenciant identifié (digitaliser la partie elle-même, pas la réservation).
- Fondations juridiques, go-to-market, équipe rédigées depuis le compte-rendu de réunion du 05/07/2026.
- Pacte d'associés v1 (PDF exporté).
- Dashboard HTML de présentation pour un rendez-vous.

**Incomplet** :
- BOM (bill of materials) par type de borne — bloquant, dépend de Hubert (prix du kit, marge matérielle).
- Chiffrage financier (`04-finances.md`) — squelette seulement.
- Coûts serveur/infra et jalons de dev — dépendent de Hubert.
- 7 décisions structurantes non tranchées en réunion d'équipe (ambition, cible pilote, prix/packs, juridique, brevet, structure sociétale, rémunération/finance).
- Montage juridique international (Lituanie/Londres) — risque fiscal « direction effective France » non purgé, fiscaliste pas encore consulté.
- Certification CE non budgétée.

## Prochaines étapes probables

- Réunion d'équipe pour trancher les 7 décisions en attente.
- Obtenir de Hubert le chiffrage technique/matériel/serveur.
- Consulter un fiscaliste international et un conseil en propriété intellectuelle (brevet).
- Finaliser le résumé exécutif une fois le kit chiffré.

## Questions ouvertes

- Aucune mention de revenu ou de client : projet 100 % pré-lancement, financé par réinvestissement (zéro salaire annoncé sur 2 ans).
- Le projet est en pause depuis mi-juillet — abandon, ou simplement en attente du livrable de Hubert ? Rien dans les fichiers ne permet de trancher.
- Dépendance forte à un tiers externe (Hubert, 52 % des parts) pour tout chiffrage technique : bloquant structurel si Hubert ne livre pas.
